---
title: CB_GETMINVISIBLE mensaje (Commctrl.h)
description: Obtiene el número mínimo de elementos visibles en la lista desplegable de un cuadro combinado.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- CB_GETMINVISIBLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174189"
---
# <a name="cb_getminvisible-message"></a>Mensaje \_ GETMINVISIBLE de CB

Obtiene el número mínimo de elementos visibles en la lista desplegable de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número mínimo de elementos visibles.

## <a name="remarks"></a>Observaciones

Cuando el número de elementos de la lista desplegable es mayor que el mínimo, el cuadro combinado usa una barra de desplazamiento.

Este mensaje se omite si el control de cuadro combinado tiene el estilo [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md).

Para usar **CB \_ GETMINVISIBLE,** la aplicación debe especificar comctl32.dll versión 6 en el manifiesto. Para obtener más información, vea [Habilitar estilos visuales.](cookbook-overview.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ SETMINVISIBLE**](cb-setminvisible.md)
</dt> <dt>

[**ComboBox \_ GetMinVisible**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





