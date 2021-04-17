---
description: Los primitivos que no tienen texturas se representan con el color especificado por su material o con los colores especificados para los vértices, si los hay.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Esquema y estado de relleno (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714673"
---
# <a name="outline-and-fill-state-direct3d-9"></a><span data-ttu-id="324b6-103">Esquema y estado de relleno (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="324b6-103">Outline and Fill State (Direct3D 9)</span></span>

<span data-ttu-id="324b6-104">Los primitivos que no tienen texturas se representan con el color especificado por su material o con los colores especificados para los vértices, si los hay.</span><span class="sxs-lookup"><span data-stu-id="324b6-104">Primitives that have no textures are rendered with the color specified by their material, or with the colors specified for the vertices, if any.</span></span> <span data-ttu-id="324b6-105">Puede seleccionar el método para rellenarlos especificando un valor definido por el tipo enumerado [**D3DFILLMODE**](./d3dfillmode.md) para el estado de \_ representación de D3DRS FILLMODE.</span><span class="sxs-lookup"><span data-stu-id="324b6-105">You can select the method to fill them by specifying a value defined by the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type for the D3DRS\_FILLMODE render state.</span></span>

<span data-ttu-id="324b6-106">Para habilitar el tramado, la aplicación debe pasar el \_ valor enumerado de D3DRS DITHERENABLE como primer parámetro a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="324b6-106">To enable dithering, your application must pass the D3DRS\_DITHERENABLE enumerated value as the first parameter to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span> <span data-ttu-id="324b6-107">Debe establecer el segundo parámetro en **true** para habilitar el tramado y **false** para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="324b6-107">It must set the second parameter to **TRUE** to enable dithering, and **FALSE** to disable it.</span></span>

<span data-ttu-id="324b6-108">En ocasiones, dibujar el último píxel en una línea puede provocar una superposición de forma no valiosa con los primitivos circundantes.</span><span class="sxs-lookup"><span data-stu-id="324b6-108">At times, drawing the last pixel in a line can cause unsightly overlap with surrounding primitives.</span></span> <span data-ttu-id="324b6-109">Puede controlar esto mediante el \_ valor enumerado de D3DRS LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="324b6-109">You can control this using the D3DRS\_LASTPIXEL enumerated value.</span></span> <span data-ttu-id="324b6-110">Sin embargo, no modifique este valor sin ningún preprevisión.</span><span class="sxs-lookup"><span data-stu-id="324b6-110">However, do not alter this setting without some forethought.</span></span> <span data-ttu-id="324b6-111">En algunas condiciones, suprimir la representación del último píxel puede producir brechas de percepción entre primitivas.</span><span class="sxs-lookup"><span data-stu-id="324b6-111">Under some conditions, suppressing the rendering of the last pixel can cause unsightly gaps between primitives.</span></span>

<span data-ttu-id="324b6-112">Los contornos de objeto se pueden dibujar estableciendo el patrón de dibujo de línea adecuado.</span><span class="sxs-lookup"><span data-stu-id="324b6-112">Object outlines can be drawn by setting the appropriate line drawing pattern.</span></span> <span data-ttu-id="324b6-113">El estado de dibujo de línea predeterminado es dibujar líneas sólidas.</span><span class="sxs-lookup"><span data-stu-id="324b6-113">The default line drawing state is to draw solid lines.</span></span> <span data-ttu-id="324b6-114">Para obtener más información, consulte [compatibilidad con el dibujo de líneas en el estado de representación de D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) .</span><span class="sxs-lookup"><span data-stu-id="324b6-114">For more information, see [Line Drawing Support in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) render state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="324b6-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="324b6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="324b6-116">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="324b6-116">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
