---
title: Método IMsTscAxEvents OnFocusReleased
description: Se llama cuando se presiona la combinación de teclas de enfoque de liberación. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de teclas CTRL+ALT+FLECHA IZQUIERDA o CTRL+ALT+FLECHA DERECHA.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Método OnFocusReleased Servicios de Escritorio remoto
- Método OnFocusReleased Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnFocusReleased
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673916c3a538f21ceea5b0b7578bb9e8f225ec2a349e38015eab0b50d73935aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512345"
---
# <a name="imstscaxeventsonfocusreleased-method"></a>IMsTscAxEvents::OnFocusReleased (método)

Se llama cuando se presiona la combinación de teclas de enfoque de liberación. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de teclas CTRL+ALT+FLECHA IZQUIERDA o CTRL+ALT+FLECHA DERECHA.

Este evento permite que ActiveX contenedor de controles de control de descontrole el control ActiveX control. Por ejemplo, esto es útil en un escenario en el que no tiene un mouse y las combinaciones de teclas especiales, como ALT+TAB, se redirigen al servidor. En este caso, no tiene ninguna manera de devolver el foco del teclado al escritorio local. Sin embargo, con la combinación de teclas CTRL+ALT+FLECHA IZQUIERDA o CTRL+ALT+FLECHA DERECHA, el contenedor ActiveX puede escuchar este evento y responder quitando el foco del control ActiveX.

## <a name="syntax"></a>Sintaxis


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iDirection* \[ En\]
</dt> <dd>

Parámetro de dirección de 1 (CTRL+ALT+FLECHA DERECHA) o 1 (CTRL+ALT+FLECHA IZQUIERDA).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este evento está disponible cuando Conexión a Escritorio remoto 6.0 se usa en el cliente.

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

 

 





