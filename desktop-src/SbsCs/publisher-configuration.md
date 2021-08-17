---
description: Un archivo de configuración del publicador redirige globalmente las aplicaciones y los ensamblados que dependen de una versión de un ensamblado en paralelo para usar otra versión del mismo ensamblado.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Publisher Configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1134fa29775fc34384f5da19e660d91de10532110304caf8b6ecacbb92fec87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141958"
---
# <a name="publisher-configuration"></a>Publisher Configuración

Un [archivo de configuración del](publisher-configuration-files.md) publicador redirige globalmente las aplicaciones y los ensamblados que dependen de una versión de un ensamblado en paralelo para usar otra versión del mismo ensamblado. Esto permite que las aplicaciones y los ensamblados usen el ensamblado actualizado sin tener que volver a generar todas las aplicaciones afectadas.

[Publisher el](publisher-configuration-files.md) publicador de un ensamblado puede proporcionar archivos de configuración al emitir una nueva versión del ensamblado con correcciones de errores o actualizaciones de seguridad compatibles. La versión actualizada debe ser totalmente compatible con versiones anteriores. Nunca se debe usar un archivo de configuración del publicador para agregar nuevas características a menos que la actualización sea totalmente compatible con versiones anteriores. Publisher archivos de configuración no se deben usar nunca para incrementar la versión principal o secundaria de un ensamblado. Por ejemplo, no redirija la versión del ensamblado 6.0.0.0 a 7.0.0.0 o a 6.1.0.0.

Publisher los archivos de configuración solo los debe emitir el publicador del ensamblado. Los desarrolladores de ensamblados deben firmar ensamblados en paralelo compartidos y archivos de configuración del publicador. Use la misma clave para firmar el ensamblado y los archivos de configuración del publicador asociados. Publisher los archivos de configuración deben firmarse con las mismas [](assembly-signing-example.md) herramientas que se usan para los ensamblados, vea Ejemplo de firma de ensamblados y Creación de archivos [y catálogos firmados.](creating-signed-files-and-catalogs.md)

Normalmente, la nueva versión de un ensamblado y el archivo de configuración del publicador asociado se instalarán en una actualización de Service Pack. Publisher archivos de configuración nunca deben proporcionarse con aplicaciones como redistribuibles porque la instalación de un archivo de configuración del publicador redirige globalmente los ensamblados en el sistema. Si el ensamblado que se actualiza se proporciona como redistribuible, el publicador debe proporcionar lo siguiente.

-   Un Windows installer (.msi archivo) que incluye la nueva versión del ensamblado con la configuración del publicador. Esto se puede instalar como Service Pack o QFE porque, en este caso, el cliente ha elegido actualizar globalmente el sistema. Las aplicaciones nunca deben instalar esta versión del paquete.
-   Un Windows de mezcla del instalador (archivo .msm) que solo incluye la nueva versión del ensamblado. Esta versión puede incluirse con las aplicaciones.

Las aplicaciones que requieren una versión mínima del ensamblado deben decir su dependencia en la versión mínima, si la versión mínima no está disponible en un sistema, la aplicación no se iniciará. Si está disponible como redistribuible, debe incluirse en la configuración de la aplicación.

Por ejemplo, la instalación del [siguiente](publisher-configuration-files.md) archivo de configuración del publicador redirige el enlace desde la versión 2.0.0.0 de Microsoft. Windows. SampleAssembly a la versión 2.0.1.0. Esto agrega una nueva directiva, denominada 1.1.0.0.Policy, en %systemDrive% \\ windows \\ winsxs \\ policies \\ x86 \_ policy.2.0.Microsoft.Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *hashvalue*>.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

La instalación del siguiente archivo de configuración del publicador para el mismo ensamblado redirige el enlace desde la versión 2.0.0.0 de Microsoft. Windows. SampleAssembly a la versión 2.0.3.0. Esto agrega otra directiva, denominada 2.1.0.0.Policy, en %systemDrive% \\ \\ windows winsxs \\ policies \\ x86 \_ policy.2.0.Microsoft.Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *hashvalue*>.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



