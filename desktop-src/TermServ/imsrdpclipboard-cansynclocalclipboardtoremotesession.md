---
title: Método CanSyncLocalClipboardToRemoteSession de la interfaz IMsRdpClipboard
description: Indica si el portapapeles local se puede sincronizar con la sesión remota.
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
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "105720240"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a>IMsRdpClipboard:: CanSyncLocalClipboardToRemoteSession (método)

Indica si el portapapeles local se puede sincronizar con la sesión remota.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parámetros

**True** si el portapapeles local se puede sincronizar con la sesión remota; en caso contrario, **false**.

## <a name="return-value"></a>Valor devuelto

Vuelva **a \_ Aceptar si es** correcto.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard se define como 2E769EE8-00C7-43DC-AFD9-235D75B72A40          |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>