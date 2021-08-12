---
title: Método SyncLocalClipboardToRemoteSession de la interfaz IMsRdpClipboard
description: Sincroniza el Portapapeles local con la sesión remota.
ms.tgt_platform: multiple
keywords:
- Método SyncLocalClipboardToRemoteSession Servicios de Escritorio remoto
- Método SyncLocalClipboardToRemoteSession Servicios de Escritorio remoto interfaz IMsRdpClipboard
- Interfaz IMsRdpClipboard Servicios de Escritorio remoto, método SyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 516782dcb86dd02b0d3fd31fee5cc463a64b0e86726c826a855e245f37ba5908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606910"
---
# <a name="imsrdpclipboardsynclocalclipboardtoremotesession-method"></a>IMsRdpClipboard::SyncLocalClipboardToRemoteSession (método)

Sincroniza el Portapapeles local con la sesión remota.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT SyncLocalClipboardToRemoteSession();
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
