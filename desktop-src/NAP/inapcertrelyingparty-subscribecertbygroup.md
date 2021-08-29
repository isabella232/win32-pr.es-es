---
title: Método INapCertRelyingParty SubscribeCertByGroup (NapCertRelyingParty.h)
description: Se suscribe a un servidor de certificados de estado (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- Método NAP SubscribeCertByGroup
- Método NAP subscribeCertByGroup, interfaz INapCertRelyingParty
- INapCertRelyingParty interface NAP , SubscribeCertByGroup (método)
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a8ed7f7dd97bf77e99e493a7c0521c62fcbcaaa776a364d0fe7e322e056de5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891455"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a>INapCertRelyingParty::SubscribeCertByGroup (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método SubscribeCertByGroup** se suscribe a un servidor de certificados de mantenimiento (HCS). El HCS ya debe estar registrado antes de suscribirse.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

 *id* \[ en\]
</dt> <dd>

[**EnforcementEntityId que**](nap-datatypes.md) contiene el identificador del cliente de cumplimiento que se está suscribiendo.

</dd> <dt>

*subscriberName* \[ En\]
</dt> <dd>

El nombre del suscriptor.

> [!Note]  
> Actualmente solo se usa con fines de registro.

 

</dd> <dt>

*reservado* \[ En\]
</dt> <dd>

Debe ser **NULL.**

</dd> <dt>

*certExists* \[ out\]
</dt> <dd>

Indica si napAgent ya mantiene un certificado de mantenimiento de este HCS y está presente en el almacén de la máquina. Si **es TRUE,** ya se está conservando un certificado de mantenimiento y está presente. Si **es FALSE,** un certificado de mantenimiento no se mantiene y está presente actualmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

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

 

 





