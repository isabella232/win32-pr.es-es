---
title: IMsTscAxEvents OnRemoteProgramDisplayed, método
description: Se le llama cuando se muestra un programa RemoteApp.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- Método OnRemoteProgramDisplayed Servicios de Escritorio remoto
- Método OnRemoteProgramDisplayed Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRemoteProgramDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802732"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a>IMsTscAxEvents:: OnRemoteProgramDisplayed (método)

Se le llama cuando se muestra un programa RemoteApp.

## <a name="syntax"></a>Sintaxis


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vbDisplayed* \[ de\]
</dt> <dd>

Indica si se muestra u oculta el programa RemoteApp.

</dd> <dt>

*uDisplayInformation* \[ de\]
</dt> <dd>

Información de presentación.

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAÍL \_ APPDISPLAY \_ reconexión automática**


</dt> <dd>

La reconexión automática está en curso.

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAÍL \_ APPDISPLAY \_ DESKTOPHOOKED**


</dt> <dd>

El número de RemoteApp llegó a cero.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Implemente este método en el receptor de eventos para recibir la notificación de que se ha mostrado una RemoteApp.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



 

 





