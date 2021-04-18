---
description: El almacenamiento en búfer de profundidad es un método para quitar líneas y superficies ocultas. De forma predeterminada, Direct3D no usa el almacenamiento en búfer de profundidad.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Estado de almacenamiento en búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494920"
---
# <a name="depth-buffering-state-direct3d-9"></a><span data-ttu-id="3ed7f-104">Estado de almacenamiento en búfer de profundidad (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3ed7f-104">Depth Buffering State (Direct3D 9)</span></span>

<span data-ttu-id="3ed7f-105">El almacenamiento en búfer de profundidad es un método para quitar líneas y superficies ocultas.</span><span class="sxs-lookup"><span data-stu-id="3ed7f-105">Depth buffering is a method of removing hidden lines and surfaces.</span></span> <span data-ttu-id="3ed7f-106">De forma predeterminada, Direct3D no usa el almacenamiento en búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="3ed7f-106">By default, Direct3D does not use depth buffering.</span></span>

<span data-ttu-id="3ed7f-107">Para obtener información general conceptual de los búferes de profundidad, vea [búferes de profundidad (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="3ed7f-107">For a conceptual overview of depth buffers, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="3ed7f-108">Las aplicaciones de C++ actualizan el estado de almacenamiento en búfer de profundidad con el \_ Estado de representación de ZENABLE de D3DRS, mediante un miembro de la enumeración [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) para especificar el nuevo valor de estado.</span><span class="sxs-lookup"><span data-stu-id="3ed7f-108">C++ applications update the depth-buffering state with the D3DRS\_ZENABLE render state, using a member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumeration to specify the new state value.</span></span>

<span data-ttu-id="3ed7f-109">Si la aplicación necesita impedir que Direct3D escriba en el búfer de profundidad, puede usar el \_ valor enumerado D3DRS ZWRITEENABLE, especificando D3DZB \_ false como el segundo parámetro para la llamada a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="3ed7f-109">If your application needs to prevent Direct3D from writing to the depth buffer, it can use the D3DRS\_ZWRITEENABLE enumerated value, specifying D3DZB\_FALSE as the second parameter for the call to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="3ed7f-110">En el ejemplo de código siguiente se muestra cómo se establece el estado del búfer de profundidad para habilitar el almacenamiento en búfer z.</span><span class="sxs-lookup"><span data-stu-id="3ed7f-110">The following code example shows how the depth-buffer state is set to enable z-buffering.</span></span>


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



<span data-ttu-id="3ed7f-111">La aplicación también puede usar el estado de representación de D3DRS \_ ZFUNC para controlar la función de comparación que usa Direct3D al realizar el almacenamiento en búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="3ed7f-111">Your application can also use the D3DRS\_ZFUNC render state to control the comparison function that Direct3D uses when performing depth buffering.</span></span>

<span data-ttu-id="3ed7f-112">La inclinación de Z es un método para mostrar una superficie delante de otra, incluso si sus valores de profundidad son los mismos.</span><span class="sxs-lookup"><span data-stu-id="3ed7f-112">Z-biasing is a method of displaying one surface in front of another, even if their depth values are the same.</span></span> <span data-ttu-id="3ed7f-113">Puede utilizar esta técnica para diversos efectos.</span><span class="sxs-lookup"><span data-stu-id="3ed7f-113">You can use this technique for a variety of effects.</span></span> <span data-ttu-id="3ed7f-114">Un ejemplo común es la representación de sombras en las paredes.</span><span class="sxs-lookup"><span data-stu-id="3ed7f-114">A common example is rendering shadows on walls.</span></span> <span data-ttu-id="3ed7f-115">Tanto la sombra como la pared tienen el mismo valor de profundidad.</span><span class="sxs-lookup"><span data-stu-id="3ed7f-115">Both the shadow and the wall have the same depth value.</span></span> <span data-ttu-id="3ed7f-116">Sin embargo, desea que la aplicación muestre la sombra en la pared.</span><span class="sxs-lookup"><span data-stu-id="3ed7f-116">However, you want your application to show the shadow on the wall.</span></span> <span data-ttu-id="3ed7f-117">La asignación de una diferencia de z a la sombra hace que Direct3D las muestre correctamente (consulte D3DRS \_ DEPTHBIAS).</span><span class="sxs-lookup"><span data-stu-id="3ed7f-117">Giving a z-bias to the shadow makes Direct3D display them properly (see D3DRS\_DEPTHBIAS).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ed7f-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3ed7f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ed7f-119">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="3ed7f-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
