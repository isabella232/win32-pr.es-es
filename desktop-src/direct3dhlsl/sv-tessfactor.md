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
ms.openlocfilehash: 308034fe607283ef9f1213cca1cabb4a7229765e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974666"
---
# <a name="sv_tessfactor"></a>SV \_ TessFactor

Define la cantidad de teselación en cada borde de una revisión.

## <a name="type"></a>Tipo



|  Tipo          |  Topología de entrada              |
|------------|----------------|
| float \[ 4\] | revisión quad     |
| float \[ 3\] | tri patch      |
| float \[ 2\] | Isolínea        |



 

Los factores de teselación deben declararse como una matriz; no se pueden empaquetar en un solo vector.

## <a name="remarks"></a>Observaciones

El valor del factor de teselación debe definirse durante la función de constante de revisión del sombreador de casco.

Valor de salida necesario para el sombreador de casco si se usan revisiones quad o tri. Este valor también es un valor de entrada necesario para que el sombreador de dominio coincida con las firmas de datos de revisión constante entre las fases de teselación.

Para una isolínea, el primer valor de SV TessFactor es el factor de teselación de densidad de línea, el segundo valor es el factor de teselación de detalle \_ de línea.

### <a name="tri-patch-tessellation-factors"></a>Tres factores de teselación de revisión

El primer componente proporciona el factor de tesselation para el borde u==0 de la revisión. El segundo componente proporciona el factor de tesselation para el borde v==0 de la revisión. El tercer componente proporciona el factor de tesselation para el borde w==0 de la revisión.

### <a name="quad-patch-tessellation-factors"></a>Factores de teselación de cuatro revisiones

El primer componente proporciona el factor de tesselation para el borde u==0 de la revisión. El segundo componente proporciona el factor de tesselation para el borde v==0 de la revisión. El tercer componente proporciona el factor de tesselation para el borde u==1 de la revisión. El cuarto componente proporciona el factor de tesselation para el borde v==1 de la revisión. El orden de los bordes es en el sentido de las agujas del reloj, empezando por el borde u==0, que es el lado izquierdo de la revisión, y desde el borde v==0, que es la parte superior de la revisión.

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




