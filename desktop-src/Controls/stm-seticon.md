---
title: STM_SETICON mensaje (Winuser.h)
description: Una aplicación envía el mensaje SETICON de STM \_ para asociar un icono a un control de icono.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- STM_SETICON controles de Windows mensaje
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167001"
---
# <a name="stm_seticon-message"></a>Mensaje SETICON de STM \_

Una aplicación envía el mensaje **\_ SETICON de STM** para asociar un icono a un control de icono.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Controle el icono para asociarlo al control de icono.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador del icono asociado previamente al control de icono o cero si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**STM \_ GETICON**](stm-geticon.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**LoadIcon**](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

