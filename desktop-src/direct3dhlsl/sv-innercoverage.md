---
title: SV_InnerCoverage
description: Entrada SVCoverage representa información de rasterización conservadora subestimada (es decir, si se garantiza que un píxel esté totalmente \_ cubierto).
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
ms.openlocfilehash: e1ac278f0524446b5171ef278e169fbe7c3a082f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996972"
---
# <a name="sv_innercoverage"></a>SV \_ InnerCoverage

Entrada SVCoverage representa información de rasterización conservadora subestimada (es decir, si se garantiza que un píxel esté totalmente \_ cubierto).

## <a name="type"></a>Tipo



|      |
|------|
| Tipo |
| uint |



 

## <a name="remarks"></a>Comentarios

Este valor generado por el sistema es necesario para la compatibilidad con el nivel 3 y solo está disponible en ese nivel. Esta entrada es mutuamente excluyente con la cobertura \_ SV; no se pueden usar ambos.

Para acceder a SV InnerCoverage, debe declararse como un único componente de uno de los registros de entrada del \_ sombreador de píxeles. El modo de interpolación de la declaración debe ser constante (no se aplica la interpolación).

La rasterización conservadora está disponible en D3D11.3 y D3D12. Consulte

-   [Rasterización conservadora de D3D11.3](/windows/desktop/direct3d11/conservative-rasterization)
-   [Rasterización conservadora de D3D12](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Modelos de sombreador 5.1 Valores del sistema](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
