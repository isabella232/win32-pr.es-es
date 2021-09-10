---
title: Configuración de un controlador instalable
description: Configuración de un controlador instalable
ms.assetid: c81f4bcb-38c6-42f1-a50d-1f700c6a3c37
keywords:
- controladores instalables, configuración
- configuración de controladores instalables
- Función OpenDriver
- Función SendDriverMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0ad16d719152dba0dc0b2ca6224122831a0ce
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372098"
---
# <a name="configuring-an-installable-driver"></a>Configuración de un controlador instalable

Para dirigir un controlador instalable para llevar a cabo tareas útiles, debe abrir el controlador mediante la función [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) y enviarle mensajes mediante la [función SendDriverMessage.](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) En el ejemplo siguiente se muestra cómo dirigir al controlador para que muestre su cuadro de diálogo de configuración.


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



 

 