# CMakeのバージョン
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
# リリースビルド用オプション
SET(CMAKE_CXX_FLAGS_RELEASE "-Wall -O2")
# デバッグビルド用オプション
SET(CMAKE_CXX_FLAGS_DEBUG "-Wall -g")
# ビルドのタイプはリリース
SET(CMAKE_BUILD_TYPE Release)
# プロジェクト名
PROJECT(myapp)


# ライブラリを検索
# find_package(GLUT)
# find_package(OpenGL)
# find_package(GLEW)




# インクルード指定
include_directories(
	${PROJECT_SOURCE_DIR}/includes
)
# ライブラリ指定
link_directories(
	${PROJECT_SOURCE_DIR}/lib
)


# subdir指定
# SUBDIRS(${PROJECT_SOURCE_DIR}/a)


# ライブラリ作成
#ADD_LIBRARY(a STATIC ${PROJECT_SOURCE_DIR}/src/a.cpp)
# バージョン番号
# SET(serial "0.1.0")
# 共有ライブラリのバージョン番号
# SET(soserial "0")
# バージョン番号の適用
#SET_TARGET_PROPERTIES(unarray PROPERTIES VERSION ${serial} SOVERSION ${soserial})
# 共有ライブラリのインストール指定
#INSTALL(TARGETS unarray LIBRARY DESTINATION lib)
# 共有ライブラリ用ヘッダーファイルのインストール指定
#INSTALL(FILES unarray.h DESTINATION include)
# ライブラリインストール
#INSTALL(TARGETS a DESTINATION ${PROJECT_SOURCE_DIR}/lib)



# 実行ファイル作成
add_executable(myapp ${PROJECT_SOURCE_DIR}/src/main.cpp)
# リンク
TARGET_LINK_LIBRARIES(myapp)

