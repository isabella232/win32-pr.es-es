---
title: Propiedad Clipboard de la interfaz IMsRdpClientNonScriptable7
description: Obtiene el controlador del Portapapeles que se usa para sincronizar los Portapapeles locales y remotos si está habilitada la sincronización manual del Portapapeles.
ms.tgt_platform: multiple
keywords:
- Propiedades del Portapapeles Servicios de Escritorio remoto
- Propiedad clipboard Servicios de Escritorio remoto interfaz , IMsRdpClientNonScriptable7
- Interfaz IMsRdpClientNonScriptable7 Servicios de Escritorio remoto propiedad , Clipboard
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
ms.openlocfilehash: 236666cbef369c4f2353ff524ceb7544e62f50d4a7e4a7ac59f3882057a92f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009645"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a>IMsRdpClientNonScriptable7::Clipboard, propiedad

Obtiene el controlador del Portapapeles que se usa para sincronizar los Portapapeles locales y remotos si está habilitada la sincronización manual del Portapapeles.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a>Valor de propiedad

[IMsRdpClipboard](imsrdpclipboard.md) que representa el controlador del Portapapeles que se usa para sincronizar los Portapapeles locales y remotos si está habilitada la sincronización manual del Portapapeles (es decir, el valor de la propiedad [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) se establece en **True).**

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