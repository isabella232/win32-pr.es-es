---
description: Las aplicaciones aisladas son aplicaciones autodescriptas instaladas con manifiestos. Las aplicaciones aisladas pueden usar ensamblados privados y ensamblados compartidos.
ms.assetid: 66c65b92-7c49-4932-b8c5-91b20fb0a038
title: Aplicaciones aisladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10c1b3f175ec05751bfc84e3826b19c9c9db01f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271503"
---
# <a name="isolated-applications"></a>Aplicaciones aisladas

Las aplicaciones aisladas son aplicaciones autodescriptas instaladas con [manifiestos](manifests.md). Las aplicaciones aisladas pueden usar [ensamblados privados y](/windows/desktop/Msi/private-assemblies) [ensamblados compartidos.](/windows/desktop/Msi/shared-assemblies)

Una aplicación se considera completamente aislada si todos sus componentes son ensamblados en paralelo compartidos [o](about-side-by-side-assemblies-.md) ensamblados privados. Se llama parcialmente aislado si usa algunos componentes que no son ensamblados en paralelo. Tenga en cuenta que si una aplicación usa algunos componentes que no son ensamblados en paralelo o usa ensamblados privados, la aplicación puede verse afectada por la instalación o eliminación de otras aplicaciones en el sistema. Para obtener más información, vea Uso compartido [de ensamblados en paralelo.](side-by-side-assembly-sharing.md)

Se recomienda a los desarrolladores que diseñen aplicaciones aisladas y actualicen las aplicaciones existentes en aplicaciones aisladas por los siguientes motivos:

-   Las aplicaciones aisladas son más estables y se actualizan de forma confiable porque no se ven afectadas por la instalación, eliminación o actualización de otras aplicaciones en el sistema.
-   Las aplicaciones aisladas se pueden diseñar para que siempre se ejecuten con las mismas versiones de ensamblado con las que se crearon y probaron.
-   Las aplicaciones aisladas pueden usar la funcionalidad proporcionada por los ensamblados en paralelo disponibles por Microsoft. Para obtener más información, [vea Supported Microsoft side-by-side Assemblies ( Ensamblados en paralelo de Microsoft admitidos).](supported-microsoft-side-by-side-assemblies.md)
-   Las aplicaciones aisladas no están vinculadas a la programación de envío de sus ensamblados en paralelo porque las aplicaciones y los administradores pueden actualizar la configuración después de la implementación sin tener que volver a instalar la aplicación. Esto no se aplicaría en el caso de que solo esté disponible una versión del ensamblado.
-   Se puede instalar una aplicación completamente aislada mediante el **comando xcopy.** [Windows Installer](../msi/windows-installer-portal.md) también se puede usar para instalar una aplicación aislada sin afectar al Registro. Para obtener más información, [vea Instalación de ensamblados Win32.](../msi/installation-of-win32-assemblies.md)

En algunos casos, las aplicaciones existentes se pueden actualizar en una aplicación aislada sin tener que volver a escribir el código de la aplicación. Se [puede crear un](application-manifests.md) manifiesto de aplicación que describa las dependencias de la aplicación en [ensamblados en paralelo.](about-side-by-side-assemblies-.md) Si la aplicación usa componentes que no son ensamblados en paralelo, estos se pueden implementar como [ensamblados privados.](/windows/desktop/Msi/private-assemblies) Tenga en cuenta que la posibilidad de hacerlo con componentes de terceros puede depender de la concesión de licencias, ya que el componente tendrá que crearse como un ensamblado. Por ejemplo, mediante la creación de un manifiesto de aplicación y la especificación de una dependencia de los controles comunes en paralelo (COMCTL32), una aplicación que se ejecuta en Windows XP puede aprovechar las ventajas de Windows con el formato *.* Siempre debe probar la aplicación para asegurarse de que es compatible con la nueva versión del ensamblado COMCTL32.

Es posible que no sea posible actualizar todas las aplicaciones existentes en una aplicación completamente aislada. Por ejemplo, algunos ensamblados del sistema Windows [File Protection (WFP)](/windows/desktop/Wfp/windows-resource-protection-portal) no están disponibles como ensamblados en paralelo y no se pueden instalar con la aplicación como ensamblado privado. Es posible aislar parcialmente estas aplicaciones mediante la especificación de dependencias de ensamblado en paralelo para algunos de los ensamblados de la aplicación en un manifiesto de aplicación.

 

 
