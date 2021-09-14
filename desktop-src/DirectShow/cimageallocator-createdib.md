---
description: El método CreateDIB crea un mapa de bits independiente del dispositivo (DIB) de GDI. La DIB se asigna en un bloque mempory compartido, que elimina una operación de copia cuando el filtro propietario bloquea la imagen.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Método CImageAllocator.CreateDIB (Winutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170037"
---
# <a name="cimageallocatorcreatedib-method"></a>CImageAllocator.CreateDIB (método)

El `CreateDIB` método crea un mapa de bits independiente del dispositivo GDI (DIB). La DIB se asigna en un bloque mempory compartido, que elimina una operación de copia cuando el filtro propietario bloquea la imagen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InSize* 
</dt> <dd>

Tamaño del mapa de bits.

</dd> <dt>

*DibData* \[ Ref\]
</dt> <dd>

Referencia a una [**estructura DIBDATA.**](dibdata.md) El método rellena esta estructura con información sobre la DIB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un código de error de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageAllocator (clase)**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator::Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




