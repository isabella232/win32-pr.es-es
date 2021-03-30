---
title: Mensaje de HDM_EDITFILTER (commctrl. h)
description: Mueve el foco de entrada al cuadro de edición cuando un botón de filtro tiene el foco.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- HDM_EDITFILTER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802863"
---
# <a name="hdm_editfilter-message"></a>HDM \_ EDITFILTER

Mueve el foco de entrada al cuadro de edición cuando un botón de filtro tiene el foco.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica la columna que se va a editar.

</dd> <dt>

*lParam* 
</dt> <dd>

Marca que especifica cómo controlar los cambios de edición del usuario. Use esta marca para especificar qué hacer si el usuario se encuentra en el proceso de edición del filtro cuando se envía el mensaje.



| Value                                                                                                                                      | Significado                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt></dt><dt> **True**</dt> </dl>  | Descartar los cambios realizados por el usuario. <br/> |
| <dl> <dt></dt><dt> **False**</dt> </dl> | Acepte los cambios realizados por el usuario. <br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero. **LRESULT** se convierte en un entero que indica **true**(1) o **false**(0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HDM \_ CLEARFILTER**](hdm-clearfilter.md)
</dt> </dl>

 

 





