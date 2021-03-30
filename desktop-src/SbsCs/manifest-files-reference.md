---
description: Los ensamblados en paralelo se usan con los siguientes tipos de archivos de manifiesto y de configuración. Los manifiestos y las configuraciones son archivos XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Referencia de archivos de manifiesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154097"
---
# <a name="manifest-files-reference"></a>Referencia de archivos de manifiesto

Los ensamblados en paralelo se usan con los siguientes tipos de archivos de manifiesto y de configuración. Los manifiestos y las configuraciones son archivos XML.



| de manifiesto                                                               | Descripción                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manifiestos de ensamblado](assembly-manifests.md)                           | Describe los nombres, las versiones, los recursos y las dependencias de ensamblado de los ensamblados en paralelo.                                                                                                               |
| [Manifiestos de aplicación](application-manifests.md)                     | Describe los nombres y las versiones de los ensamblados en paralelo compartidos a los que se debe enlazar la aplicación en tiempo de ejecución y también pueden contener metadatos para ensamblados en paralelo privados usados por la aplicación. |
| [Archivos de configuración de la aplicación](application-configuration-files.md) | Redirige las versiones de ensamblado de las dependencias de ensamblado mediante [la configuración por aplicación](per-application-configuration.md).                                                                            |
| [Archivos de configuración del publicador](publisher-configuration-files.md)     | Redirige las versiones de ensamblado de dependencias de ensamblado por ensamblado mediante una [configuración de publicador](publisher-configuration.md).                                                              |



 

Para obtener una lista del esquema del archivo de manifiesto, consulte [esquema del archivo de manifiesto](manifest-file-schema.md).

Para obtener una lista del esquema del archivo de configuración de la aplicación, consulte [esquema del archivo de configuración](application-configuration-file-schema.md)de la aplicación.

Para obtener una lista del esquema del archivo de configuración del publicador, consulte [esquema del archivo de configuración del publicador](publisher-configuration-file-schema.md).

Otras tecnologías amplían el formato utilizado por los manifiestos de configuración y control de versiones de Windows. Los desarrolladores deben consultar la documentación específica de la tecnología que se usa para obtener información sobre el formato del manifiesto. Por ejemplo:

-   [ClickOnce](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [Common Language Runtime](/dotnet/standard/clr)
-   [Control de cuentas de usuario [UAC]](/previous-versions/bb756929(v=msdn.10))

 

 
