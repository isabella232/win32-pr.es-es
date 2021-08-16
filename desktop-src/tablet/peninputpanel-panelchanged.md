---
description: Desusado. PenInputPanel se ha reemplazado por el Panel de entrada de texto (TIP). Se produce cuando el objeto PenInputPanel cambia entre diseños.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Evento PenInputPanel.PanelChanged (Msalterut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f722609ae71761a2a2a05c743aba7bfd83b7d4ff8689333bf2093d4dc21345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856524"
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

## <a name="remarks"></a>Comentarios

Al crear un [**objeto PenInputPanel,**](peninputpanel-class.md) [**handwriting**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) es el **valor predeterminado de PanelType.** Si cambia el panel estableciendo la propiedad [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) antes de que el panel de entrada de lápiz se active por primera vez, **se produce un evento PanelChanged.**

El **evento PanelChanged** no se genera cuando el usuario cambia entre los paneles de escritura con formato y boxed.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 
