---
description: El \_ mensaje de respuesta del teléfono TAPI se envía a una aplicación para informar de los resultados de la llamada a función que se completó de forma asincrónica.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: Mensaje de PHONE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689943"
---
# <a name="phone_reply-message"></a>Mensaje de respuesta de teléfono \_

El mensaje **de \_ respuesta del teléfono** TAPI se envía a una aplicación para informar de los resultados de la llamada a función que se completó de forma asincrónica.


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

Identificador de solicitud para el que es la respuesta.

</dd> <dt>

*dwParam2* 
</dt> <dd>

La indicación de error o correcto. La aplicación debe convertir este parámetro en un valor LONG. Cero indica que se ha realizado correctamente; un número negativo indica un error.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las funciones que operan de forma asincrónica devuelven un valor de identificador de solicitud positivo a la aplicación. Este identificador de solicitud se devuelve con el mensaje de respuesta para identificar la solicitud que se completó. El otro parámetro del mensaje **de \_ respuesta del teléfono** contiene la indicación de éxito o error. Los errores posibles son los mismos que los definidos por la función correspondiente. Este mensaje no se puede deshabilitar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




