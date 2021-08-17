---
description: Obtiene la dirección del punto de conexión de un motor remoto.
MS-HAID: vspixengine.IPeerToPeerEngine\_GetPlaybackEndpoint\_BOOL\_BSTR\_ptr\_BSTR\_ptr\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPeerToPeerEngine::GetPlaybackEndpoint (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3B391048-E7F7-4DA7-96A3-05875B170DCA
api_name:
- IPeerToPeerEngine.GetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6b8d099762da58cefaaa208026c9b60fc5103f4e6b2551ba679da83a76f2f8bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094795"
---
# <a name="span-idvspixengineipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptrspanipeertopeerenginegetplaybackendpoint-method"></a><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine::GetPlaybackEndpoint (método)

Obtiene la dirección del punto de conexión de un motor remoto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPlaybackEndpoint(
   BOOL              bUseAuthentication,
   BSTR *            pEndpoint,
   BSTR *            sessionKey,
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a>Parámetros

*bUseAuthentication*   
true si el motor remoto usa la autenticación; de lo contrario, false.

*pEndpoint*   
En la devolución, una cadena COM que contiene la dirección del punto de conexión de la máquina de reproducción remota.

*sessionKey*   
En la devolución, una cadena COM que contiene la clave de sesión usada para el cifrado.

*pRemoteVersion*   
En la devolución, la versión del motor remoto.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPeerToPeerEngine**](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
