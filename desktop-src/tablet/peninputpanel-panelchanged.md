---
description: Desusado. PenInputPanel se ha reemplazado por el Panel de entrada de texto (TIP). Se produce cuando el objeto PenInputPanel cambia entre diseños.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Evento PenInputPanel.PanelChanged (Msalterut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361021"
---
# <a name="peninputpanelpanelchanged-event"></a>PenInputPanel.PanelChanged, evento

En desuso. [**PenInputPanel se**](peninputpanel-class.md) ha reemplazado por el [Panel de entrada de texto (TIP).](text-input-panel-reference.md)

Se produce cuando el [**objeto PenInputPanel**](peninputpanel-class.md) cambia entre diseños.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewPanelType* \[ En\]
</dt> <dd>

El nuevo tipo de panel usado para la entrada dentro [**del objeto PenInputPanel,**](peninputpanel-class.md) después de que se des activara el evento **PanelChanged.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Al crear un [**objeto PenInputPanel,**](peninputpanel-class.md) [**handwriting**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) es el **valor predeterminado de PanelType.** Si cambia el panel estableciendo la propiedad [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) antes de que el panel de entrada de lápiz se active por primera vez, **se produce un evento PanelChanged.**

El **evento PanelChanged** no se genera cuando el usuario cambia entre los paneles de escritura con formato y boxed.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 
