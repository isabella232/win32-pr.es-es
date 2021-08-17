---
title: Método INapCertRelyingParty UnSubscribeCertByGroup (NapCertRelyingParty.h)
description: Cancela la suscripción a un servidor de certificados de mantenimiento (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Método NAP UnSubscribeCertByGroup
- Método UNSubscribeCertByGroup NAP, interfaz INapCertRelyingParty
- INapCertRelyingParty interface NAP , UnSubscribeCertByGroup (método)
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d8b9f5398ba63c0e6108adfefd51d0546180db4536dbd95615e5b15dddde523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940223"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a>INapCertRelyingParty::UnSubscribeCertByGroup (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método UnSubscribeCertByGroup** cancela la suscripción de un servidor de certificados de mantenimiento (HCS).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

 *id* \[ en\]
</dt> <dd>

[**EnforcementEntityId que**](nap-datatypes.md) contiene el identificador del cliente de cumplimiento que no se está suscribiendo.

</dd> <dt>

 *reservado* \[ En\]
</dt> <dd>

Debe ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

Si no hay ningún otro suscriptor a HCS, NapAgent eliminará los certificados de mantenimiento correspondientes del almacén de la máquina local.

Antes de llamar a este método, llame [**a SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapCertRelyingParty.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCertRelyingParty.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





