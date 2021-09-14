---
title: BCM_GETNOTELENGTH mensaje (Commctrl.h)
description: Obtiene la longitud del texto de la nota que se puede mostrar en la descripción de un botón de vínculo de comando. Envíe este mensaje explícitamente o mediante la \_ macro Button GetNoteLength.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- BCM_GETNOTELENGTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170125"
---
# <a name="bcm_getnotelength-message"></a>Mensaje \_ GETNOTELENGTH de BCM

Obtiene la longitud del texto de la nota que se puede mostrar en la descripción de un botón de vínculo de comando. Envíe este mensaje explícitamente o mediante la macro [**\_ Button GetNoteLength.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la longitud del texto de la nota en **WCHARs**, sin incluir ningún valor **NULL** de terminación, o cero si no hay texto de nota.

## <a name="remarks"></a>Observaciones

A partir de comctl32 DLL versión 6.01, los botones de vínculo de comando pueden tener una nota. Para obtener información sobre las versiones de DLL, vea [Versiones de control comunes](common-control-versions.md).

El **mensaje \_ GETNOTELENGTH** de BCM solo funciona con los estilos de botón [**\_ BS COMMANDLINK**](button-styles.md) y [**BS \_ DEFCOMMANDLINK.**](button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Tipos de botón](button-types-and-styles.md)
</dt> </dl>

 

 





