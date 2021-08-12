---
title: Interfaz IMsRdpClipboard
description: Representa el controlador del Portapapeles que se usa para sincronizar los Portapapeles locales y remotos si está habilitada la sincronización manual del Portapapeles.
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClipboard Servicios de Escritorio remoto
- Interfaz IMsRdpClipboard Servicios de Escritorio remoto, descrito
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
ms.openlocfilehash: a1ffc9a503365337676a11ccbdb872c1c7c7bed24eeb108fe1d565ced4de41d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606882"
---
# <a name="imsrdpclipboard-interface"></a>Interfaz IMsRdpClipboard

Representa el controlador del Portapapeles que se usa para sincronizar los Portapapeles locales y remotos si está habilitada la sincronización manual del Portapapeles (es decir, el valor de la propiedad [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) se establece en **True).**

## <a name="members"></a>Miembros

La **interfaz IMsRdpClipboard** hereda de **IUnknown.** **IMsRdpClipboard** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpClipboard tiene** estos métodos.


| Método        | Descripción      |
|:---------------|:----------------|
| [**CanSyncLocalClipboardToRemoteSession**](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  Indica si el Portapapeles local se puede sincronizar con la sesión remota.                   |
| [**CanSyncRemoteClipboardToLocalSession**](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  Indica si el Portapapeles remoto se puede sincronizar con la sesión local.                   |
| [**SyncLocalClipboardToRemoteSession**](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  Sincroniza el Portapapeles local con la sesión remota.                   |
| [**SyncRemoteClipboardToLocalSession**](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   Sincroniza el Portapapeles remoto con la sesión local.                      |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID IMsRdpClipboard se define como \_ 2E769EE8-00C7-43DC-AFD9-235D75B72A40            |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable7::Clipboard**](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
