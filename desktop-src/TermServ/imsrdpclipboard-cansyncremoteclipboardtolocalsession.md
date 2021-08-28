---
title: Método CanSyncRemoteClipboardToLocalSession de la interfaz IMsRdpClipboard
description: Indica si el Portapapeles remoto se puede sincronizar con la sesión local.
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
ms.openlocfilehash: 40a9fc5d6dcdc2e96d9ce916bce0567cccc90adf10fcacc5d797f61ed292c116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000845"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>Método IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession

Indica si el Portapapeles remoto se puede sincronizar con la sesión local.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parámetros

**TRUE** si el Portapapeles remoto se puede sincronizar con la sesión local; de lo contrario, **FALSE**.

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