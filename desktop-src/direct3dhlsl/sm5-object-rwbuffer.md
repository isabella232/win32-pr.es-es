---
title: RWBuffer
description: Un búfer de lectura/escritura.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- HLSL de RWBuffer
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
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358113"
---
# <a name="rwbuffer"></a>RWBuffer

Un búfer de lectura/escritura.



| Método                                                     | Descripción                            |
|------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-rwbuffer-getdimensions.md) | Obtiene las dimensiones de recursos.          |
| [**Carga**](rwbuffer-load.md)                              | Obtiene un valor en un búfer de lectura y escritura. |
| [**Operador\[\]**](sm5-object-rwbuffer-operatorindex.md)  | Devuelve una variable de recurso.           |



 

También se puede pasar una variable de recurso a cualquier operación sin ordenar o interbloqueada.

Los objetos **RWBuffer** pueden ir precedidos de la clase de almacenamiento **globallycoherent**. Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras. Sin este especificador, una barrera de memoria o una sincronización vaciará un UAV solo dentro del grupo actual.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




