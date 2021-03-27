---
title: SV_InnerCoverage
description: SV \_ InputCoverage representa la información de rasterización conservadora desestimada (es decir, si se garantiza que un píxel está totalmente incluido).
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
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997141"
---
# <a name="sv_innercoverage"></a>VP \_ InnerCoverage

SV \_ InputCoverage representa la información de rasterización conservadora desestimada (es decir, si se garantiza que un píxel está totalmente incluido).

## <a name="type"></a>Tipo



|      |
|------|
| Tipo |
| uint |



 

## <a name="remarks"></a>Observaciones

Este valor generado por el sistema es necesario para la compatibilidad de nivel 3 y solo está disponible en ese nivel. Esta entrada es mutuamente excluyente con la \_ cobertura de SV; no se pueden usar las dos.

Para tener acceso a \_ la InnerCoverage de SV, debe declararse como un componente único de uno de los registros de entrada del sombreador de píxeles. El modo de interpolación en la declaración debe ser constante (no se aplica la interpolación).

La rasterización conservadora está disponible tanto en D3D 11.3 como en D3D12. Consulte

-   [Rasterización conservadora de D3D 11.3](/windows/desktop/direct3d11/conservative-rasterization)
-   [Rasterización conservadora D3D12](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Modelo de sombreador 5,1 valores del sistema](shader-model-5-1-system-values.md)
</dt> </dl>

 

 