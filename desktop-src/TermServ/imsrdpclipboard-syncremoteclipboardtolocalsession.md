---
title: Método SyncRemoteClipboardToLocalSession de la interfaz IMsRdpClipboard
description: Sincroniza el Portapapeles remoto con la sesión local.
ms.tgt_platform: multiple
keywords:
- Método SyncRemoteClipboardToLocalSession Servicios de Escritorio remoto
- Método SyncRemoteClipboardToLocalSession Servicios de Escritorio remoto, interfaz IMsRdpClipboard
- Interfaz IMsRdpClipboard Servicios de Escritorio remoto, método SyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e1e56a67504ab3182ed6ccaba97591e8259d6e46b6ebdd3bdc06fbaf63c170f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000825"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a>Método IMsRdpClipboard::SyncRemoteClipboardToLocalSession

Sincroniza el Portapapeles remoto con la sesión local.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT SyncRemoteClipboardToLocalSession();
```

## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

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