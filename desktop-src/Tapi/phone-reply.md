---
description: El mensaje TAPI PHONE REPLY se envía a una aplicación para informar de los \_ resultados de la llamada de función que se completó de forma asincrónica.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: PHONE_REPLY mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071079"
---
# <a name="phone_reply-message"></a>Mensaje \_ DE RESPUESTA TELEFÓNICA

El mensaje **TAPI PHONE \_ REPLY se** envía a una aplicación para informar de los resultados de la llamada de función que se completó de forma asincrónica.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Devuelve la instancia de devolución de llamada de la aplicación.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador de solicitud para el que se trata de la respuesta.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Indicación de error o correcto. La aplicación debe convertir este parámetro en LONG. Cero indica que se ha correcto; Un número negativo indica un error.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las funciones que operan de forma asincrónica devuelven un valor de identificador de solicitud positivo a la aplicación. Este identificador de solicitud se devuelve con el mensaje de respuesta para identificar la solicitud que se completó. El otro parámetro para el mensaje **PHONE \_ REPLY** lleva la indicación de éxito o error. Los posibles errores son los mismos que los definidos por la función correspondiente. Este mensaje no se puede deshabilitar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




