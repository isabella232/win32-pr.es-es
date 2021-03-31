---
title: Mensaje de CB_SETMINVISIBLE (commctrl. h)
description: Una aplicación envía un \_ mensaje CB SETMINVISIBLE para establecer el número mínimo de elementos visibles en la lista desplegable de un cuadro combinado.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- CB_SETMINVISIBLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac88155424c0b1ecf6c91f398e7a9a2d437eff90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149946"
---
# <a name="cb_setminvisible-message"></a>\_Mensaje SETMINVISIBLE CB

Una aplicación envía un mensaje **CB \_ SETMINVISIBLE** para establecer el número mínimo de elementos visibles en la lista desplegable de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el número mínimo de elementos visibles.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es **true**. De lo contrario, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Cuando el número de elementos de la lista desplegable es mayor que el mínimo, el cuadro combinado usa una barra de desplazamiento. De forma predeterminada, 30 es el número mínimo de elementos visibles.

Este mensaje se omite si el control de cuadro combinado tiene el estilo [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md).

Para usar **CB \_ SETMINVISIBLE**, la aplicación debe especificar comctl32.dll versión 6 del manifiesto. Para obtener más información, vea [habilitar estilos visuales](cookbook-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ GETMINVISIBLE**](cb-getminvisible.md)
</dt> <dt>

[**ComboBox \_ SetMinVisible**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





