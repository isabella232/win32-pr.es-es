---
title: IMsTscAxEvents OnReceivedTSPublicKey, método
description: Se llama durante la secuencia de conexión cuando el cliente recupera la clave pública del servidor. Solo se llama a este evento si la propiedad NotifyTSPublicKey es VARIANT \_ true.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Método OnReceivedTSPublicKey Servicios de Escritorio remoto
- Método OnReceivedTSPublicKey Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnReceivedTSPublicKey
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491326"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a>IMsTscAxEvents:: OnReceivedTSPublicKey (método)

Se llama durante la secuencia de conexión cuando el cliente recupera la clave pública del servidor. Solo se llama a este evento si la propiedad **NotifyTSPublicKey** es **Variant \_ true**. Esto es después de la [**conexión**](imstscaxevents-onconnecting.md), pero antes de [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) y de la [**conexión**](imstscaxevents-onconnected.md).

## <a name="syntax"></a>Sintaxis


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*publicKey* \[ de\]
</dt> <dd>

Contiene la clave pública del equipo remoto.

</dd> <dt>

*pfContinueLogon* \[ enuncia\]
</dt> <dd>

Un puntero a una variable de **tipo \_ bool** que recibe si el proceso de inicio de sesión debe continuar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2008 con SP1<br/>                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





