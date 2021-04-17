---
description: Desusado. El PenInputPanel se ha reemplazado por el panel de entrada de texto (TIP). Se produce cuando el objeto PenInputPanel se ha mostrado u oculto.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Evento PenInputPanel. VisibleChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697816"
---
# <a name="peninputpanelvisiblechanged-event"></a>Evento PenInputPanel. VisibleChanged

En desuso. El [**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por el [Panel de entrada de texto (TIP)](text-input-panel-reference.md).

Se produce cuando el objeto [**PenInputPanel**](peninputpanel-class.md) se ha mostrado u oculto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewVisibility* \[ de\]
</dt> <dd>

**Variante \_ TRUE** para hacer que el objeto [**PenInputPanel**](peninputpanel-class.md) se convierta en visible; de lo contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El evento **VisibleChanged** se aplica al destino de mantener el mouse del panel de entrada de Tablet PC. Sin embargo, no se genera cuando el destino de mantener el mouse se expande para mostrar el panel de entrada completo de Tablet PC.

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

 

 




