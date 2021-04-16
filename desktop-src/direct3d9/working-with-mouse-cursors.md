---
description: Los métodos de cursor del mouse permiten que la aplicación especifique un cursor de color proporcionando una superficie que contenga una imagen.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Trabajar con cursores del mouse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495563"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a><span data-ttu-id="81f0d-103">Trabajar con cursores del mouse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="81f0d-103">Working with Mouse Cursors (Direct3D 9)</span></span>

<span data-ttu-id="81f0d-104">Los métodos de cursor del mouse permiten que la aplicación especifique un cursor de color proporcionando una superficie que contenga una imagen.</span><span class="sxs-lookup"><span data-stu-id="81f0d-104">The mouse cursor methods enable the application to specify a color cursor by providing a surface that contains an image.</span></span> <span data-ttu-id="81f0d-105">El sistema garantizará que este cursor se actualizará a la mitad de la velocidad de presentación o más si la velocidad de fotogramas de la aplicación es lenta.</span><span class="sxs-lookup"><span data-stu-id="81f0d-105">The system will ensure that this cursor will be updated at half the display rate or more if the application's frame rate is slow.</span></span> <span data-ttu-id="81f0d-106">Sin embargo, el cursor nunca se actualizará con más frecuencia que la frecuencia de actualización de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="81f0d-106">However, the cursor will never be updated more frequently than the display refresh rate.</span></span>

<span data-ttu-id="81f0d-107">La posición del cursor del mouse está ligada al cursor del sistema, escalada correctamente para la resolución espacial del modo de presentación actual, pero la aplicación puede moverla explícitamente.</span><span class="sxs-lookup"><span data-stu-id="81f0d-107">The mouse cursor position is tied to the system cursor, appropriately scaled for the current display mode spatial resolution, but it can be moved explicitly by the application.</span></span> <span data-ttu-id="81f0d-108">Esto es análogo al comportamiento del cursor del mouse del sistema compatible con la API Win32.</span><span class="sxs-lookup"><span data-stu-id="81f0d-108">This is analogous to the behavior of the Win32 API - supported system mouse cursor.</span></span> <span data-ttu-id="81f0d-109">Para obtener más información sobre cómo usar un cursor del mouse en la aplicación Direct3D, vea los temas de referencia siguientes.</span><span class="sxs-lookup"><span data-stu-id="81f0d-109">For more information about how to use a mouse cursor in your Direct3D application, see the following reference topics.</span></span>

-   [<span data-ttu-id="81f0d-110">**IDirect3DDevice9::ShowCursor**</span><span class="sxs-lookup"><span data-stu-id="81f0d-110">**IDirect3DDevice9::ShowCursor**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [<span data-ttu-id="81f0d-111">**IDirect3DDevice9::SetCursorPosition**</span><span class="sxs-lookup"><span data-stu-id="81f0d-111">**IDirect3DDevice9::SetCursorPosition**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [<span data-ttu-id="81f0d-112">**IDirect3DDevice9::SetCursorProperties**</span><span class="sxs-lookup"><span data-stu-id="81f0d-112">**IDirect3DDevice9::SetCursorProperties**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

<span data-ttu-id="81f0d-113">Direct3D garantiza que el mouse es compatible con las implementaciones de hardware o con el tiempo de ejecución de Direct3D que realiza operaciones de blitting aceleradas por hardware al llamar a [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="81f0d-113">Direct3D ensures that the mouse is supported either by hardware implementations or by the Direct3D run time that performs hardware-accelerated blitting operations when calling [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81f0d-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81f0d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81f0d-115">Sugerencias de programación</span><span class="sxs-lookup"><span data-stu-id="81f0d-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
