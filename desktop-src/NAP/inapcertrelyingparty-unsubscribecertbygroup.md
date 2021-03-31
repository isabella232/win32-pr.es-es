---
title: Método INapCertRelyingParty UnSubscribeCertByGroup (NapCertRelyingParty. h)
description: Cancela la suscripción de un servidor de certificados de mantenimiento (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Método UnSubscribeCertByGroup NAP
- Método UnSubscribeCertByGroup NAP, interfaz INapCertRelyingParty
- Interfaz INapCertRelyingParty NAP, método UnSubscribeCertByGroup
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
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996534"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a>INapCertRelyingParty:: UnSubscribeCertByGroup (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **UnSubscribeCertByGroup** cancela la suscripción de un servidor de certificados de mantenimiento (HCS).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

 *ID.* \[ en\]
</dt> <dd>

Un [**EnforcementEntityId**](nap-datatypes.md) que contiene el identificador del cliente de cumplimiento que se va a cancelar.

</dd> <dt>

 *reservado* \[ de\]
</dt> <dd>

Debe ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Si no hay ningún otro suscriptor al HCS, el NapAgent eliminará los certificados de mantenimiento correspondientes del almacén del equipo local.

Antes de llamar a este método, llame a [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).

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

 

 





