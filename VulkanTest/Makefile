VULKAN_SDK_PATH = $(PATH)
CFLAGS = -std=c++17 -I$(VULKAN_SDK_PATH)/include
LDFLAGS = -L$(VULKAN_SDK_PATH)/lib `pkg-config --static --libs glfw3` -lvulkan
VulkanTest:
	g++ $(CFLAGS) -o VulkanTest main.cpp $(LDFLAGS)

.PHONY: test clean

test: VulkanTest
	VK_LAYER_PATH=/usr/share/vulkan/explicit_layer.d
	./VulkanTest

clean:
	rm -f VulkanTest