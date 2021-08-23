---
description: Desusado. PenInputPanel se ha reemplazado por el Panel de entrada de texto (TIP). Se produce cuando el objeto PenInputPanel se muestra u se oculta a sí mismo.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Evento PenInputPanel.VisibleChanged (Msalterut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc917f34c09ef0d4f079fd55e476bbbc4cea266e1b1c436a62b20d6c08ed1b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596619"
---
# <a name="peninputpanelvisiblechanged-event"></a>PenInputPanel.VisibleChanged, evento

En desuso. [**PenInputPanel se**](peninputpanel-class.md) ha reemplazado por el [Panel de entrada de texto (TIP).](text-input-panel-reference.md)

Se produce cuando el [**objeto PenInputPanel**](peninputpanel-class.md) se muestra u se oculta a sí mismo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewVisibility* \[ En\]
</dt> <dd>

**VARIANT \_ TRUE** para hacer que [**el objeto PenInputPanel**](peninputpanel-class.md) se vuelva visible; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El **evento VisibleChanged** se aplica al destino del puntero del panel de entrada de Tablet PC. Sin embargo, no se genera cuando el destino del mouse se expande para mostrar el panel de entrada completo de Tablet PC.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




