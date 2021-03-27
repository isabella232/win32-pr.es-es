---
description: SFVM \_ GETPANE puede modificarse o no estar disponible.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: Mensaje de SFVM_GETPANE (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002300"
---
# <a name="sfvm_getpane-message"></a>SFVM \_ GETPANE

\[**SFVM \_ GETPANE** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Permite que el objeto de devolución de llamada proporcione el panel de la barra de estado en el que se va a mostrar la información de la zona de Internet. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*paneID* \[ de\]
</dt> <dd>

IDENTIFICADOR del panel solicitado. Suele \_ ser la zona del panel, pero puede ser cualquiera de los valores siguientes.

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span id="PANE_NONE"></span><span id="pane_none"></span>**ninguno de los paneles \_**


</dt> <dd>

Ningún panel.

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>**zona del panel \_**


</dt> <dd>

Panel zona de Internet.

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PANEL \_ sin conexión**


</dt> <dd>

Panel sin conexión.

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>**impresora de panel \_**


</dt> <dd>

El panel de indicación de impresión.

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>**SSL de panel \_**


</dt> <dd>

El panel SSL.

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**navegación de panel \_**


</dt> <dd>

Panel de navegación.

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**progreso del panel \_**


</dt> <dd>

Panel de la barra de progreso.

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**privacidad del panel \_**


</dt> <dd>

El panel indicador de privacidad.

</dd> </dl> </dd> <dt>

*Panel* \[ de enuncia\]
</dt> <dd>

Puntero a un **valor DWORD** que contiene el número del panel.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
