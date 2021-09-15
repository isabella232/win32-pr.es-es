---
description: Los ensamblados en paralelo se usan con los siguientes tipos de archivos de manifiesto y configuración. Los manifiestos y las configuraciones son archivos XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Referencia de archivos de manifiesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271487"
---
# <a name="manifest-files-reference"></a>Referencia de archivos de manifiesto

Los ensamblados en paralelo se usan con los siguientes tipos de archivos de manifiesto y configuración. Los manifiestos y las configuraciones son archivos XML.



| Manifest                                                               | Descripción                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manifiestos de ensamblado](assembly-manifests.md)                           | Describe los nombres, las versiones, los recursos y las dependencias de ensamblado de los ensamblados en paralelo.                                                                                                               |
| [Manifiestos de aplicación](application-manifests.md)                     | Describe los nombres y versiones de los ensamblados en paralelo compartidos a los que la aplicación debe enlazarse en tiempo de ejecución y también puede contener metadatos para ensamblados en paralelo privados utilizados por la aplicación. |
| [Archivos de configuración de la aplicación](application-configuration-files.md) | Redirige las versiones de ensamblado de las dependencias de ensamblado mediante [la configuración por aplicación](per-application-configuration.md).                                                                            |
| [Publisher Archivos de configuración](publisher-configuration-files.md)     | Redirige las versiones de ensamblado de las dependencias de ensamblado por ensamblado mediante una configuración [del publicador](publisher-configuration.md).                                                              |



 

Para obtener una lista del esquema del archivo de manifiesto, vea [Esquema de archivo de manifiesto.](manifest-file-schema.md)

Para obtener una lista del esquema del archivo de configuración de la aplicación, vea [Esquema del archivo de configuración de la aplicación](application-configuration-file-schema.md).

Para obtener una lista del esquema del archivo de configuración del publicador, [vea Publisher de archivo de configuración .](publisher-configuration-file-schema.md)

Otras tecnologías amplían el formato utilizado por Windows control de versiones y manifiestos de configuración. Los desarrolladores deben consultar la documentación específica de la tecnología que se usa para obtener información sobre el formato del manifiesto. Por ejemplo:

-   [ClickOnce](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [Common Language Runtime](/dotnet/standard/clr)
-   [Control de cuentas de usuario [UAC]](/previous-versions/bb756929(v=msdn.10))

 

 
