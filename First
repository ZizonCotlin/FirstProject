import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

# 건축물의 기본 형태를 정의하는 변수들
length = 10  # 길이
width = 10   # 너비
height = 10  # 높이

# 건축물의 꼭지점 좌표 생성
corners = np.array([[0, 0, 0],
                    [length, 0, 0],
                    [length, width, 0],
                    [0, width, 0],
                    [0, 0, height],
                    [length, 0, height],
                    [length, width, height],
                    [0, width, height]])

# 각 벽면을 구성하는 꼭지점 인덱스
faces = [[0, 1, 5, 4],
         [1, 2, 6, 5],
         [2, 3, 7, 6],
         [3, 0, 4, 7],
         [4, 5, 6, 7],
         [0, 3, 2, 1]]

# 3D 시각화
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# 벽면을 그리는 과정
for face in faces:
    ax.add_collection3d(Poly3DCollection([corners[face]], facecolors='cyan', linewidths=1, edgecolors='r', alpha=.25))

ax.scatter(corners[:,0], corners[:,1], corners[:,2], c='black')

# 축의 한계 설정
ax.set_xlabel('X')
ax.set_ylabel('Y')
ax.set_zlabel('Z')
ax.set_xlim([0, length+5])
ax.set_ylim([0, width+5])
ax.set_zlim([0, height+5])

plt.show()
