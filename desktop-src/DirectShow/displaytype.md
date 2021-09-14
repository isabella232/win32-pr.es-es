---
description: La función DisplayType envía información sobre un tipo de medio a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: Función DisplayType (Wxdebug.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061672"
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

Cadena que contiene un mensaje que se mostrará con la información del tipo de medio.

</dd> <dt>

*pmtIn* 
</dt> <dd>

ointer a la [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contiene el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función genera varios mensajes LOG \_ TRACE. En el nivel de registro 2 o superior, la función muestra el tipo principal, el subtipo y el tipo de formato, así como los datos del bloque de formato. En el nivel de registro 5 o superior, la función muestra información adicional, como los rectángulos de origen y de destino para los tipos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 




