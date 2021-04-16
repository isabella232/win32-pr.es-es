---
title: IMsTscAxEvents OnFocusReleased, método
description: Se le llama cuando se presiona la combinación de teclas de foco de versión. Por ejemplo, se llama a este evento cuando el usuario presiona las teclas CTRL + ALT + Flecha izquierda o CTRL + ALT + Flecha derecha.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Método OnFocusReleased Servicios de Escritorio remoto
- Método OnFocusReleased Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnFocusReleased
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
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686022"
---
# <a name="imstscaxeventsonfocusreleased-method"></a>IMsTscAxEvents:: OnFocusReleased (método)

Se le llama cuando se presiona la combinación de teclas de foco de versión. Por ejemplo, se llama a este evento cuando el usuario presiona las teclas CTRL + ALT + Flecha izquierda o CTRL + ALT + Flecha derecha.

Este evento permite al contenedor de controles ActiveX quitar el control del control ActiveX. Por ejemplo, esto es útil en un escenario en el que no hay un mouse, y las combinaciones de teclas especiales, como ALT + TAB, se redirigen al servidor. En este caso, no tiene una manera de devolver el foco de teclado al escritorio local. Sin embargo, con la combinación de teclas CTRL + ALT + Flecha izquierda o CTRL + ALT + Flecha derecha, el contenedor ActiveX puede realizar escuchas para este evento y responder tomando el foco fuera del control ActiveX.

## <a name="syntax"></a>Sintaxis


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iDirection* \[ de\]
</dt> <dd>

El parámetro Direction de 1 (CTRL + ALT + Flecha derecha) o 1 (CTRL + ALT + Flecha izquierda).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este evento está disponible cuando se utiliza Conexión a Escritorio remoto 6,0 en el cliente.

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

 

 





