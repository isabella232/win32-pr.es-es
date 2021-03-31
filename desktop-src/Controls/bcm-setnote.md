---
title: Mensaje de BCM_SETNOTE (commctrl. h)
description: Establece el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button SetNote.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- BCM_SETNOTE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996380"
---
# <a name="bcm_setnote-message"></a>\_Mensaje SETNOTE de BCM

Establece el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena **WCHAR** terminada en null que contiene la nota.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

A partir de la versión 6,01 de comctl32 DLL, los botones de vínculo de comando pueden tener una nota.

El **mensaje \_ SETNOTE de BCM** solo funciona con los estilos de botón [**BS \_ COMMANDLINK**](button-styles.md) y [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Tipos de botón](button-types-and-styles.md)
</dt> </dl>

 

 





