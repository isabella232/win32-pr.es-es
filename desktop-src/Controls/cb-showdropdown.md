---
title: CB_SHOWDROPDOWN mensaje (Winuser.h)
description: Una aplicación envía un mensaje CB SHOWDROPDOWN para mostrar u ocultar el cuadro de lista de un cuadro combinado que tiene el estilo CBS DROPDOWN o \_ \_ CBS \_ DROPDOWNLIST.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN controles de Windows mensaje
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
ms.openlocfilehash: 6c820c65c053f7acbcffb379228ea5f7720476b6d2165ac4988ce8789e912cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832243"
---
# <a name="cb_showdropdown-message"></a>Mensaje \_ SHOWDROPDOWN de CB

Una aplicación envía un **mensaje \_ CB SHOWDROPDOWN** para mostrar u ocultar el cuadro de lista de un cuadro combinado que tiene el estilo [**CBS \_ DROPDOWN**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST.**](combo-box-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un **valor BOOL** que especifica si el cuadro de lista desplegable se va a mostrar u ocultar. Un valor true **muestra** el cuadro de lista; Un valor **de FALSE** lo oculta.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto siempre es **TRUE.**

## <a name="remarks"></a>Comentarios

Este mensaje no tiene ningún efecto en un cuadro combinado creado con el [**estilo \_ SIMPLE de CBS.**](combo-box-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
</dt> </dl>

 

 





