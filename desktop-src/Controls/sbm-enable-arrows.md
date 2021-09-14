---
title: SBM_ENABLE_ARROWS mensaje (Winuser.h)
description: Una aplicación envía el mensaje SBM ENABLE ARROWS para habilitar o deshabilitar una o ambas flechas de un control de \_ \_ barra de desplazamiento.
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
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167089"
---
# <a name="sbm_enable_arrows-message"></a>Mensaje SBM \_ ENABLE \_ ARROWS

Una aplicación envía el mensaje **SBM \_ ENABLE \_ ARROWS** para habilitar o deshabilitar una o ambas flechas de un control de barra de desplazamiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si las flechas de la barra de desplazamiento están habilitadas o deshabilitadas e indica qué flechas están habilitadas o deshabilitadas. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                   | Significado                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB \_ DISABLE \_ BOTH**</dt> </dl> | Deshabilita ambas flechas en una barra de desplazamiento.<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**DESHABILITACIÓN DE ESB \_ \_**</dt> </dl> | Deshabilita la flecha hacia abajo en una barra de desplazamiento vertical.<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**ESB \_ DISABLE \_ LTUP**</dt> </dl> | Deshabilita la flecha izquierda en una barra de desplazamiento horizontal o la flecha arriba en una barra de desplazamiento vertical.<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**ESB \_ DISABLE \_ LEFT**</dt> </dl> | Deshabilita la flecha izquierda en una barra de desplazamiento horizontal.<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**ESB \_ DISABLE \_ RTDN**</dt> </dl> | Deshabilita la flecha derecha en una barra de desplazamiento horizontal o la flecha hacia abajo en una barra de desplazamiento vertical.<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**DESHABILITACIÓN DE ESB \_ \_**</dt> </dl>       | Deshabilita la flecha arriba en una barra de desplazamiento vertical.<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**ESB \_ HABILITAR \_ AMBOS**</dt> </dl>    | Habilita ambas flechas en una barra de desplazamiento.<br/>                                                            |



 

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
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





