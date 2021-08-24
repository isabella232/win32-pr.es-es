---
title: EM_DISPLAYBAND mensaje (Richedit.h)
description: Muestra una parte del contenido de un control de edición enriquecido, como se ha formatado previamente para un dispositivo mediante el mensaje EM \_ FORMATRANGE.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- EM_DISPLAYBAND controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67fc951940d76dced2851a01b7049b053f3e3c2b45f6eee95eb27bef633f59c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915945"
---
# <a name="em_displayband-message"></a>Mensaje \_ DE EM DISPLAYBAND

Muestra una parte del contenido de un control de edición enriquecido, como se ha formatado previamente para un dispositivo mediante el [**mensaje EM \_ FORMATRANGE.**](em-formatrange.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**RECT**](/previous-versions//dd162897(v=vs.85)) que especifica el área de presentación del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es **TRUE.**

Si se produce un error en la operación, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Comentarios

Los objetos Text y Component Object Model (COM) se recortan mediante el rectángulo. La aplicación no necesita establecer la región de recorte.

La banda es el proceso por el que se genera una sola página de salida mediante uno o varios rectángulos o bandas independientes. Cuando todas las bandas se colocan en la página, se produce una imagen completa. Este enfoque lo suelen usar las impresoras de trama que no tienen suficiente memoria o capacidad para crear imágenes de una página completa a la vez. Los dispositivos de banda incluyen la mayoría de las impresoras de matriz de puntos, así como algunas impresoras de rayos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Imprimir controles rich edit](printing-rich-edit-controls.md)
</dt> </dl>

 

