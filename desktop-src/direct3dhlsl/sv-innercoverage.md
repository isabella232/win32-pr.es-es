---
title: SV_InnerCoverage
description: Entrada SVCoverage representa información de rasterización conservadora infravalorada (es decir, si se garantiza que un píxel esté totalmente \_ cubierto).
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172ee60cb85e69568c8cb226aa19fa325686726f42fc27c7aa21231b1a55ef28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724383"
---
# <a name="sv_innercoverage"></a>SV \_ InnerCoverage

Entrada SVCoverage representa información de rasterización conservadora infravalorada (es decir, si se garantiza que un píxel esté totalmente \_ cubierto).

## <a name="type"></a>Tipo



| Tipo     |
|------|
| uint |



 

## <a name="remarks"></a>Comentarios

Este valor generado por el sistema es necesario para la compatibilidad con el nivel 3 y solo está disponible en ese nivel. Esta entrada es mutuamente excluyente con la cobertura \_ SV; ambos no se pueden usar.

Para acceder a SV InnerCoverage, debe declararse como un único componente de uno de los registros de entrada del \_ sombreador de píxeles. El modo de interpolación de la declaración debe ser constante (no se aplica la interpolación).

La rasterización conservadora está disponible en D3D11.3 y D3D12. Consulte

-   [Rasterización conservadora de D3D11.3](/windows/desktop/direct3d11/conservative-rasterization)
-   [Rasterización conservadora de D3D12](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Valores del sistema del modelo de sombreador 5.1](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
