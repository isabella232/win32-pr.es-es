---
title: Método INapCertRelyingParty SubscribeCertByGroup (NapCertRelyingParty. h)
description: Se suscribe a un servidor de certificados de mantenimiento (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- Método SubscribeCertByGroup NAP
- Método SubscribeCertByGroup NAP, interfaz INapCertRelyingParty
- Interfaz INapCertRelyingParty NAP, método SubscribeCertByGroup
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
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651402"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a>INapCertRelyingParty:: SubscribeCertByGroup (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **SubscribeCertByGroup** se suscribe a un servidor de certificados de mantenimiento (HCS). El HCS ya debe estar registrado antes de suscribirse.

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

 *ID.* \[ en\]
</dt> <dd>

Un [**EnforcementEntityId**](nap-datatypes.md) que contiene el identificador del cliente de cumplimiento que se suscribe.

</dd> <dt>

*subscriberName* \[ de\]
</dt> <dd>

El nombre del suscriptor.

> [!Note]  
> Actualmente, esto solo se usa para fines de registro.

 

</dd> <dt>

*reservado* \[ de\]
</dt> <dd>

Debe ser **null**.

</dd> <dt>

*certExists* \[ enuncia\]
</dt> <dd>

Indica si el NapAgent ya mantiene un certificado de mantenimiento de este HCS y está presente en el almacén del equipo. Si es **true**, ya se está manteniendo un certificado de mantenimiento y está presente. Si es **false**, no se mantiene actualmente un certificado de mantenimiento y está presente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>NapCertRelyingParty. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCertRelyingParty. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





