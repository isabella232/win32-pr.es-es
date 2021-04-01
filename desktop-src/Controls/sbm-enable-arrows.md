---
title: Mensaje de SBM_ENABLE_ARROWS (Winuser. h)
description: Una aplicación envía el \_ mensaje de \_ flechas habilitar SBM para habilitar o deshabilitar una o ambas flechas de un control de barra de desplazamiento.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- SBM_ENABLE_ARROWS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996807"
---
# <a name="sbm_enable_arrows-message"></a>\_Mensaje de flechas habilitadas de SBM \_

Una aplicación envía el mensaje de **\_ \_ flechas habilitar SBM** para habilitar o deshabilitar una o ambas flechas de un control de barra de desplazamiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si las flechas de la barra de desplazamiento están habilitadas o deshabilitadas e indica qué flechas están habilitadas o deshabilitadas. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                   | Significado                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB \_ deshabilitar \_ ambas**</dt> </dl> | Deshabilita ambas flechas en una barra de desplazamiento.<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**deshabilitar ESB \_ \_**</dt> </dl> | Deshabilita la flecha hacia abajo de una barra de desplazamiento vertical.<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**ESB \_ Disable \_ LTUP**</dt> </dl> | Deshabilita la flecha izquierda en una barra de desplazamiento horizontal o en la flecha hacia arriba de una barra de desplazamiento vertical.<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**\_deshabilitación ESB \_ izquierda**</dt> </dl> | Deshabilita la flecha izquierda en una barra de desplazamiento horizontal.<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**ESB \_ Disable \_ RTDN**</dt> </dl> | Deshabilita la flecha derecha en una barra de desplazamiento horizontal o en la flecha hacia abajo de una barra de desplazamiento vertical.<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**deshabilitar ESB \_ \_**</dt> </dl>       | Deshabilita la flecha arriba en una barra de desplazamiento vertical.<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**ESB \_ habilitar \_ ambos**</dt> </dl>    | Habilita ambas flechas en una barra de desplazamiento.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es **true**; de lo contrario, es **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 





