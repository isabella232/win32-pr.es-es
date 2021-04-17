---
description: Desusado. El PenInputPanel se ha reemplazado por el panel de entrada de texto (TIP). Se produce cuando se mueve el objeto PenInputPanel.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Evento PenInputPanel. PanelMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697817"
---
# <a name="peninputpanelpanelmoving-event"></a>Evento PenInputPanel. PanelMoving

En desuso. El [**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por el [Panel de entrada de texto (TIP)](text-input-panel-reference.md).

Se produce cuando se mueve el objeto [**PenInputPanel**](peninputpanel-class.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Izquierda* \[ in, out\]
</dt> <dd>

La nueva posición horizontal, o eje x, del borde izquierdo del objeto [**PenInputPanel**](peninputpanel-class.md) , en coordenadas de la pantalla.

</dd> <dt>

*Parte superior* \[ in, out\]
</dt> <dd>

Nuevo eje vertical, o y, posición del borde izquierdo del objeto [**PenInputPanel**](peninputpanel-class.md) , en coordenadas de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El evento **PanelMoving** está diseñado para cambiar la posición del panel de entrada del lápiz cambiando los parámetros *izquierdo* y *superior* .

Los métodos [**moveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) y [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) hacen que el objeto [**PenInputPanel**](peninputpanel-class.md) llame a su código de posicionamiento automático que desencadena un evento **PanelMoving** . Por consiguiente, llamar a estos métodos dentro de un controlador **PanelMoving** puede producir un bucle infinito recursivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




