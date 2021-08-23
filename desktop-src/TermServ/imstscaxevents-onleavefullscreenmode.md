---
title: Método IMsTscAxEvents OnLeaveFullScreenMode
description: Se llama cuando el cliente sale del modo de pantalla completa. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de teclas de método abreviado de modo de pantalla completa (CTRL+ALT+BREAK).
ms.assetid: 95c5d427-b6e2-4a42-9816-b130ab533ac0
ms.tgt_platform: multiple
keywords:
- Método OnLeaveFullScreenMode Servicios de Escritorio remoto
- Método OnLeaveFullScreenMode Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnLeaveFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLeaveFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efacca782d771337ffe3419bd9820be268cacc1ae6f7d33f04a4bb8127079c7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138448"
---
# <a name="imstscaxeventsonleavefullscreenmode-method"></a>Método IMsTscAxEvents::OnLeaveFullScreenMode

Se llama cuando el cliente sale del modo de pantalla completa. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de teclas de método abreviado de modo [de pantalla](terminal-services-shortcut-keys.md) completa (CTRL+ALT+BREAK).

## <a name="syntax"></a>Sintaxis


```C++
void OnLeaveFullScreenMode();
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





