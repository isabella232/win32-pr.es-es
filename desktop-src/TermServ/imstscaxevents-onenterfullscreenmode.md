---
title: Método IMsTscAxEvents OnEnterFullScreenMode
description: Se llama cuando el cliente entra en modo de pantalla completa. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de teclas de método abreviado de modo de pantalla completa (CTRL+ALT+BREAK).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- Método OnEnterFullScreenMode Servicios de Escritorio remoto
- Método OnEnterFullScreenMode Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnEnterFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnEnterFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e40da93f0e29fb183cea540b0f195d61c4969d65c2b7829bf86d8e3c8eba81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512405"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a>Método IMsTscAxEvents::OnEnterFullScreenMode

Se llama cuando el cliente entra en modo de pantalla completa. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de teclas de método abreviado de modo [de pantalla](terminal-services-shortcut-keys.md) completa (CTRL+ALT+BREAK).

## <a name="syntax"></a>Sintaxis


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





