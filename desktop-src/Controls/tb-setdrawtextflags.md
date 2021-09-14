---
title: TB_SETDRAWTEXTFLAGS mensaje (Commctrl.h)
description: Establece las marcas de dibujo de texto de la barra de herramientas.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- TB_SETDRAWTEXTFLAGS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166626"
---
# <a name="tb_setdrawtextflags-message"></a>Mensaje \_ SETDRAWTEXTFLAGS de TB

Establece las marcas de dibujo de texto de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Una o varias de las marcas DT, especificadas en DrawText , que indican qué bits de \_ *lParam* se usarán al dibujar el [](/windows/desktop/api/winuser/nf-winuser-drawtext)texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Una o varias marcas \_ DT, especificadas en [**DrawText,**](/windows/desktop/api/winuser/nf-winuser-drawtext)que indican cómo se dibujará el texto del botón. Este valor se pasará a la **función DrawText** cuando se dibuje el texto del botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve las marcas de dibujo de texto anteriores.

## <a name="remarks"></a>Observaciones

El *parámetro wParam* permite especificar qué marcas se usarán al dibujar el texto, incluso si estas marcas están desactivadas. Por ejemplo, si no desea que se utilice la marca DT CENTER al dibujar texto, agregaría la marca DT CENTER a wParam y no especificaría la marca DT CENTER en \_ \_  \_ *lParam*. Esto impide que el control pase la marca DT \_ CENTER a la función [**DrawText.**](/windows/desktop/api/winuser/nf-winuser-drawtext)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

