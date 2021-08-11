---
description: Las aplicaciones pueden declarar el aislamiento de controlador de impresora en su manifiesto de aplicación para aislar la aplicación del controlador de impresora y mejorar la confiabilidad de las aplicaciones.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 'Cómo: Usar el aislamiento de aplicaciones'
ms.date: 05/31/2018
ms.openlocfilehash: 818ba30e7b294c695b2f67bb9bccc485959db43818bb95aedaa67cafc26d3559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233836"
---
# <a name="how-to-use-application-isolation"></a>Cómo: Usar el aislamiento de aplicaciones

Las aplicaciones pueden declarar el aislamiento de controlador de impresora en su manifiesto de aplicación para aislar la aplicación del controlador de impresora y mejorar la confiabilidad de la aplicación. El Windows de impresión permite que los controladores de impresora se ejecuten en procesos independientes del proceso en el que se ejecuta el cola de impresión. El uso de esta característica impide que la aplicación se bloquea en caso de que el controlador de impresora tenga un error.

El aislamiento del controlador de impresora se implementa en Windows 7 y Windows Server 2008 R2.

### <a name="prerequisites"></a>Requisitos previos

-   Un código administrado o una Windows Store que usa Windows impresión.

## <a name="instructions"></a>Instrucciones

### <a name="update-the-app-manifest"></a>Actualización del manifiesto de aplicación

La habilitación del aislamiento de controlador de impresora requiere que se agregue el elemento **printerDriverIsolation** al manifiesto de la aplicación. Le mostramos cómo:

1.  Edite el manifiesto de aplicación y agregue el elemento **printerDriverIsolation** con un valor de **true** al elemento **windowsSettings** del elemento **de** aplicación, como se muestra en este ejemplo.
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  Recompile la aplicación.

 

 



