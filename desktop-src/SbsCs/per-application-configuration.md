---
description: La configuración por aplicación redirige la dependencia de una aplicación determinada de una versión de un ensamblado simultáneo a otra versión del ensamblado.
ms.assetid: b7988385-c87e-443c-8ec3-84ab3c172eab
title: Configuración por aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17543c9972deefe2a2beda1f5eeba1c5ace2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278601"
---
# <a name="per-application-configuration"></a>Configuración por aplicación

La configuración por aplicación redirige la dependencia de una aplicación determinada de una versión de un ensamblado simultáneo a otra versión del ensamblado. Una configuración por aplicación puede ser necesaria si la operación correcta de una aplicación determinada requiere una versión de ensamblado diferente de la versión especificada normalmente como configuración [predeterminada](default-configuration.md) o configuración del [publicador](publisher-configuration.md). Por ejemplo, una actualización global de la versión de ensamblado por parte del publicador podría corregir el ensamblado, pero interrumpir esta aplicación concreta. En este caso, la configuración por aplicación podría usarse para permitir que la aplicación se siga ejecutando con la versión anterior del ensamblado.

A partir de Windows Server 2003, la configuración por aplicación siempre invalida la [configuración predeterminada](default-configuration.md) en función de cada aplicación. La configuración por aplicación invalida la [configuración del publicador](publisher-configuration.md) por aplicación solo si el [archivo de configuración](application-configuration-files.md) de la aplicación especifica *Apply = "no"* en **publisherPolicy** y existe una entrada correspondiente en la base de datos de compatibilidad de aplicaciones.

> [!Note]  
> En Windows XP, la configuración por aplicación invalida la configuración [predeterminada](default-configuration.md) y la [configuración del publicador](publisher-configuration.md) por aplicación. Para obtener más información, consulte [configuración por aplicación en Windows XP](per-application-configuration-on-windows-xp.md).

 

A partir de Windows Server 2003, una configuración por aplicación invalidará [una configuración de publicador](publisher-configuration.md) si el [archivo de configuración](application-configuration-files.md) de la aplicación especifica *Apply = "Yes"* en **publisherPolicy** y se establece la marca EnableAppConfig para la aplicación en la base de datos de compatibilidad de aplicaciones. Esta capacidad de invalidar una configuración de publicador mediante una configuración por aplicación permite que la aplicación se ejecute en modo SafeMode. Para obtener más información sobre la base de datos de compatibilidad de aplicaciones y SafeMode, vea el kit de herramientas de compatibilidad de aplicaciones de Windows. Puede obtener el kit de herramientas de compatibilidad de aplicaciones de Windows de [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) .

> [!Note]  
> Si envía componentes con un [archivo de configuración](application-configuration-files.md) de la aplicación (archivo. config) que especifica *Apply = "no"* en **publisherPolicy**, se producirá un error en la generación del contexto de activación. La configuración por aplicación se omitirá si se entregan los componentes con un archivo. config que especifique *Apply = "Yes"* en **publisherPolicy**.

 

Los administradores de aplicaciones pueden implementar una configuración por aplicación mediante la creación e instalación de archivos de configuración de la aplicación y la actualización de la base de datos de compatibilidad de aplicaciones. El archivo de configuración de la aplicación se debe implementar e instalar en la misma carpeta que el archivo ejecutable de la aplicación. Para obtener una lista del esquema de archivo, consulte [esquema del archivo de configuración](application-configuration-file-schema.md)de la aplicación. La base de datos de compatibilidad de aplicaciones debe distribuirse tal y como se describe en el kit de herramientas de compatibilidad de aplicaciones.

> [!Note]  
> Si la aplicación se ejecuta en modo SafeMode, no recibirá ninguna corrección de seguridad o corrección de errores importantes. es posible que el publicador del ensamblado emita como archivos de configuración del publicador. Por tanto, una aplicación que utiliza la configuración por aplicación puede seguir funcionando de forma incorrecta incluso después de que se aplique al sistema un nuevo ensamblado con estas correcciones. Por esta razón, los desarrolladores de aplicaciones nunca deben enviar una aplicación con una configuración por aplicación. La configuración por aplicación solo la deben usar los administradores corporativos como una solución temporal cuando la aplicación está interrumpida por una configuración de publicador. En este caso, la solución permanente es que los desarrolladores del ensamblado y los desarrolladores de la aplicación deberán trabajar juntos para asegurarse de que los ensamblados con la configuración del publicador sean totalmente compatibles con las versiones anteriores.

 

El siguiente es un ejemplo de un archivo de configuración de la aplicación. Para obtener más información, vea archivos de configuración de la aplicación.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
 <windows>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity  processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
   <publisherPolicy apply="no"/>                     
   <dependentAssembly>
    <assemblyIdentity type="win32" processorArchitecture="x86" name="Microsoft.Windows.SampleAssembly" publicKeyToken="0000000000000000"/>
    <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
   </dependentAssembly>
  </assemblyBinding>
 </windows>
</configuration>
```

El administrador de la aplicación debe agregar las entradas necesarias a la base de datos de compatibilidad de aplicaciones. Descargue e instale el kit de herramientas de compatibilidad de aplicaciones de Windows 2,6 de [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) . Cree un nuevo personalizado o actualice la base de datos existente con el administrador de compatibilidad tal y como se describe en el kit de herramientas. La corrección de compatibilidad que desea elegir para la capa de compatibilidad de la aplicación es EnableAppConfig. Siempre debe probar las aplicaciones antes de instalar una nueva base de datos de compatibilidad.

 

 



