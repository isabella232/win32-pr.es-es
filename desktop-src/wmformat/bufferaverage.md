---
title: BufferAverage
description: El atributo BufferAverage contiene el tamaño de búfer promedio necesario para una secuencia de velocidad de bits variable (VBR).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- BufferAverage formato de Windows Media
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148946"
---
# <a name="bufferaverage"></a>BufferAverage

El atributo **BufferAverage** contiene el tamaño de búfer promedio necesario para una secuencia de velocidad de bits variable (VBR).

## <a name="global-constant"></a>Constante global

g \_ wszBufferAverage

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ DWORD**

## <a name="remarks"></a>Observaciones

Al tener acceso a la interfaz **IWMHeaderInfo3** del objeto escritor, puede Agregar o cambiar este valor. En otros objetos (editor de metadatos, lector y lector sincrónico), este valor es de solo lectura.

El escritor escribe automáticamente un valor de **BufferAverage** para cada secuencia VBR.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




