---
description: Las aplicaciones pueden declarar el aislamiento del controlador de impresora en el manifiesto de la aplicación para aislar la aplicación del controlador de impresora y mejorar la confiabilidad de las aplicaciones.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 'Cómo: utilizar el aislamiento de aplicaciones'
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276771"
---
# <a name="how-to-use-application-isolation"></a>Cómo: utilizar el aislamiento de aplicaciones

Las aplicaciones pueden declarar el aislamiento del controlador de impresora en el manifiesto de la aplicación para aislar la aplicación del controlador de impresora y mejorar la confiabilidad de la aplicación. El servicio de impresión de Windows permite que los controladores de impresora se ejecuten en procesos independientes del proceso en el que se ejecuta el administrador de trabajos de impresión. Con esta característica, la aplicación impide que se bloquee en caso de que se produzca un error en el controlador de impresora.

El aislamiento del controlador de impresora se implementa en Windows 7 y Windows Server 2008 R2.

### <a name="prerequisites"></a>Requisitos previos

-   Una aplicación de código administrado o de la tienda Windows que usa la impresión de Windows.

## <a name="instructions"></a>Instrucciones

### <a name="update-the-app-manifest"></a>Actualización del manifiesto de la aplicación

Para habilitar el aislamiento del controlador de impresora, es necesario agregar el elemento **printerDriverIsolation** al manifiesto de la aplicación. A continuación se muestra cómo hacerlo:

1.  Edite el manifiesto de la aplicación, agregando el elemento **printerDriverIsolation** con un valor de **true** al elemento **windowsSettings** del elemento **Application** , como se muestra en este ejemplo.
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  Vuelva a compilar la aplicación.

 

 



