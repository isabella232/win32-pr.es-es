---
title: Configuración de un controlador instalable
description: Configuración de un controlador instalable
ms.assetid: c81f4bcb-38c6-42f1-a50d-1f700c6a3c37
keywords:
- Controladores instalables, configurar
- configuración de controladores instalables
- OpenDriver función)
- SendDriverMessage función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0ad16d719152dba0dc0b2ca6224122831a0ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077582"
---
# <a name="configuring-an-installable-driver"></a>Configuración de un controlador instalable

Para dirigir un controlador instalable para llevar a cabo tareas útiles, debe abrir el controlador mediante la función [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) y enviar mensajes mediante la función [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) . En el ejemplo siguiente se muestra cómo dirigir el controlador para que muestre su cuadro de diálogo de configuración.


```C++
LONG MyConfigureDriver()
{
    HDRVR hdrvr;
    DRVCONFIGINFO dci;
    LONG lRes;

    // Open the driver (no additional parameters needed this time).
    if ((hdrvr = OpenDriver(L"\\samples\\sample.drv", 0, 0)) == 0) {
        // Can't open the driver
        return DRVCNF_CANCEL;
    }

    // Make sure driver has a configuration dialog box.
    if (SendDriverMessage(hdrvr, DRV_QUERYCONFIGURE, 0, 0) != 0) {
        // Set the DRVCONFIGINFO structure and send the message
        dci.dwDCISize = sizeof (dci);
        dci.lpszDCISectionName = (LPWSTR)0;
        dci.lpszDCIAliasName = (LPWSTR)0;
        lRes = SendDriverMessage(hdrvr, DRV_CONFIGURE, 0, (LONG)&dci);
     }

    // Close the driver (no additional parameters needed this time).
    CloseDriver(hdrvr, 0, 0);

    return lRes;
}
 
```



 

 