---
description: Modo protegido
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Modo protegido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2f16b9f923215af6c2211339859d8eab4803e6793be248a83760e298ed084c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994785"
---
# <a name="protected-mode"></a>Modo protegido

La mayoría Windows Internet Explorer 8 características de seguridad están disponibles en Internet Explorer 8 para el sistema operativo Windows XP con Service Pack 2 (SP2) y versiones posteriores. El modo protegido solo está disponible para Windows Vista o versiones posteriores, ya que se basa en las siguientes características de seguridad que son nuevas en Windows Vista:

-   [El control de cuentas de usuario (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) facilita la ejecución sin privilegios de administrador. Cuando los usuarios ejecutan programas con privilegios de usuario limitados, son más seguros de un ataque que cuando se ejecutan con privilegios de administrador. El Windows operativo puede impedir que el código malintencionado lleve a cabo acciones perjudiciales.
-   Un mecanismo de integridad [](../secauthz/securable-objects.md) restringe el acceso de escritura a objetos protegibles mediante procesos de menor integridad, de la misma manera que la pertenencia a grupos de cuentas de usuario restringe los derechos de los usuarios para acceder a componentes confidenciales del sistema.
-   [Interfaz de usuario aislamiento de privilegios de usuario (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) impide que los procesos envíen mensajes de ventana seleccionados y otras API DE USUARIO a procesos que se ejecutan con mayor integridad.

La infraestructura de seguridad del mecanismo de integridad de Windows permite que el modo protegido proporcione a Windows Internet Explorer los privilegios que los usuarios necesitan para examinar la Web, al tiempo que se retienen los privilegios que los usuarios necesitan para instalar programas en modo silencioso o modificar datos confidenciales del sistema.

Los usuarios pueden deshabilitar esta característica mediante una casilla y los administradores pueden deshabilitarla mediante directiva de grupo.

> [!IMPORTANT]
> Debe deshabilitar la característica solo como medida temporal durante la solución de problemas para comparar el comportamiento de la aplicación cuando la característica está habilitada o no. Se recomienda mantener esta característica habilitada permanentemente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
