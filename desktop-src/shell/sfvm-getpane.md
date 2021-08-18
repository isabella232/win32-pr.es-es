---
description: SFVM \_ GETPANE puede modificarse o no estar disponible.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: SFVM_GETPANE mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef936d4218c29c8d0574e97b8de73c1a0d54f4d62df7dba4f43f371bfeaf95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968674"
---
# <a name="sfvm_getpane-message"></a>Mensaje \_ GETPANE de SFVM

\[**SFVM \_ GETPANE** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Permite que el objeto de devolución de llamada proporcione el panel de la barra de estado en el que se va a mostrar la información de la zona de Internet. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*paneID* \[ En\]
</dt> <dd>

Identificador del panel solicitado. Normalmente se trata de PANE \_ ZONE, pero puede ser cualquiera de los valores siguientes.

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span id="PANE_NONE"></span><span id="pane_none"></span>**PANEL \_ NINGUNO**


</dt> <dd>

No hay ningún panel.

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>**ZONA \_ DE PANEL**


</dt> <dd>

El panel Zona de Internet.

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PANEL \_ SIN CONEXIÓN**


</dt> <dd>

Panel sin conexión.

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>**IMPRESORA \_ DE PANEL**


</dt> <dd>

Panel de indicaciones de impresión.

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>**PANEL \_ SSL**


</dt> <dd>

Panel SSL.

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**NAVEGACIÓN POR \_ EL PANEL**


</dt> <dd>

Panel de navegación.

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**PROGRESO DEL \_ PANEL**


</dt> <dd>

Panel de la barra de progreso.

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PRIVACIDAD \_ DEL PANEL**


</dt> <dd>

Panel indicador de privacidad.

</dd> </dl> </dd> <dt>

*panel* \[ out\]
</dt> <dd>

Puntero a un **DWORD** que contiene el número de panel.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
