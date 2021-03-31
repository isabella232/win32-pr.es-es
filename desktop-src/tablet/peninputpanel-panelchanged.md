---
description: Desusado. El PenInputPanel se ha reemplazado por el panel de entrada de texto (TIP). Se produce cuando cambia el objeto PenInputPanel entre diseños.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Evento PenInputPanel. PanelChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361173"
---
# <a name="peninputpanelpanelchanged-event"></a>Evento PenInputPanel. PanelChanged

En desuso. El [**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por el [Panel de entrada de texto (TIP)](text-input-panel-reference.md).

Se produce cuando cambia el objeto [**PenInputPanel**](peninputpanel-class.md) entre diseños.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewPanelType* \[ de\]
</dt> <dd>

El nuevo tipo de panel que se usa para la entrada dentro del objeto [**PenInputPanel**](peninputpanel-class.md) , después de que se desencadene el evento **PanelChanged** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Al crear un objeto [**PenInputPanel**](peninputpanel-class.md) , la [**escritura a mano**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) es el valor predeterminado de **PanelType**. Si cambia el panel estableciendo la propiedad [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) antes de que el panel de entrada del lápiz se active por primera vez, se produce un evento **PanelChanged** .

El evento **PanelChanged** no se genera cuando el usuario cambia entre los paneles de escritura con líneas y con conversión boxing.

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

 

 
