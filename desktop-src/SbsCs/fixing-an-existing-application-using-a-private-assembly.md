---
description: A partir de Windows XP, puede crear un ensamblado privado y hacer que esté disponible para una aplicación específica.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Corregir una aplicación existente mediante un ensamblado privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082062"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a>Corregir una aplicación existente mediante un ensamblado privado

A partir de Windows XP, puede crear un ensamblado privado y hacer que esté disponible para una aplicación específica. Esta capacidad se puede utilizar para corregir una aplicación que es incompatible con una actualización. Un ejemplo sería una aplicación que sea incompatible con la versión más reciente de MSVCRT.DLL después de actualizar el sistema operativo. En este caso, no tiene la opción de reemplazar la versión del sistema porque MSVCRT.DLL es un archivo protegido de Windows. En lugar de tener que volver a escribir la aplicación para que funcione con la nueva versión de MSVCRT, puede crear un ensamblado privado para MSVCRT e instalarlo en la carpeta de la aplicación. Tenga en cuenta que no todos los componentes compartidos son un candidato adecuado para un ensamblado en paralelo privado y algunos componentes tienen restricciones de licencia sobre dónde se pueden instalar sus componentes. El componente debe cumplir los criterios de un componente en paralelo. Pregunte al publicador del componente si puede proporcionar un ensamblado adecuado.

El manifiesto del ensamblado privado y el manifiesto de la aplicación deben instalarse en la misma carpeta que el ejecutable de la aplicación. Cuando se ejecuta la aplicación, consulta el manifiesto de aplicación y carga la versión de MSVCRT que es privada para la aplicación.

En este ejemplo, el ensamblado privado incluiría MSVCRT.DLL y MSVCIRT.DLL como en el siguiente manifiesto del ensamblado:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

El siguiente es un ejemplo de un posible manifiesto de aplicación.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



