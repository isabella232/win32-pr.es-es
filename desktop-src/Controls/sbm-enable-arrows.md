---
title: SBM_ENABLE_ARROWS mensaje (Winuser.h)
description: Una aplicación envía el mensaje SBM ENABLE ARROWS para habilitar o deshabilitar una o ambas \_ \_ flechas de un control de barra de desplazamiento.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- SBM_ENABLE_ARROWS controles de Windows mensaje
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e7f3ef8728befe72ec4f2c4afe39caeb10bc0b58984612a5db2445963dc549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770025"
---
# <a name="sbm_enable_arrows-message"></a>Mensaje de SBM \_ ENABLE \_ ARROWS

Una aplicación envía el mensaje **SBM \_ ENABLE \_ ARROWS** para habilitar o deshabilitar una o ambas flechas de un control de barra de desplazamiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si las flechas de la barra de desplazamiento están habilitadas o deshabilitadas e indica qué flechas están habilitadas o deshabilitadas. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                   | Significado                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB \_ DISABLE \_ BOTH**</dt> </dl> | Deshabilita ambas flechas en una barra de desplazamiento.<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**DESHABILITACIÓN DE ESB \_ \_**</dt> </dl> | Deshabilita la flecha abajo en una barra de desplazamiento vertical.<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**ESB \_ DISABLE \_ LTUP**</dt> </dl> | Deshabilita la flecha izquierda en una barra de desplazamiento horizontal o la flecha arriba en una barra de desplazamiento vertical.<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**ESB \_ DISABLE \_ LEFT**</dt> </dl> | Deshabilita la flecha izquierda en una barra de desplazamiento horizontal.<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**ESB \_ DISABLE \_ RTDN**</dt> </dl> | Deshabilita la flecha derecha en una barra de desplazamiento horizontal o la flecha abajo en una barra de desplazamiento vertical.<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**DESHABILITACIÓN DE ESB \_ \_**</dt> </dl>       | Deshabilita la flecha arriba en una barra de desplazamiento vertical.<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**HABILITACIÓN DE ESB \_ \_**</dt> </dl>    | Habilita ambas flechas en una barra de desplazamiento.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es **TRUE**; de lo contrario, es **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





