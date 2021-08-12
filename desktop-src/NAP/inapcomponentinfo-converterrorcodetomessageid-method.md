---
title: Método INapComponentInfo ConvertErrorCodeToMessageId (NapCommon.h)
description: Lo usa el sistema NAP para solicitar que el cliente de mantenimiento convierta un código de error HRESULT en un identificador de mensaje.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Nap del método ConvertErrorCodeToMessageId
- Método NAP ConvertErrorCodeToMessageId , interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método ConvertErrorCodeToMessageId
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c670585674713d114f6505a0c3211d599663545f6b06a40669f7fba8b7eddf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621734"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a>Método INapComponentInfo::ConvertErrorCodeToMessageId

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP usa el método de devolución de llamada **INapComponentInfo::ConvertErrorCodeToMessageId** para solicitar al cliente de mantenimiento que convierta un código de error HRESULT en un identificador de mensaje.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*errorCode* \[ En\]
</dt> <dd>

Código [**de error**](nap-error-constants.md) del sistema NAP que se va a convertir en **messageId**.

</dd> <dt>

*msgId* \[ out\]
</dt> <dd>

Puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso de la cadena localizada correspondiente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de estos códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

El sistema **NAP usa el MessageId** devuelto para recuperar una cadena localizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





