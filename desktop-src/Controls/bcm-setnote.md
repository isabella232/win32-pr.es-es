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
ms.openlocfilehash: 82f0f049c1ad8a9837695a1f5d7327883e1dabfb7dd077bd6efce78fa6a0a708
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921555"
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

## <a name="remarks"></a>Comentarios

A partir de comctl32 DLL versión 6.01, los botones de vínculo de comando pueden tener una nota.

El **mensaje \_ SETNOTE de BCM** solo funciona con los estilos de botón [**\_ BS COMMANDLINK**](button-styles.md) y [**BS \_ DEFCOMMANDLINK.**](button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



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

 

 





