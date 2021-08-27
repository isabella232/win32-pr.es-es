---
description: El mensaje TAPI LINE REQUEST se envía para informar de la llegada \_ de una nueva solicitud desde otra aplicación.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: LINE_REQUEST mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cd49b14aafabfdd4d7ab37c5f2beec1487a08a53385ae8a1439b7443d49cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126235"
---
# <a name="line_request-message"></a>Mensaje \_ DE SOLICITUD DE LÍNEA

El mensaje TAPI **LINE \_ REQUEST se** envía para informar de la llegada de una nueva solicitud desde otra aplicación.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

No se usa.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de registro de la aplicación especificada en [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).

</dd> <dt>

*dwParam1* 
</dt> <dd>

Modo de solicitud de la solicitud recién pendiente. Este parámetro usa las [**constantes LINEREQUESTMODE \_**](linerequestmode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Las condiciones para este parámetro son: si *dwParam1* se establece en LINEREQUESTMODE \_ DROP, *dwParam2* contiene *el hWnd* de la aplicación que solicita la colocación. De lo contrario, *dwParam2* no se usa.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si *dwParam1* se establece en LINEREQUESTMODE DROP, la palabra de orden bajo \_ de *dwParam3* contiene *el wRequestID* especificado por la aplicación que solicitó la colocación. De lo contrario, *dwParam3* no se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **mensaje \_ LINE REQUEST** se envía a la aplicación de prioridad más alta que se ha registrado para el modo de solicitud correspondiente. Este mensaje indica la llegada de una solicitud de telefonía asistida del modo de solicitud especificado. Si *dwParam1* es LINEREQUESTMODE MAKECALL, la aplicación puede invocar lineGetRequest mediante el modo de solicitud \_ correspondiente para recibir la solicitud. [](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) Si *dwParam1* es LINEREQUESTMODE DROP, el mensaje contiene todos los datos que el destinatario de la solicitud \_ necesita para realizar la solicitud.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[**tapiRequestMakeCall**](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




