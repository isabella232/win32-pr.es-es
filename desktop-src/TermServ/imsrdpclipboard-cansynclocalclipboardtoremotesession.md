---
title: Método CanSyncLocalClipboardToRemoteSession de la interfaz IMsRdpClipboard
description: Indica si el Portapapeles local se puede sincronizar con la sesión remota.
ms.tgt_platform: multiple
keywords:
- Método CanSyncLocalClipboardToRemoteSession Servicios de Escritorio remoto
- Método CanSyncLocalClipboardToRemoteSession Servicios de Escritorio remoto, interfaz IMsRdpClipboard
- Interfaz IMsRdpClipboard Servicios de Escritorio remoto, método CanSyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: dabc12064ff43a2bb64a562d1aa3050681f46c31dd2698154beb1dafe3cfd85e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606920"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a>Método IMsRdpClipboard::CanSyncLocalClipboardToRemoteSession

Indica si el Portapapeles local se puede sincronizar con la sesión remota.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parámetros

**TRUE** si el Portapapeles local se puede sincronizar con la sesión remota; de lo contrario, **FALSE**.

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID IMsRdpClipboard se define como \_ 2E769EE8-00C7-43DC-AFD9-235D75B72A40          |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>