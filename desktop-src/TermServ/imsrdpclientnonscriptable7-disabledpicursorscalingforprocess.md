---
title: Método DisableDpiCursorScalingForProcess de la interfaz IMsRdpClientNonScriptable7
description: Deshabilita el escalado local del cursor del mouse recibido del servidor, lo que garantiza que la forma del cursor se represente correctamente sin modificaciones.
ms.tgt_platform: multiple
keywords:
- Método DisableDpiCursorScalingForProcess Servicios de Escritorio remoto
- Interfaz DisableDpiCursorScalingForProcess Servicios de Escritorio remoto, IMsRdpClientNonScriptable7
- Interfaz IMsRdpClientNonScriptable7 Servicios de Escritorio remoto, método DisableDpiCursorScalingForProcess
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.DisableDpiCursorScalingForProcess
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b054e75edd9ae8d012d117a603cac9679c28c81b555f63d7390a17b7022157e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854876"
---
# <a name="imsrdpclientnonscriptable7disabledpicursorscalingforprocess-method"></a>IMsRdpClientNonScriptable7::D isableDpiCursorScalingForProcess

Deshabilita el escalado local del cursor del mouse recibido del servidor, lo que garantiza que la forma del cursor se represente correctamente sin modificaciones.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT DisableDpiCursorScalingForProcess();
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
| IID                      | IID \_ IMsRdpClientNonScriptable7 se define como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>
