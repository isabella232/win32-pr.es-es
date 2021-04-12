---
title: Método INapCertRelyingParty GetSubscribedRelyingParties (NapCertRelyingParty. h)
description: Obtiene una lista de usuarios de confianza que se han suscrito.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- Método GetSubscribedRelyingParties NAP
- Método GetSubscribedRelyingParties NAP, interfaz INapCertRelyingParty
- Interfaz INapCertRelyingParty NAP, método GetSubscribedRelyingParties
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489382"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a>INapCertRelyingParty:: GetSubscribedRelyingParties (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **GetSubscribedRelyingParties** obtiene una lista de usuarios de confianza que se han suscrito.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*recuento* \[ enuncia\]
</dt> <dd>

Un puntero a un [**EnforcementEntityCount**](nap-datatypes.md) que contiene el número de usuarios de confianza suscritos.

</dd> <dt>

*relyingParties* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a un [**EnforcementEntityId**](nap-datatypes.md) que contiene la lista de usuarios de confianza suscritos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

El autor de la llamada debe liberar el parámetro *relyingParties* mediante **CoTaskMemFree**.

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

 

 





