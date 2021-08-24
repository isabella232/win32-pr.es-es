---
description: Desusado. PenInputPanel se ha reemplazado por el Panel de entrada de texto (TIP). Se produce cuando se mueve el objeto PenInputPanel.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Evento PenInputPanel.PanelMoving (Mspanel.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4a152afdef9fcd10fb92fdec55d9a460faf58ca91536e96c9876203fbad44c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596614"
---
# <a name="peninputpanelpanelmoving-event"></a>PenInputPanel.PanelMoving, evento

En desuso. [**PenInputPanel se**](peninputpanel-class.md) ha reemplazado por el [Panel de entrada de texto (TIP).](text-input-panel-reference.md)

Se produce cuando se [**mueve el objeto PenInputPanel.**](peninputpanel-class.md)

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

Nueva posición horizontal, o eje X, del borde izquierdo del [**objeto PenInputPanel,**](peninputpanel-class.md) en coordenadas de pantalla.

</dd> <dt>

*Parte superior* \[ in, out\]
</dt> <dd>

Nueva posición vertical, o eje Y, del borde izquierdo del [**objeto PenInputPanel,**](peninputpanel-class.md) en coordenadas de pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El **evento PanelMoving** está diseñado para usarse para cambiar la posición del panel de entrada del lápiz cambiando los parámetros *Left* *y Top.*

Los [**métodos MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) y [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) hacen que el [**objeto PenInputPanel**](peninputpanel-class.md) llame a su código de posicionamiento automático que desencadena **un evento PanelMoving.** Por lo tanto, llamar a estos métodos dentro **de un controlador PanelMoving** puede dar lugar a un bucle sin fin recursivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




