---
description: Establece la dirección del punto de conexión utilizada para conectarse a un motor remoto.
MS-HAID: vspixengine.IPeerToPeerEngine\_SetPlaybackEndpoint\_BOOL\_BSTR\_BSTR\_RemotingVersion
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPeerToPeerEngine::SetPlaybackEndpoint (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D261D2EA-C930-406E-A5E1-CE5E98162399
api_name:
- IPeerToPeerEngine.SetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 68a52342f3494b831439764eb74cd16132ec770e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622941"
---
# <a name="span-idvspixengineipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversionspanipeertopeerenginesetplaybackendpoint-method"></a><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>IPeerToPeerEngine::SetPlaybackEndpoint (método)

Establece la dirección del punto de conexión utilizada para conectarse a un motor remoto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPlaybackEndpoint(
   BOOL            bUseAuthentication,
   BSTR            endpoint,
   BSTR            sessionKey,
   RemotingVersion remoteVersion
);
```

## <a name="parameters"></a>Parámetros

*bUseAuthentication*   
true para usar la autenticación; de lo contrario, false.

*Extremo*   
Cadena COM que contiene la dirección del punto de conexión.

*sessionKey*   
Cadena COM que contiene la clave de sesión utilizada para el cifrado.

*remoteVersion*   
Especifica la versión del motor remoto que se usará.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPeerToPeerEngine**](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
