---
description: El método NotifyAllocator informa al objeto CDrawImage de si el asignador de la conexión es un objeto CImageAllocator.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Método CDrawImage.NotifyAllocator (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c40504c81ad404fec8bd442d243602ba90d6c7ffeb770e448a5cbe788d76428b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076355"
---
# <a name="cdrawimagenotifyallocator-method"></a>CDrawImage.NotifyAllocator (método)

El método informa al objeto CDrawImage de si el asignador de la `NotifyAllocator` conexión es un objeto [**CImageAllocator.**](cimageallocator.md) 

## <a name="syntax"></a>Sintaxis


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bUsingImageAllocator* 
</dt> <dd>

Valor booleano que indica qué tipo de asignador se está utilizando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El filtro propietario debe llamar a este método después de que los pines acepten un asignador. Si el filtro sabe que el asignador es **un objeto CImageAllocator,** debe llamar a este método con el valor **TRUE**. (Normalmente, el filtro lo sabrá solo si posee el asignador en cuestión). De lo contrario, debe llamar a este método con el **valor FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::D rawImage**](cdrawimage-drawimage.md)
</dt> </dl>

 

 




