---
title: Mensaje de EM_REPLACESEL (Winuser. h)
description: Reemplaza el texto seleccionado en un control de edición o un control Rich Edit con el texto especificado.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- EM_REPLACESEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151149"
---
# <a name="em_replacesel-message"></a>\_Mensaje REPLACESEL em

Reemplaza el texto seleccionado en un control de edición o un control Rich Edit con el texto especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si se puede deshacer la operación de reemplazo. Si es **true**, se puede deshacer la operación. Si es **false** , la operación no se puede deshacer.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena terminada en null que contiene el texto de reemplazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use el **mensaje \_ REPLACESEL em** para reemplazar solo una parte del texto en un control de edición. Para reemplazar todo el texto, use el mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .

Si no hay ninguna selección, el texto de sustitución se inserta en el símbolo de intercalación.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

En un control Rich Edit, el texto de reemplazo toma el formato del carácter en el símbolo de intercalación o, si hay una selección, del primer carácter de la selección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SETTEXT de WM \_**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

