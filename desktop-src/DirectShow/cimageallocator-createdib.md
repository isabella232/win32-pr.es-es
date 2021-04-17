---
description: El método CreateDIB crea un mapa de bits independiente del dispositivo GDI (DIB). El DIB se asigna en un bloque mempory compartido, que elimina una operación de copia cuando el filtro propietario blits la imagen.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Método CImageAllocator. CreateDIB (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680515"
---
# <a name="cimageallocatorcreatedib-method"></a>CImageAllocator. CreateDIB, método

El `CreateDIB` método crea un mapa de bits independiente del dispositivo GDI (DIB). El DIB se asigna en un bloque mempory compartido, que elimina una operación de copia cuando el filtro propietario blits la imagen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Insize* 
</dt> <dd>

Tamaño del mapa de bits.

</dd> <dt>

*DibData* \[ CLI\]
</dt> <dd>

Referencia a una estructura [**DIBDATA**](dibdata.md) . El método rellena esta estructura con información sobre el DIB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o un código de error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageAllocator**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator:: Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




