---
description: En Windows XP, la configuración por aplicación invalida la configuración predeterminada y la configuración del publicador por aplicación.
ms.assetid: 5b55d12d-8805-4820-91af-5ef583de3463
title: Configuración por aplicación en Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6fa2e14e24e48be84247a23feecddf2784fbc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912513"
---
# <a name="per-application-configuration-on-windows-xp"></a>Configuración por aplicación en Windows XP

En Windows XP, la configuración por aplicación invalida la configuración [predeterminada](default-configuration.md) y la [configuración del publicador](publisher-configuration.md) por aplicación. Esto redirige la dependencia de una aplicación específica de una versión de un ensamblado simultáneo a otra versión especificada del ensamblado.

> [!Note]  
> A partir de Windows Server 2003, la configuración por aplicación invalida la [configuración del publicador](publisher-configuration.md) por aplicación solo si el archivo de [configuración](application-configuration-files.md) de la aplicación especifica *Apply = "no"* en **publisherPolicy** y existe una entrada correspondiente en la base de datos de compatibilidad de aplicaciones. La configuración por aplicación siempre invalida la [configuración predeterminada](default-configuration.md). Para obtener información [, consulte Configuración por aplicación](per-application-configuration.md).

 

Una configuración por aplicación puede ser necesaria si la operación correcta de una aplicación determinada requiere una versión de ensamblado diferente de la versión especificada normalmente como configuración predeterminada o de publicador. Por ejemplo, una actualización global de la versión de ensamblado por parte del publicador podría corregir el ensamblado, pero interrumpir esta aplicación concreta. En este caso, la configuración por aplicación podría usarse para permitir que la aplicación se siga ejecutando con la versión anterior del ensamblado. Otro ejemplo: una instalación Service Pack que contiene una actualización de ensamblado podría usar la [configuración del publicador](publisher-configuration.md) para redirigir las dependencias de todas las aplicaciones y ensamblados del sistema de la versión 1.0.0.0 a la 1.0.1.0. Si hay una aplicación que requiere que la versión 1.0.0.0 funcione correctamente, se puede redirigir a la versión 1.0.0.0 mediante la configuración por aplicación.

Los administradores de aplicaciones pueden implementar una configuración por aplicación mediante la creación e instalación de [archivos de configuración](application-configuration-files.md)de la aplicación. Estas redirigen una aplicación específica de dependencia en una versión de un ensamblado en paralelo para depender de otra versión. Los archivos de [*configuración*](/windows/desktop/Msi/a-gly) de la aplicación pueden invalidar [los archivos de configuración del publicador](publisher-configuration-files.md) y la configuración predeterminada especificada por los [manifiestos de aplicación](application-manifests.md) y los [manifiestos de ensamblado](assembly-manifests.md). El archivo de configuración de la aplicación incluye información utilizada por el cargador cuando se llama a [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

Para configurar una aplicación para que invalide el manifiesto de aplicación y la configuración del publicador, un desarrollador debe crear un archivo de configuración de la aplicación. El archivo de configuración de la aplicación se implementa e instala en la misma carpeta que el archivo ejecutable de la aplicación. Para obtener una lista del esquema de archivo, consulte [esquema del archivo de configuración](application-configuration-file-schema.md)de la aplicación.

Tenga en cuenta que si la aplicación usa la configuración por aplicación, no recibirá ninguna corrección de seguridad o corrección de errores importantes. es posible que el publicador del ensamblado emita como archivos de configuración del publicador. Por tanto, una aplicación que utiliza la configuración por aplicación puede seguir funcionando de forma incorrecta incluso después de que se aplique al sistema un nuevo ensamblado con estas correcciones. Por esta razón, los desarrolladores de aplicaciones nunca deben enviar una aplicación con una configuración por aplicación. La configuración por aplicación solo la deben usar los administradores corporativos como una solución temporal cuando la aplicación está interrumpida por una configuración de publicador. En este caso, la solución permanente es que los desarrolladores del ensamblado y los desarrolladores de la aplicación deberán trabajar juntos para asegurarse de que los ensamblados con la configuración del publicador sean totalmente compatibles con las versiones anteriores.

El siguiente es un ejemplo de un archivo de configuración de la aplicación. Para obtener más información, vea [archivos de configuración](application-configuration-files.md)de la aplicación.

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

 

 
