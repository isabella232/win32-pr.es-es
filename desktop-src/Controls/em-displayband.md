---
title: Mensaje EM_DISPLAYBAND (RichEdit. h)
description: Muestra una parte del contenido de un control Rich Edit, como se formateó anteriormente para un dispositivo mediante el \_ mensaje em FORMATRANGE.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- EM_DISPLAYBAND controles de mensajes de Windows
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
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996651"
---
# <a name="em_displayband-message"></a>\_Mensaje DISPLAYBAND em

Muestra una parte del contenido de un control Rich Edit, como se formateó anteriormente para un dispositivo mediante el mensaje [**em \_ FORMATRANGE**](em-formatrange.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica el área de presentación del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es **true**.

Si se produce un error en la operación, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

El rectángulo recorta el texto y los objetos del modelo de objetos componentes (COM). No es necesario que la aplicación establezca la región de recorte.

El uso de bandas es el proceso por el que se genera una sola página de salida mediante uno o varios rectángulos o bandas independientes. Cuando todas las bandas se colocan en la página, se obtiene una imagen completa. Este enfoque suele usarse en impresoras de tramas que no tienen suficiente memoria o capacidad de imagen de una página completa al mismo tiempo. Los dispositivos de bandas incluyen la mayoría de las impresoras matriciales, así como algunas impresoras láser.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Imprimir controles Rich Edit](printing-rich-edit-controls.md)
</dt> </dl>

 

