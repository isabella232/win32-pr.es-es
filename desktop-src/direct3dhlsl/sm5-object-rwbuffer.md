---
title: RWBuffer
description: Búfer de lectura y escritura.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- RWBuffer HLSL
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963571"
---
# <a name="rwbuffer"></a>RWBuffer

Búfer de lectura y escritura.



| Método                                                     | Descripción                            |
|------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-rwbuffer-getdimensions.md) | Obtiene las dimensiones de recursos.          |
| [**Carga**](rwbuffer-load.md)                              | Obtiene un valor en un búfer de lectura y escritura. |
| [**Operador\[\]**](sm5-object-rwbuffer-operatorindex.md)  | Devuelve una variable de recurso.           |



 

También se puede pasar una variable de recurso a cualquier operación desordenada o entrelazado.

**Los objetos RWBuffer** pueden tener como prefijo la clase de almacenamiento **globalmentecoherente**. Esta clase de almacenamiento hace que las barreras de memoria y las sincronizaciones vaciarán los datos en toda la GPU para que otros grupos puedan ver escrituras. Sin este especificador, una barrera o sincronización de memoria vaciará un UAV solo dentro del grupo actual.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




