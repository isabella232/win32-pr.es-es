---
title: Método INapCertRelyingParty GetSubscribedRelyingParties (NapCertRelyingParty.h)
description: Obtiene una lista de usuarios de confianza que se han suscrito.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- Método NAP getSubscribedRelyingParties
- Método NAP de GetSubscribedRelyingParties , interfaz INapCertRelyingParty
- INapCertRelyingParty interface NAP , GetSubscribedRelyingParties (método)
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
ms.openlocfilehash: 4e9d94fd0816e9e8b3e89ba4001b30d83617276938c683f8f0efb6fd17530cb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891454"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a>Método INapCertRelyingParty::GetSubscribedRelyingParties

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método GetSubscribedRelyingParties obtiene** una lista de usuarios de confianza que se han suscrito.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Puntero a [**enforcementEntityCount que**](nap-datatypes.md) contiene el número de usuarios de confianza suscritos.

</dd> <dt>

*relyingParties* \[ out\]
</dt> <dd>

Puntero a un puntero a [**enforcementEntityId**](nap-datatypes.md) que contiene la lista de usuarios de confianza suscritos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error según el resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

El autor de la llamada debe liberar *el parámetro relyingParties* **mediante CoTaskMemFree.**

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

 

 





