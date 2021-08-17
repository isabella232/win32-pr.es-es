---
title: BufferAverage
description: El atributo BufferAverage contiene el tamaño medio del búfer necesario para una secuencia de velocidad de bits variable (VBR).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- BufferAverage windows Media Format
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd839bff96f5ba327e585f8608bd4612fc047d354c24fee972e507ea5ca681f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656125"
---
# <a name="bufferaverage"></a>BufferAverage

El **atributo BufferAverage** contiene el tamaño medio de búfer necesario para una secuencia de velocidad de bits variable (VBR).

## <a name="global-constant"></a>Constante global

g \_ wszBufferAverage

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Al acceder a **la interfaz IWMHeaderInfo3** del objeto de escritor, puede agregar o cambiar este valor. En otros objetos (editor de metadatos, lector y lector sincrónico), este valor es de solo lectura.

El sistema de escritura escribe automáticamente un valor **BufferAverage** para cada secuencia de VBR.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




