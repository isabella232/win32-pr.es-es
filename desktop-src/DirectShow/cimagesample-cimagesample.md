---
description: Método de constructor.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Constructor CImageSample. CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670490"
---
# <a name="cimagesamplecimagesample-constructor"></a>Constructor CImageSample. CImageSample

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAllocator* 
</dt> <dd>

Puntero al asignador que creó este ejemplo.

</dd> <dt>

*pName* 
</dt> <dd>

ignorado.

</dd> <dt>

*phr* 
</dt> <dd>

ignorado.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntero a un búfer de memoria asignado por el autor de la llamada, de *longitud* de tamaño. El búfer debe contener un mapa de bits independiente del dispositivo GDI (DIB).

</dd> <dt>

*length* 
</dt> <dd>

Longitud del búfer.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase [**CImageAllocator**](cimageallocator.md) crea un archivo DIB mediante un objeto de asignación de archivos respaldado por el archivo de paginación del sistema operativo. El identificador del objeto de asignación de archivos se almacena en el miembro **hMapping** de la estructura **m \_ DibData** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageSample**](cimagesample.md)
</dt> </dl>

 

 




