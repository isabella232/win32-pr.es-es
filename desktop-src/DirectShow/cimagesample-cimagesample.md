---
description: 'Constructor CImageSample.CImageSample: método constructor.'
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Constructor CImageSample.CImageSample (Winutil.h)
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
ms.openlocfilehash: 4eeb15ec42daed1fa835eff28a4953b223d9782859bfcc23b174dee8fee65019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402535"
---
# <a name="cimagesamplecimagesample-constructor"></a>Constructor CImageSample.CImageSample

Método constructor.

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

*Phr* 
</dt> <dd>

ignorado.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntero a un búfer de memoria asignado por el autor de la llamada, de longitud *de tamaño*. El búfer debe contener un mapa de bits independiente del dispositivo GDI (DIB).

</dd> <dt>

*length* 
</dt> <dd>

Longitud del búfer.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [**clase CImageAllocator**](cimageallocator.md) crea una DIB mediante un objeto de asignación de archivos que está respaldo por el archivo de paginación del sistema operativo. El identificador del objeto de asignación de archivos se almacena en el **miembro hMapping** de la **estructura m \_ DibData.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImageSample (clase)**](cimagesample.md)
</dt> </dl>

 

 




