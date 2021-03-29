---
description: Un administrador puede usar los métodos siguientes para permitir que un usuario que no sea administrador Instale una aplicación con privilegios del sistema elevados.
ms.assetid: 61b9297e-f45e-4f50-9001-9bae580e1bf4
title: Instalación de un paquete con privilegios elevados para un no administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81de333d6ca388017e03c96f739d7bd258a7c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912845"
---
# <a name="installing-a-package-with-elevated-privileges-for-a-non-admin"></a>Instalación de un paquete con privilegios elevados para un no administrador

Un administrador puede usar los métodos siguientes para permitir que un usuario que no sea administrador Instale una aplicación con privilegios del sistema elevados.

-   En Windows Vista con Windows Installer, un miembro del grupo administradores puede proporcionar autorización a un usuario que no sea administrador para elevar la instalación a través del [*control de cuentas de usuario*](u-gly.md) (UAC), tal como se describe en uso de [Windows Installer con UAC](using-windows-installer-with-uac.md).

    **Windows Vista:** Obligatorio.

También se pueden usar los métodos siguientes para instalar una aplicación con privilegios del sistema elevados.

-   Un administrador puede anunciar una aplicación en el equipo de un usuario asignando o publicando el paquete de Windows Installer mediante la implementación de la aplicación y [Directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page). El administrador anuncia el paquete para la instalación por equipo. Si un usuario que no es administrador instala la aplicación, la instalación se puede ejecutar con privilegios elevados. Los usuarios que no son administradores no pueden instalar paquetes sin anunciar que requieran privilegios elevados del sistema.
-   Un administrador puede ir al equipo del usuario y [anunciar](advertisement.md) la aplicación para la instalación por equipo. Dado que el Windows Installer siempre tiene privilegios elevados mientras se instala en el contexto de [instalación](installation-context.md)por máquina, si un usuario que no es administrador instala entonces la aplicación anunciada, la instalación se puede ejecutar con privilegios elevados. Los usuarios que no son administradores todavía no pueden instalar paquetes sin anunciar que requieran privilegios elevados.
-   Un usuario sin privilegios puede instalar una aplicación anunciada que requiera privilegios elevados si un agente del sistema local anuncia la aplicación. La aplicación se puede anunciar para una instalación por usuario o por equipo. Una aplicación instalada con este método se considera administrada. Para obtener más información, vea [anunciar una aplicación Per-User que se va a instalar con privilegios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).
-   Un administrador puede establecer la directiva [AlwaysInstallElevated](alwaysinstallelevated.md) para las instalaciones por usuario y por equipo. Este método puede abrir un equipo a un riesgo de seguridad, ya que cuando se establece esta Directiva, un usuario que no es administrador puede ejecutar instalaciones con privilegios elevados y tener acceso a ubicaciones seguras en el equipo, como la clave del registro Carpetadelsistema o **HKLM** .

    Si la aplicación se instala por equipo mientras se establece la directiva [AlwaysInstallElevated](alwaysinstallelevated.md) , el producto se trata como administrado. En este caso, la aplicación todavía puede realizar una reparación con privilegios elevados si se quita la Directiva. Además, si la aplicación se instala por usuario mientras se establece la Directiva AlwaysInstallElevated, la aplicación no puede realizar una reparación si se quita la Directiva.

-   Un administrador puede ir al equipo de un usuario y realizar una instalación por equipo de la aplicación. Dado que se requieren privilegios para realizar este tipo de instalación, las instalaciones por equipo siempre se administran.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contexto de instalación](installation-context.md)
</dt> </dl>

 

 
