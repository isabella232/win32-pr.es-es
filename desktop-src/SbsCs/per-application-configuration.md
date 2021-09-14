---
description: La configuración por aplicación redirige la dependencia de una aplicación determinada de una versión de un ensamblado en paralelo a otra versión del ensamblado.
ms.assetid: b7988385-c87e-443c-8ec3-84ab3c172eab
title: Configuración por aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17543c9972deefe2a2beda1f5eeba1c5ace2ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071343"
---
# <a name="per-application-configuration"></a>Configuración por aplicación

La configuración por aplicación redirige la dependencia de una aplicación determinada de una versión de un ensamblado en paralelo a otra versión del ensamblado. Una configuración por aplicación puede ser necesaria si el funcionamiento correcto de una aplicación determinada requiere [](default-configuration.md) una versión de ensamblado diferente de la versión especificada normalmente como configuración predeterminada o configuración del [publicador](publisher-configuration.md). Por ejemplo, una actualización global de la versión del ensamblado por parte del publicador podría corregir el ensamblado, pero interrumpir esta aplicación en particular. En este caso, se podría usar la configuración por aplicación para permitir que la aplicación continúe funcionando con la versión anterior del ensamblado.

A partir Windows Server 2003, la configuración por [](default-configuration.md) aplicación siempre invalida la configuración predeterminada por aplicación. La configuración por [](publisher-configuration.md) aplicación invalida la configuración del publicador por aplicación solo si el archivo de configuración de la aplicación especifica *apply="no"* en **publisherPolicy** y hay una entrada correspondiente en la base de datos de compatibilidad de aplicaciones. [](application-configuration-files.md)

> [!Note]  
> En Windows XP, la configuración por aplicación [](default-configuration.md) invalida la configuración predeterminada y la configuración del [publicador](publisher-configuration.md) por aplicación. Para obtener información, [vea Configuración por aplicación en Windows XP.](per-application-configuration-on-windows-xp.md)

 

[A](publisher-configuration.md) partir de Windows Server 2003, una configuración por aplicación [](application-configuration-files.md) invalidará una configuración del publicador si el archivo de configuración de la aplicación especifica *apply="yes"* en **publisherPolicy** y la marca EnableAppConfig se establece para la aplicación en la base de datos de compatibilidad de aplicaciones. Esta funcionalidad para invalidar una configuración del publicador mediante una configuración por aplicación permite que la aplicación se ejecute en Safemode. Para obtener más información sobre la base de datos de compatibilidad de aplicaciones y Safemode, vea el Windows compatibilidad de aplicaciones Toolkit. Puede obtener el Windows compatibilidad de Toolkit de [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) .

> [!Note]  
> Si envía componentes con un archivo de configuración de aplicación [(archivo](application-configuration-files.md) .config) que especifica *apply="no"* en **publisherPolicy**, se producirá un error en la generación del contexto de activación. La configuración por aplicación se omitirá si envía componentes con un archivo .config *especificando apply="yes"* en **publisherPolicy**.

 

Los administradores de aplicaciones pueden implementar una configuración por aplicación mediante la creación e instalación de archivos de configuración de aplicaciones y la actualización de la base de datos de compatibilidad de aplicaciones. A continuación, el archivo de configuración de la aplicación debe implementarse e instalarse en la misma carpeta que el archivo ejecutable de la aplicación. Para obtener una lista del esquema de archivo, vea [Esquema del archivo de configuración de la aplicación](application-configuration-file-schema.md). La base de datos de compatibilidad de aplicaciones debe distribuirse como se describe en el cuadro de Toolkit.

> [!Note]  
> Si la aplicación se ejecuta en Safemode, no recibirá ninguna corrección de seguridad o corrección de errores importante que el publicador del ensamblado pueda emitir como archivos de configuración del publicador. Por lo tanto, una aplicación que usa la configuración por aplicación puede permanecer insegura o seguir funcionando incorrectamente incluso después de que se aplique un nuevo ensamblado con estas correcciones al sistema. Por esta razón, los desarrolladores de aplicaciones nunca deben enviar una aplicación con una configuración por aplicación. La configuración por aplicación solo la deben usar los administradores corporativos como una corrección temporal cuando una configuración del publicador divide la aplicación. En este caso, la solución permanente es que los desarrolladores del ensamblado y los desarrolladores de la aplicación tendrán que trabajar juntos para asegurarse de que los ensamblados con la configuración del publicador sean totalmente compatibles con versiones anteriores.

 

A continuación se muestra un ejemplo de un archivo de configuración de la aplicación. Para obtener más información, vea Archivos de configuración de aplicaciones.

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

El administrador de la aplicación debe agregar las entradas necesarias a la base de datos de compatibilidad de aplicaciones. Descargue e instale el Windows compatibilidad de Toolkit 2.6 desde [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) . Cree una nueva base de datos personalizada o actualice la existente mediante el administrador de compatibilidad, tal como se describe en el kit de herramientas. La corrección de compatibilidad que quiere elegir para la capa de compatibilidad de la aplicación es EnableAppConfig. Siempre debe probar las aplicaciones antes de instalar una nueva base de datos de compatibilidad.

 

 



