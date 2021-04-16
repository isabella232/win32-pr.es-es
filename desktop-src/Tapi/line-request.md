---
description: El mensaje de solicitud de línea TAPI \_ se envía para informar de la llegada de una nueva solicitud desde otra aplicación.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: Mensaje de LINE_REQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690226"
---
# <a name="line_request-message"></a>Mensaje de solicitud de línea \_

El mensaje **de \_ solicitud de línea** TAPI se envía para informar de la llegada de una nueva solicitud desde otra aplicación.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de registro de la aplicación especificada en [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).

</dd> <dt>

*dwParam1* 
</dt> <dd>

Modo de solicitud de la solicitud recién pendiente. Este parámetro usa las [**\_ constantes LINEREQUESTMODE**](linerequestmode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Las condiciones para este parámetro son, si *dwParam1* se establece en LINEREQUESTMODE \_ Drop, *dwParam2* contiene el *hWnd* de la aplicación que solicita la eliminación. De lo contrario, *dwParam2* no se utiliza.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si *dwParam1* se establece en LINEREQUESTMODE \_ Drop, la palabra de orden inferior de *dwParam3* contiene el *wRequestID* tal como lo especifica la aplicación que solicitó la eliminación. De lo contrario, *dwParam3* no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje de **\_ solicitud de línea** se envía a la aplicación de prioridad más alta que se ha registrado para el modo de solicitud correspondiente. Este mensaje indica la llegada de una solicitud de telefonía asistida del modo de solicitud especificado. Si *dwParam1* es LINEREQUESTMODE \_ MAKECALL, la aplicación puede invocar [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) mediante el modo de solicitud correspondiente para recibir la solicitud. Si *dwParam1* es LINEREQUESTMODE \_ Drop, el mensaje contiene todos los datos que el destinatario de la solicitud necesita para realizar la solicitud.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[**tapiRequestMakeCall**](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




