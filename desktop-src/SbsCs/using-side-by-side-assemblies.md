---
description: Use el procedimiento siguiente para desarrollar una nueva aplicación o actualizar una existente para usar los ensamblados en paralelo disponibles en Microsoft u otros publicadores de ensamblados en paralelo.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Usar ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60170dc4873f03dfc17769f91106e02b591e0b1db81695d773a35b392a2c7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141718"
---
# <a name="using-side-by-side-assemblies"></a>Usar ensamblados en paralelo

Use el procedimiento siguiente para desarrollar una nueva aplicación o [](about-side-by-side-assemblies-.md) actualizar una existente para usar los ensamblados en paralelo disponibles en Microsoft u otros publicadores de ensamblados en paralelo. Para obtener una lista de los ensamblados en paralelo proporcionados actualmente por Microsoft, vea Supported [Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md). Tenga en cuenta que la aplicación debe ejecutarse en al menos Windows XP para instalar los ensamblados como ensamblados en paralelo. Para obtener más información, vea Directrices para crear [ensamblados en paralelo.](guidelines-for-creating-side-by-side-assemblies.md)

**Para agregar un ensamblado en paralelo a una aplicación**

1.  Identifique los ensamblados en paralelo que requiere la aplicación. A partir Windows XP, estos ensamblados en paralelo y sus manifiestos de ensamblado se instalan con el sistema operativo, pero no se registran globalmente.
2.  Use un editor XML para crear un manifiesto [de aplicación](application-manifests.md). Consulte el siguiente manifiesto de aplicación de ejemplo. Para obtener más información, vea [Manifiestos de aplicación en](application-manifests.md) la referencia [de archivos de manifiesto.](manifest-files-reference.md)
3.  Escriba los valores de atributo en el [*subelemento assemblyIdentity*](d-sbscs-gly.md) del contexto DEF del manifiesto de aplicación que define de forma única la aplicación. Para obtener más información sobre el ensamblado de contexto **DEFIdentity**, vea [Manifiestos de aplicación](application-manifests.md).
4.  Si el ensamblado contiene ensamblados dependientes, escriba valores de atributo en los subelementos [*ref-context assemblyIdentity*](r-sbscs-gly.md) correspondientes del manifiesto de aplicación. Para obtener más información sobre ref-context **assemblyIdentity**, vea [Manifiestos de aplicación](application-manifests.md).

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  Puede incluir el manifiesto de aplicación en el archivo de encabezado ejecutable binario de la aplicación.

    En este caso, agregue también la siguiente línea al archivo de encabezado de aplicación:

    <dl> CREATEPROCESS \_ MANIFEST RESOURCE ID RT MANIFEST \_ \_ \_ "YourApp.exe.manifest"  
    </dl>

    Como alternativa, puede colocar un archivo de manifiesto independiente en el mismo directorio que el archivo ejecutable de la aplicación. El sistema operativo carga primero el manifiesto desde el sistema de archivos y, a continuación, comprueba la sección de recursos del ejecutable. La versión del sistema de archivos tiene prioridad.

6.  [Los ensamblados compartidos](/windows/desktop/Msi/shared-assemblies) deben instalarse con [la versión Windows Installer](../msi/windows-installer-portal.md) 2.0. Cree un paquete Windows Installer como se describe en [How Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)(Cómo instalar ensamblados Win32 para compartir en paralelo en Windows XP? .
7.  [Los ensamblados privados](/windows/desktop/Msi/private-assemblies) se pueden instalar mediante la [Windows installer](../msi/windows-installer-portal.md) versión 2.0. Cree un paquete Windows Installer como se describe en [How Do I Install Win32 Assemblies for the Private Use of an Application on Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)(Cómo instalar ensamblados Win32 para el uso privado de una aplicación en Windows XP? . También puede usar cualquier otro instalador para copiar un ensamblado privado y su manifiesto en la misma carpeta que el archivo ejecutable de la aplicación.
8.  Pruebe la aplicación para garantizar los resultados. Tenga en cuenta que el equipo de prueba no debe tener registrado el ensamblado en paralelo.
9.  Implemente la aplicación o actualice como un paquete Windows instalador.

## <a name="example-application-manifest"></a>Manifiesto de aplicación de ejemplo

A continuación se muestra un ejemplo de un manifiesto de aplicación:

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

 

 
