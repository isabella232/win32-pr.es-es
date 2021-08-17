---
description: Uso de Per-Application de configuración
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: Uso de Per-Application de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbc38a2433d2da6d2a39985523a5ebffd0d971102bc883e44ae24d9fcc165ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372345"
---
# <a name="using-per-application-configuration-files"></a>Uso de Per-Application de configuración

El uso de archivos de configuración de COM+ por aplicación requiere los siguientes pasos básicos:

-   Configure un directorio raíz de la aplicación para una aplicación COM+.
-   Cree application.manifest y application.config archivos en el directorio raíz de la aplicación COM+.

> [!Note]  
> Los archivos de configuración por aplicación solo están disponibles a partir de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.

 

**Para usar un archivo de configuración por aplicación**

1.  Cree una biblioteca de clases .NET, con una referencia al ensamblado System.EnterpriseServices.

2.  La biblioteca de clases debe contener el código siguiente:

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    Tenga en cuenta que "ConfigData1" es un nombre de configuración de ejemplo. Puede reemplazarlo por el nombre de configuración que prefiera.

3.  Cree una aplicación COM+ vacía. Para obtener instrucciones sobre cómo hacerlo, consulte [Creación de una nueva aplicación COM+.](creating-a-new-com--application.md)
4.  Instale la biblioteca de clases que creó en la aplicación COM+. Para obtener instrucciones sobre cómo hacerlo, vea [Installing New Components](installing-new-components.md).
5.  En la herramienta administrativa Servicios de componentes, haga clic con el botón derecho en la aplicación COM+ que creó y seleccione **Propiedades.**
6.  En el **cuadro de** diálogo Propiedades, seleccione la **pestaña** Activación.
7.  Asegúrese de que **el tipo de activación** está establecido en Aplicación de **servidor**.
8.  En el **cuadro de texto Directorio** raíz de la aplicación, escriba la ruta de acceso o vaya al directorio donde desea almacenar los archivos de configuración de la aplicación para esta aplicación.
9.  Haga clic en **Aceptar**.

    Tenga en cuenta que también puede especificar el directorio raíz de la aplicación COM+ a través de la propiedad ApplicationDirectory de la [**clase COMAdminCatalogObject.**](comadmincatalogobject.md) Para obtener más información, vea [**Aplicaciones**](applications.md).

10. En el directorio que eligió para almacenar los archivos de configuración de la aplicación, cree un archivo denominado *.manifest de* aplicación. Con un editor de texto, agregue el texto siguiente a este archivo:

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. En el mismo directorio, cree un archivo denominado *application.config.* Con un editor de texto, agregue el texto siguiente a este archivo:

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    Tenga en cuenta que este archivo de configuración es simplemente un ejemplo. Puede crear varias claves con distintos nombres y valores. Sin embargo, tenga en cuenta que "ConfigData1" coincide con el nombre de configuración usado en la biblioteca de clases creada anteriormente.

12. Cree una aplicación de consola de .NET, con una referencia a la biblioteca de clases .NET que creó anteriormente y una referencia al ensamblado System.EnterpriseServices.
13. La aplicación de consola debe contener el código siguiente:
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

Ejecución de la aplicación de consola. La salida debe ser:

``` syntax
Configuration Data Number 1
```

 

 



