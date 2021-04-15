---
description: Las aplicaciones aisladas son aplicaciones autodescriptivas instaladas con manifiestos. Las aplicaciones aisladas pueden usar ensamblados privados y ensamblados compartidos.
ms.assetid: 66c65b92-7c49-4932-b8c5-91b20fb0a038
title: Aplicaciones aisladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10c1b3f175ec05751bfc84e3826b19c9c9db01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497230"
---
# <a name="isolated-applications"></a>Aplicaciones aisladas

Las aplicaciones aisladas son aplicaciones autodescriptivas instaladas con [manifiestos](manifests.md). Las aplicaciones aisladas pueden usar ensamblados [privados](/windows/desktop/Msi/private-assemblies) y [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies).

Una aplicación se considera totalmente aislada si todos sus componentes son [ensamblados en paralelo](about-side-by-side-assemblies-.md) compartidos o ensamblados privados. Se llama parcialmente aislada si usa algunos componentes que no son ensamblados en paralelo. Tenga en cuenta que si una aplicación usa algunos componentes que no son ensamblados en paralelo, o utiliza ensamblados privados, la aplicación puede verse afectada por la instalación o desinstalación de otras aplicaciones del sistema. Para obtener más información, consulte [uso compartido de ensamblados en paralelo](side-by-side-assembly-sharing.md).

Se recomienda a los desarrolladores diseñar aplicaciones aisladas y actualizar las aplicaciones existentes en aplicaciones aisladas por las siguientes razones:

-   Las aplicaciones aisladas se actualizan de forma más estable y confiable porque no se ven afectadas por la instalación, la eliminación o la actualización de otras aplicaciones en el sistema.
-   Las aplicaciones aisladas se pueden diseñar para que siempre se ejecuten con las mismas versiones de ensamblado con las que se compilaron y probaron.
-   Las aplicaciones aisladas pueden usar la funcionalidad proporcionada por los ensamblados en paralelo que pone a su disposición Microsoft. Para obtener más información, consulte [ensamblados en paralelo de Microsoft compatibles](supported-microsoft-side-by-side-assemblies.md).
-   Las aplicaciones aisladas no están asociadas a la programación de envío de sus ensamblados en paralelo, ya que las aplicaciones y los administradores pueden actualizar la configuración después de la implementación sin tener que volver a instalar la aplicación. Esto no sería aplicable en caso de que solo se esté disponible una versión del ensamblado.
-   Se puede instalar una aplicación totalmente aislada mediante el comando **xcopy** . También se puede usar [Windows Installer](../msi/windows-installer-portal.md) para instalar una aplicación aislada sin que ello afecte al registro. Para obtener más información, vea [instalación de ensamblados Win32](../msi/installation-of-win32-assemblies.md).

En algunos casos, las aplicaciones existentes se pueden actualizar en una aplicación aislada sin tener que volver a escribir el código de la aplicación. Se puede crear un [manifiesto de aplicación](application-manifests.md) que describa las dependencias de la aplicación en [ensamblados en paralelo](about-side-by-side-assemblies-.md). Si la aplicación usa componentes que no son ensamblados en paralelo, se pueden implementar como [ensamblados privados](/windows/desktop/Msi/private-assemblies). Tenga en cuenta que la posibilidad de hacerlo con componentes de terceros puede depender de la concesión de licencias, ya que el componente deberá crearse como un ensamblado. Por ejemplo, mediante la creación de un manifiesto de aplicación y la especificación de una dependencia de los controles comunes en paralelo (COMCTL32), una aplicación que se ejecuta *en Windows XP* puede aprovechar las ventajas de las características de Windows. Siempre debe probar la aplicación para asegurarse de que es compatible con la nueva versión del ensamblado de COMCTL32.

Es posible que no sea posible actualizar todas las aplicaciones existentes en una aplicación totalmente aislada. Por ejemplo, algunos ensamblados del sistema de [protección de archivos de Windows (WFP)](/windows/desktop/Wfp/windows-resource-protection-portal) no están disponibles como ensamblados en paralelo y no se pueden instalar con la aplicación como un ensamblado privado. Puede aislar parcialmente estas aplicaciones mediante la especificación de dependencias de ensamblado en paralelo para algunos de los ensamblados de la aplicación en un manifiesto de aplicación.

 

 
