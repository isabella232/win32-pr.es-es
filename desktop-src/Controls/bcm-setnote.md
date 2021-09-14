---
title: BCM_SETNOTE mensaje (Commctrl.h)
description: Establece el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o usar la macro Button \_ SetNote.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- BCM_SETNOTE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968743"
---
# <a name="bcm_setnote-message"></a>Mensaje \_ SETNOTE de BCM

Establece el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o usar la macro [**Button \_ SetNote.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena **WCHAR** terminada en NULL que contiene la nota.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

A partir de comctl32 DLL versión 6.01, los botones de vínculo de comando pueden tener una nota.

El **mensaje \_ SETNOTE de BCM** solo funciona con los estilos de botón [**\_ BS COMMANDLINK**](button-styles.md) y [**BS \_ DEFCOMMANDLINK.**](button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Tipos de botón](button-types-and-styles.md)
</dt> </dl>

 

 





