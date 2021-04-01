---
title: Mensaje de TB_SETDRAWTEXTFLAGS (commctrl. h)
description: Establece las marcas de dibujo de texto de la barra de herramientas.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- TB_SETDRAWTEXTFLAGS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996801"
---
# <a name="tb_setdrawtextflags-message"></a>\_Mensaje SETDRAWTEXTFLAGS TB

Establece las marcas de dibujo de texto de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Una o varias de las \_ marcas DT, especificadas en [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), que indican qué bits de *lParam* se utilizarán al dibujar el texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Una o varias de las \_ marcas DT, especificadas en [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), que indican cómo se dibujará el texto del botón. Este valor se pasará a la función **DrawText** cuando se dibuje el texto del botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve las marcas de dibujo de texto anteriores.

## <a name="remarks"></a>Observaciones

El parámetro *wParam* le permite especificar qué marcas se utilizarán al dibujar el texto, aunque estas marcas estén desactivadas. Por ejemplo, si no desea que se use la \_ marca DT Center al dibujar texto, debe agregar la marca DT \_ Center a *wParam* y no especificar la marca DT \_ Center en *lParam*. Esto evita que el control pase la \_ marca DT Center a la función [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

