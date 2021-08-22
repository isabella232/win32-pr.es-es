---
title: SV_TessFactor
description: Define la cantidad de teselación en cada borde de una revisión.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2243827fa1b955079aaf64b9805cf02ac82934bde814ed780570a5ba9b63ade8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285501"
---
# <a name="sv_tessfactor"></a>SV \_ TessFactor

Define la cantidad de teselación en cada borde de una revisión.

## <a name="type"></a>Tipo



|  Tipo          |  Topología de entrada              |
|------------|----------------|
| float \[ 4\] | revisión quad     |
| float \[ 3\] | revisión tri      |
| float \[ 2\] | Isolínea        |



 

Los factores de teselación deben declararse como una matriz; no se pueden empaquetar en un solo vector.

## <a name="remarks"></a>Comentarios

El valor del factor de teselación debe definirse durante la función de constante de revisión del sombreador de casco.

Valor de salida requerido para el sombreador de casco si se usan revisiones quad o tri. Este valor también es un valor de entrada necesario para que el sombreador de dominio coincida con las firmas de datos de constante de revisión entre las fases de teselación.

Para una isolínea, el primer valor de SV TessFactor es el factor de teselación de densidad de línea; el segundo valor es el factor de teselación de detalle \_ de línea.

### <a name="tri-patch-tessellation-factors"></a>Factores de teselación de tres revisiones

El primer componente proporciona el factor de tejida para el borde u==0 de la revisión. El segundo componente proporciona el factor de tejida para el borde v==0 de la revisión. El tercer componente proporciona el factor de tejida para el borde w==0 de la revisión.

### <a name="quad-patch-tessellation-factors"></a>Factores de teselación de revisiones cuadránticas

El primer componente proporciona el factor de tejida para el borde u==0 de la revisión. El segundo componente proporciona el factor de tejida para el borde v==0 de la revisión. El tercer componente proporciona el factor de tejida para el borde u==1 de la revisión. El cuarto componente proporciona el factor de tejida para el borde v==1 de la revisión. El orden de los bordes es en el sentido de las agujas del reloj, empezando por el borde u==0, que es el lado izquierdo de la revisión, y desde el borde v==0, que es la parte superior de la revisión.

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




