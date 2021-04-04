---
description: Utilice el procedimiento siguiente para desarrollar una nueva aplicación, o actualizar una aplicación existente, para usar los ensamblados en paralelo disponibles de Microsoft u otros publicadores de ensamblados en paralelo.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Usar ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907831"
---
# <a name="using-side-by-side-assemblies"></a>Usar ensamblados en paralelo

Utilice el procedimiento siguiente para desarrollar una nueva aplicación, o actualizar una aplicación existente, para usar los [ensamblados en paralelo](about-side-by-side-assemblies-.md) disponibles de Microsoft u otros publicadores de ensamblados en paralelo. Para obtener una lista de los ensamblados en paralelo proporcionados por Microsoft actualmente, consulte [ensamblados en paralelo de Microsoft compatibles](supported-microsoft-side-by-side-assemblies.md). Tenga en cuenta que la aplicación debe ejecutarse al menos en Windows XP para instalar los ensamblados como ensamblados en paralelo. Para obtener más información, vea [instrucciones para crear ensamblados en paralelo](guidelines-for-creating-side-by-side-assemblies.md).

**Para agregar un ensamblado en paralelo a una aplicación**

1.  Identificar los ensamblados en paralelo que requiere la aplicación. A partir de Windows XP, estos ensamblados en paralelo y sus manifiestos de ensamblado se instalan con el sistema operativo, pero no se registran de forma global.
2.  Use un editor XML para crear un [manifiesto de aplicación](application-manifests.md). Vea el siguiente manifiesto de aplicación de ejemplo. Para obtener más información, consulte [manifiestos de aplicación](application-manifests.md) en la [referencia de archivos de manifiesto](manifest-files-reference.md).
3.  Escriba los valores de atributo en el subelemento [*assemblyIdentity del contexto de Def*](d-sbscs-gly.md) del manifiesto de aplicación que define la aplicación de forma única. Para obtener más información sobre el **assemblyIdentity** de Def-context, consulte [manifiestos de aplicación](application-manifests.md).
4.  Si el ensamblado contiene ensamblados dependientes, escriba los valores de atributo en los subelementos de [*assemblyIdentity de contexto de referencia*](r-sbscs-gly.md) correspondientes del manifiesto de aplicación. Para obtener más información sobre el **assemblyIdentity** de referencia, vea [manifiestos de aplicación](application-manifests.md).

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  Puede incluir el manifiesto de aplicación en el archivo de encabezado ejecutable binario de la aplicación.

    En este caso, agregue también la siguiente línea al archivo de encabezado de la aplicación:

    <dl> Manifiesto del manifiesto de CREATEPROCESS ID. de recurso de manifiesto \_ \_ \_ RT \_ "YourApp.exe. manifest"  
    </dl>

    Como alternativa, puede colocar un archivo de manifiesto independiente en el mismo directorio que el archivo ejecutable de la aplicación. El sistema operativo carga primero el manifiesto del sistema de archivos y, a continuación, comprueba la sección de recursos del archivo ejecutable. La versión del sistema de archivos tiene prioridad.

6.  Los [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies) deben instalarse con la versión [Windows Installer](../msi/windows-installer-portal.md) 2,0. Cree un paquete de Windows Installer como se describe en [¿cómo se instalan los ensamblados Win32 para el uso compartido simultáneo en Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).
7.  Los [ensamblados privados](/windows/desktop/Msi/private-assemblies) se pueden instalar con la versión [Windows Installer](../msi/windows-installer-portal.md) 2,0. Cree un paquete de Windows Installer como se describe en [¿cómo se instalan los ensamblados Win32 para el uso privado de una aplicación en Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md). También puede usar cualquier otro instalador para copiar un ensamblado privado y su manifiesto en la misma carpeta que el archivo ejecutable de la aplicación.
8.  Pruebe la aplicación para garantizar los resultados. Tenga en cuenta que el equipo de prueba no debe tener el ensamblado en paralelo registrado.
9.  Implemente la aplicación o actualice como un paquete de Windows Installer.

## <a name="example-application-manifest"></a>Ejemplo de manifiesto de aplicación

El siguiente es un ejemplo de un manifiesto de aplicación:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
