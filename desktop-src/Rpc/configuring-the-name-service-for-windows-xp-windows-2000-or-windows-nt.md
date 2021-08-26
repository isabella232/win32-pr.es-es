---
title: Configuración del servicio de nombres
description: A partir Windows 2000, al instalar el SDK de Windows, el programa de instalación selecciona automáticamente Localizador de Microsoft como proveedor de servicios de nombres. Puede cambiar el proveedor de servicios de nombre mediante Panel de control.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84450f4408ac0e90be04cfff7d1cbc92890cde4434969431a986e9cda378ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022445"
---
# <a name="configuring-the-name-service"></a>Configuración del servicio de nombres

A partir Windows 2000, al instalar el SDK de Windows, el programa de instalación selecciona automáticamente Localizador de Microsoft como proveedor de servicios de nombres. Puede cambiar el proveedor de servicios de nombre mediante Panel de control.

El equipo host que ejecuta el nsid actúa como puerta de enlace a DCE Servicio de directorio de celdas, pasando llamadas de función NSI entre equipos que ejecutan sistemas operativos de Microsoft y equipos DCE. Una dirección de red puede tener hasta 80 caracteres; por ejemplo, 11.1.9.169 es una dirección válida.

> [!Note]  
> Debe tener el producto Digital Equipment Corporation DCE CDS para configurar DCE CDS como proveedor de servicios de nombre. Consulte la documentación proporcionada por Digital Equipment Corporation para obtener información sobre DCE CDS.

 

**Para volver a configurar el proveedor de servicios de nombres**

1.  En Panel de control, haga clic en el **icono Conexiones de** red. Aparece **la ventana Conexiones de** red.
2.  Seleccione la conexión de red que desea configurar, haga clic con el botón derecho y seleccione **Propiedades** en el menú contextual. Aparece **el cuadro de diálogo Propiedades** de conexión.
3.  En el cuadro **de diálogo Propiedades de** conexión, seleccione Cliente para redes **Microsoft** y haga clic en **el botón** Propiedades. Aparece el cuadro de diálogo Propiedades de red de Cliente para **Microsoft.**
4.  En el cuadro de diálogo Propiedades de red de Cliente para **Microsoft,** abra la lista desplegable Proveedor de **servicios** de nombres y seleccione un proveedor de nombres en la lista.
    1.  Al seleccionar Localizador de Microsoft, haga clic en Aceptar. A continuación, se completa el proceso de configuración.
    2.  Al seleccionar la instancia de DCE  Servicio de directorio de celdas, en el cuadro Dirección de red , escriba el nombre del equipo host que ejecuta el demonio NSI (nsid) y, a continuación, haga clic en Aceptar.

**Para volver a configurar el proveedor de servicios de nombre Windows 2000**

1.  En Panel de control, haga clic en **el icono** Red.

    Aparece **el cuadro** de diálogo Red.

2.  En el cuadro **de diálogo** Red , haga clic **en Configurar**.
3.  En la **lista NetworkSoftware,** seleccione **Configuración de RPC.**

    Aparece el cuadro de diálogo Configuración **del proveedor de servicios de** nombres RPC.

4.  En el cuadro **de diálogo Configuración del proveedor** de servicios de nombres RPC , seleccione un proveedor de servicios de nombres de la lista.
    1.  Al seleccionar Localizador de Microsoft, haga clic en Aceptar. A continuación, se completa el proceso de configuración.
    2.  Al seleccionar la instancia de DCE  Servicio de directorio de celdas, en el cuadro Dirección de red , escriba el nombre del equipo host que ejecuta el demonio NSI (nsid) y, a continuación, haga clic en Aceptar.

 

 




