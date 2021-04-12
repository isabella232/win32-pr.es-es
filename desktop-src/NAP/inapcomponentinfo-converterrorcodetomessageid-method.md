---
title: Método INapComponentInfo ConvertErrorCodeToMessageId (NapCommon. h)
description: Lo usa el sistema NAP para solicitar al cliente de mantenimiento que convierta un código de error HRESULT en un ID. de mensaje.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Método ConvertErrorCodeToMessageId NAP
- Método ConvertErrorCodeToMessageId NAP, interfaz INapComponentInfo
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
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492809"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a>INapComponentInfo:: ConvertErrorCodeToMessageId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: ConvertErrorCodeToMessageId** para solicitar al cliente de mantenimiento que convierta un código de error HRESULT en un identificador de mensaje.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ErrorCode* \[ de\]
</dt> <dd>

[**Código de error**](nap-error-constants.md) del sistema NAP que se va a convertir en **MessageId**.

</dd> <dt>

*msgId* \[ enuncia\]
</dt> <dd>

Un puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso de la cadena localizada correspondiente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva uno de estos códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

El sistema NAP usa el **MessageId** devuelto para recuperar una cadena traducida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





