---
title: Configuración del servicio de nombres
description: A partir de Windows 2000, al instalar el Windows SDK, el programa de instalación selecciona automáticamente Microsoft Locator como proveedor de servicio de nombres. Puede cambiar el proveedor de servicios de nombres a través del panel de control.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486778"
---
# <a name="configuring-the-name-service"></a>Configuración del servicio de nombres

A partir de Windows 2000, al instalar el Windows SDK, el programa de instalación selecciona automáticamente Microsoft Locator como proveedor de servicio de nombres. Puede cambiar el proveedor de servicios de nombres a través del panel de control.

El equipo host que ejecuta NSID actúa como puerta de enlace al Servicio de directorio de celdas de DCE, pasando llamadas a la función NSI entre equipos que ejecutan sistemas operativos de Microsoft y equipos DCE. Una dirección de red puede tener hasta 80 caracteres, por ejemplo, 11.1.9.169 es una dirección válida.

> [!Note]  
> Para configurar los CD de DCE como proveedor de servicios de nombres, debe tener el producto de los CD de DCE de Digital Equipment Corporation. Consulte la documentación proporcionada por Digital Equipment Corporation para obtener información acerca de los CD de DCE.

 

**Para volver a configurar el proveedor de servicios de nombres**

1.  En el panel de control, haga clic en el icono **conexiones de red** . Aparece la ventana **conexiones de red** .
2.  Seleccione la conexión de red que desea configurar, haga clic con el botón secundario y seleccione **propiedades** en el menú contextual. Aparece el cuadro de diálogo Propiedades de la **conexión** .
3.  En el cuadro de diálogo **propiedades de conexión** , seleccione **cliente para redes de Microsoft** y haga clic en el botón **propiedades** . Aparece el cuadro **de diálogo Propiedades de cliente para Microsoft Network** .
4.  En el cuadro de diálogo **propiedades de cliente para Microsoft Network** , abra el menú desplegable **proveedor de servicios de nombres** y seleccione un proveedor de nombres de la lista.
    1.  Al seleccionar localizador de Microsoft, haga clic en Aceptar. A continuación, se completa el proceso de configuración.
    2.  Al seleccionar el Servicio de directorio de celdas DCE, en el cuadro **dirección de red** , escriba el nombre del equipo host que ejecuta el demonio NSI (NSID) y, a continuación, haga clic en Aceptar.

**Para volver a configurar el proveedor de servicios de nombres para Windows 2000**

1.  En el panel de control, haga clic en el icono **red** .

    Aparece el cuadro de diálogo **red** .

2.  En el cuadro de diálogo **red** , haga clic en **configurar**.
3.  En la lista **NetworkSoftware** , seleccione **configuración de RPC**.

    Aparece el cuadro de diálogo **configuración de proveedor de servicio de nombres de RPC** .

4.  En el cuadro de diálogo **configuración de proveedor de servicio de nombres RPC** , seleccione un proveedor de servicios de nombres de la lista.
    1.  Al seleccionar localizador de Microsoft, haga clic en Aceptar. A continuación, se completa el proceso de configuración.
    2.  Al seleccionar el Servicio de directorio de celdas DCE, en el cuadro **dirección de red** , escriba el nombre del equipo host que ejecuta el demonio NSI (NSID) y, a continuación, haga clic en Aceptar.

 

 




