---
description: .
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Modo protegido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace82e27bbec3bb97a9ffbd3b64c9c6cee9e11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910585"
---
# <a name="protected-mode"></a>Modo protegido

La mayoría de las características de seguridad de Windows Internet Explorer 8 están disponibles en Internet Explorer 8 para el sistema operativo Windows XP con Service Pack 2 (SP2) y versiones posteriores. El modo protegido solo está disponible para Windows Vista o versiones posteriores, ya que se basa en las siguientes características de seguridad que son nuevas en Windows Vista:

-   [Control de cuentas de usuario (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) facilita la ejecución sin privilegios de administrador. Cuando los usuarios ejecutan programas con privilegios de usuario limitados, son más seguros de un ataque que cuando se ejecutan con privilegios de administrador. El sistema operativo Windows puede impedir que el código malintencionado lleve a cabo acciones dañinas.
-   Un mecanismo de integridad restringe el acceso de escritura a los [objetos protegibles](../secauthz/securable-objects.md) mediante procesos de menor integridad, del mismo modo que la pertenencia al grupo de cuentas de usuario restringe los derechos de los usuarios para tener acceso a componentes confidenciales del sistema.
-   El [aislamiento de privilegios de interfaz de usuario (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) impide que los procesos envíen mensajes de ventana seleccionados y otras API de usuario a los procesos que se ejecutan con mayor integridad.

La infraestructura de seguridad del mecanismo de integridad de Windows permite que el modo protegido proporcione a Windows Internet Explorer los privilegios que los usuarios necesitan para explorar la web, a la vez que conserva los privilegios que los usuarios necesitan para instalar programas de forma silenciosa o modificar los datos confidenciales del sistema.

Los usuarios pueden deshabilitar esta característica mediante una casilla y los administradores pueden deshabilitarla mediante directiva de grupo.

> [!IMPORTANT]
> Solo debe deshabilitar la característica como medida temporal durante la solución de problemas para comparar el comportamiento de la aplicación cuando la característica está habilitada o no. Se recomienda mantener esta característica habilitada de forma permanente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
