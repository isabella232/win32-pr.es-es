---
title: OutputPatch
description: OutputPatch
ms.assetid: 24841938-6c84-4e1f-ba8a-a81b589bdd51
keywords:
- OutputPatch HLSL
topic_type:
- apiref
api_name:
- OutputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea806da8fe9b4219490c26b84e5b77f6f92b324a72850c79080de6ca363ef4e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725244"
---
# <a name="outputpatch"></a>OutputPatch

Representa una matriz de puntos de control de salida que están disponibles para la función patch-constant del sombreador de casco, así como para el sombreador de dominio.



| Método                                                       | Descripción                         |
|--------------------------------------------------------------|-------------------------------------|
| [**Operador\[\]**](sm5-object-outputpatch-operatorindex.md) | Obtiene una variable de recurso de solo lectura. |



 

Además, la clase InputPatch admite las siguientes propiedades:



| Propiedades | Tipo | Descripción                   |
|------------|------|-------------------------------|
| Length     | uint | Número de puntos de control. |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




