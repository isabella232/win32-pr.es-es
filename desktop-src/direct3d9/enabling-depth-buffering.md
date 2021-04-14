---
description: 'Después de crear un búfer de profundidad, como se describe en crear un búfer de profundidad (Direct3D 9), puede habilitar el almacenamiento en búfer de profundidad llamando al método IDirect3DDevice9:: SetRenderState.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Habilitar el almacenamiento en búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359884"
---
# <a name="enabling-depth-buffering-direct3d-9"></a><span data-ttu-id="ba222-103">Habilitar el almacenamiento en búfer de profundidad (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ba222-103">Enabling Depth Buffering (Direct3D 9)</span></span>

<span data-ttu-id="ba222-104">Después de crear un búfer de profundidad, como se describe en [crear un búfer de profundidad (Direct3D 9)](creating-a-depth-buffer.md), puede habilitar el almacenamiento en búfer de profundidad llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ba222-104">After you create a depth buffer, as described in [Creating a Depth Buffer (Direct3D 9)](creating-a-depth-buffer.md), you enable depth buffering by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ba222-105">Establezca el estado de representación de ZENABLE de D3DRS \_ para habilitar el almacenamiento en búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="ba222-105">Set the D3DRS\_ZENABLE render state to enable depth-buffering.</span></span> <span data-ttu-id="ba222-106">Use el \_ miembro true D3DZB del tipo enumerado [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) (o **true**) para habilitar el almacenamiento en búfer z, D3DZB \_ USEW para habilitar el almacenamiento en búfer de w o D3DZB \_ false (o **false**) para deshabilitar el almacenamiento en búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="ba222-106">Use the D3DZB\_TRUE member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type (or **TRUE**) to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE (or **FALSE**) to disable depth buffering.</span></span>

> [!Note]  
> <span data-ttu-id="ba222-107">Para usar el almacenamiento en búfer de w, la aplicación debe establecer una matriz de proyección compatible incluso si no usa la canalización de transformación de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ba222-107">To use w-buffering, your application must set a compliant projection matrix even if it doesn't use the Direct3D transformation pipeline.</span></span> <span data-ttu-id="ba222-108">Para obtener información sobre cómo proporcionar una matriz de proyección adecuada, vea [una matriz de proyección fácil](projection-transform.md)</span><span class="sxs-lookup"><span data-stu-id="ba222-108">For information about providing an appropriate projection matrix, see [A W-Friendly Projection Matrix](projection-transform.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ba222-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba222-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba222-110">Búferes de profundidad</span><span class="sxs-lookup"><span data-stu-id="ba222-110">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
