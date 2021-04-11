---
title: Mensaje de CB_SHOWDROPDOWN (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SHOWDROPDOWN para mostrar u ocultar el cuadro de lista de un cuadro combinado que tenga el \_ estilo desplegable CBS o CBS \_ DROPDOWNLIST.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150927"
---
# <a name="cb_showdropdown-message"></a>\_Mensaje SHOWDROPDOWN CB

Una aplicación envía un mensaje **CB \_ SHOWDROPDOWN** para mostrar u ocultar el cuadro de lista de un cuadro combinado que tenga el estilo [**\_ desplegable CBS**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un **booleano** que especifica si se va a mostrar u ocultar el cuadro de lista desplegable. Un valor de **true** muestra el cuadro de lista; un valor **false** lo oculta.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto siempre es **true**.

## <a name="remarks"></a>Observaciones

Este mensaje no tiene ningún efecto en un cuadro combinado creado con el estilo [**\_ simple CBS**](combo-box-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
</dt> </dl>

 

 





