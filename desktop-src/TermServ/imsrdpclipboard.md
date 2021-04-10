---
title: Interfaz IMsRdpClipboard
description: Representa el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClipboard
- Servicios de Escritorio remoto de la interfaz IMsRdpClipboard, descrito
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104151929"
---
# <a name="imsrdpclipboard-interface"></a>Interfaz IMsRdpClipboard

Representa el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles (es decir, el valor de la propiedad [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) se establece en **true**).

## <a name="members"></a>Miembros

La interfaz **IMsRdpClipboard** hereda de **IUnknown**. **IMsRdpClipboard** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMsRdpClipboard** tiene estos métodos.


| Método        | Descripción      |
|:---------------|:----------------|
| [**CanSyncLocalClipboardToRemoteSession**](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  Indica si el portapapeles local se puede sincronizar con la sesión remota.                   |
| [**CanSyncRemoteClipboardToLocalSession**](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  Indica si el portapapeles remoto se puede sincronizar con la sesión local.                   |
| [**SyncLocalClipboardToRemoteSession**](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  Sincroniza el portapapeles local con la sesión remota.                   |
| [**SyncRemoteClipboardToLocalSession**](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   Sincroniza el portapapeles remoto con la sesión local.                      |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard se define como 2E769EE8-00C7-43DC-AFD9-235D75B72A40            |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable7:: Clipboard**](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
