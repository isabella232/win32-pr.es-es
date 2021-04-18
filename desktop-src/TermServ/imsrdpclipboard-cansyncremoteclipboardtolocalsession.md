---
title: Método CanSyncRemoteClipboardToLocalSession de la interfaz IMsRdpClipboard
description: Indica si el portapapeles remoto se puede sincronizar con la sesión local.
ms.tgt_platform: multiple
keywords:
- Método CanSyncRemoteClipboardToLocalSession Servicios de Escritorio remoto
- Método CanSyncRemoteClipboardToLocalSession Servicios de Escritorio remoto, interfaz IMsRdpClipboard
- Interfaz IMsRdpClipboard Servicios de Escritorio remoto, método CanSyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "105720253"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>IMsRdpClipboard:: CanSyncRemoteClipboardToLocalSession (método)

Indica si el portapapeles remoto se puede sincronizar con la sesión local.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parámetros

**True** si el portapapeles remoto se puede sincronizar con la sesión local; en caso contrario, **false**.

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