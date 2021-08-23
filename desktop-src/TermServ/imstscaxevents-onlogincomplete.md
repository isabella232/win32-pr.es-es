---
title: Método IMsTscAxEvents OnLoginComplete
description: Se llama cuando el control de cliente ha iniciado sesión correctamente en un servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto), después de la presentación del cuadro de diálogo Windows inicio de sesión.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Método OnLoginComplete Servicios de Escritorio remoto
- Método OnLoginComplete Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnLoginComplete
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6c89b494a250652e054e245eb0de3267a860bec1a193c7dc953f93fd0800c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138438"
---
# <a name="imstscaxeventsonlogincomplete-method"></a>IMsTscAxEvents::OnLoginComplete (método)

Se llama cuando el control de cliente ha iniciado sesión correctamente en un servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto), después de la presentación del cuadro de diálogo Windows inicio de sesión.

## <a name="syntax"></a>Sintaxis


```C++
void OnLoginComplete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Implemente este método en el receptor de eventos para recibir la notificación de que el control ha completado el inicio de sesión.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo controlar este evento mediante Visual Basic código de scripting. La suposición en este ejemplo es que el objeto de control se denomina "MsRdpClient".

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
End sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





