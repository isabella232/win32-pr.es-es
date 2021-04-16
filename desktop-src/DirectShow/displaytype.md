---
description: La función DisplayType envía información sobre un tipo de medio a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: Función DisplayType (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3d83bbe7a24463fc4cfaed4ace3adec9d6fcf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680270"
---
# <a name="displaytype-function"></a>Función DisplayType

La `DisplayType` función envía información sobre un tipo de medio a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*label* 
</dt> <dd>

Cadena que contiene un mensaje que se va a mostrar con la información del tipo de archivo multimedia.

</dd> <dt>

*pmtIn* 
</dt> <dd>

ointer a la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contiene el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función genera varios mensajes de seguimiento de registro \_ . En el nivel de registro 2 o superior, la función muestra el tipo principal, el subtipo y el tipo de formato, y los datos del bloque de formato. En el nivel de registro 5 o superior, la función muestra información adicional, como los rectángulos de origen y de destino para los tipos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 




