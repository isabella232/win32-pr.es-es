---
description: En Windows XP, la configuración por aplicación invalida la configuración predeterminada y la configuración del publicador por aplicación.
ms.assetid: 5b55d12d-8805-4820-91af-5ef583de3463
title: Configuración por aplicación en Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6fa2e14e24e48be84247a23feecddf2784fbc6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071347"
---
# <a name="per-application-configuration-on-windows-xp"></a>Configuración por aplicación en Windows XP

En Windows XP, la configuración por aplicación [](default-configuration.md) invalida la configuración predeterminada y la configuración del [publicador](publisher-configuration.md) por aplicación. Esto redirige la dependencia de una aplicación específica de una versión de un ensamblado en paralelo a otra versión especificada del ensamblado.

> [!Note]  
> A partir de Windows Server 2003, la [](publisher-configuration.md) configuración por aplicación invalida la configuración [](application-configuration-files.md) del publicador por aplicación solo si el archivo de configuración de la aplicación especifica *apply="no"* en **publisherPolicy** y hay una entrada correspondiente en la base de datos de compatibilidad de aplicaciones. La configuración por aplicación siempre invalida la [configuración predeterminada.](default-configuration.md) Para obtener información, [vea configuración por aplicación.](per-application-configuration.md)

 

Una configuración por aplicación puede ser necesaria si el funcionamiento correcto de una aplicación determinada requiere una versión de ensamblado diferente de la versión especificada normalmente como configuración predeterminada o de publicador. Por ejemplo, una actualización global de la versión del ensamblado por parte del publicador podría corregir el ensamblado, pero interrumpir esta aplicación en particular. En este caso, se podría usar la configuración por aplicación para permitir que la aplicación continúe funcionando con la versión anterior del ensamblado. Otro ejemplo, una instalación de Service Pack [](publisher-configuration.md) que contiene una actualización de ensamblado podría usar la configuración del publicador para redirigir las dependencias de todas las aplicaciones y ensamblados del sistema de la versión 1.0.0.0 a la 1.0.1.0. Si hay una aplicación que requiere que la versión 1.0.0.0 funcione correctamente, se puede redirigir a la versión 1.0.0.0 mediante la configuración por aplicación.

Los administradores de aplicaciones pueden implementar una configuración por aplicación mediante la creación e instalación de archivos [de configuración de aplicaciones](application-configuration-files.md). Redirigen una aplicación específica de la dependencia de una versión de un ensamblado en paralelo a la dependencia de otra versión. [*Los archivos de configuración*](/windows/desktop/Msi/a-gly) de la aplicación pueden invalidar los archivos [de configuración del publicador](publisher-configuration-files.md) y la configuración predeterminada especificada por [manifiestos de aplicación](application-manifests.md) y [manifiestos de ensamblado.](assembly-manifests.md) El archivo de configuración de la aplicación incluye información que usa el cargador cuando [**se llama a CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Para configurar una aplicación para invalidar el manifiesto de aplicación y la configuración del publicador, un desarrollador debe crear un archivo de configuración de la aplicación. A continuación, el archivo de configuración de la aplicación se implementa e instala en la misma carpeta que el archivo ejecutable de la aplicación. Para obtener una lista del esquema de archivo, vea [Esquema del archivo de configuración de la aplicación](application-configuration-file-schema.md).

Tenga en cuenta que si la aplicación usa la configuración por aplicación, no recibirá ninguna corrección de seguridad o corrección de errores importante que el publicador del ensamblado pueda emitir como archivos de configuración del publicador. Por lo tanto, una aplicación que usa la configuración por aplicación puede permanecer insegura o seguir funcionando incorrectamente incluso después de que se aplique un nuevo ensamblado con estas correcciones al sistema. Por esta razón, los desarrolladores de aplicaciones nunca deben enviar una aplicación con una configuración por aplicación. La configuración por aplicación solo la deben usar los administradores corporativos como una corrección temporal cuando una configuración del publicador divide la aplicación. En este caso, la solución permanente es que los desarrolladores del ensamblado y los desarrolladores de la aplicación tendrán que trabajar juntos para asegurarse de que los ensamblados con la configuración del publicador sean totalmente compatibles con versiones anteriores.

A continuación se muestra un ejemplo de un archivo de configuración de la aplicación. Para obtener más información, vea [Archivos de configuración de aplicaciones](application-configuration-files.md).

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
  <windows>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <assemblyIdentity 
          name="Microsoft.Windows.mysampleApp" 
          processorArchitecture="x86" 
          version="1.0.0.0" type="win32"/>
        <dependentAssembly>
          <assemblyIdentity type="win32" 
              name="Microsoft.Windows.SampleAssembly" 
              processorArchitecture="x86" 
              publicKeyToken="0000000000000000"/>
          <bindingRedirect 
              oldVersion="2.0.0.0" 
              newVersion="2.0.1.0"/>
        </dependentAssembly>
    </assemblyBinding>
   </windows>
</configuration>
```

 

 
