---
title: Propiedad Clipboard de la interfaz IMsRdpClientNonScriptable7
description: Obtiene el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles.
ms.tgt_platform: multiple
keywords:
- Propiedad Clipboard Servicios de Escritorio remoto
- Propiedad Clipboard Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable7, propiedad Clipboard
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "103997613"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a>IMsRdpClientNonScriptable7:: Clipboard (propiedad)

Obtiene el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a>Valor de propiedad

Un [IMsRdpClipboard](imsrdpclipboard.md) que representa el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles (es decir, el valor de la propiedad [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) se establece en **true**).

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 se define como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>