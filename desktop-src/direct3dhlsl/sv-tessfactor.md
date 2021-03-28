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
ms.openlocfilehash: 8fa49b19109985b590747098826199b33a32dd2d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104983767"
---
# <a name="sv_tessfactor"></a>VP \_ TessFactor

Define la cantidad de teselación en cada borde de una revisión.

## <a name="type"></a>Tipo



|            |                |
|------------|----------------|
| Tipo       | Topología de entrada |
| Float \[ 4\] | revisión cuádruple     |
| Float \[ 3\] | Tri patch      |
| Float \[ 2\] | isolínea        |



 

Los factores de teselación se deben declarar como una matriz; no se pueden empaquetar en un único vector.

## <a name="remarks"></a>Observaciones

El valor del factor de teselación debe definirse durante la función de constante patch del sombreador de casco.

Valor de salida necesario para el sombreador de casco si se usan cuatro o tres revisiones. Este valor también es un valor de entrada necesario para que el sombreador de dominios coincida con las firmas de datos constantes de revisión entre las fases de teselación.

En el caso de una isolínea, el primer valor de VP \_ TessFactor es el factor de teselación de densidad de línea, el segundo valor es el factor de teselación de detalles de línea.

### <a name="tri-patch-tessellation-factors"></a>Tri factores de teselación de revisiones

El primer componente proporciona el factor tesselation para el borde u = = 0 de la revisión. El segundo componente proporciona el factor tesselation para el borde v = = 0 de la revisión. El tercer componente proporciona el factor tesselation para el borde w = = 0 de la revisión.

### <a name="quad-patch-tessellation-factors"></a>Factores de teselación de cuatro revisiones

El primer componente proporciona el factor tesselation para el borde u = = 0 de la revisión. El segundo componente proporciona el factor tesselation para el borde v = = 0 de la revisión. El tercer componente proporciona el factor tesselation para el borde u = = 1 de la revisión. El cuarto componente proporciona el factor tesselation para el borde v = = 1 de la revisión. El orden de los bordes es en el sentido de las agujas del reloj, empezando desde el borde u = = 0, que es el lado izquierdo de la revisión, y desde el borde v = = 0, que es la parte superior de la revisión.

Esta función se admite en los siguientes tipos de sombreadores:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




