---
description: Un administrador puede usar los métodos siguientes para permitir que un usuario que no es administrador instale una aplicación con privilegios elevados del sistema.
ms.assetid: 61b9297e-f45e-4f50-9001-9bae580e1bf4
title: Instalación de un paquete con privilegios elevados para un usuario que no es administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81de333d6ca388017e03c96f739d7bd258a7c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072057"
---
# <a name="installing-a-package-with-elevated-privileges-for-a-non-admin"></a>Instalación de un paquete con privilegios elevados para un usuario que no es administrador

Un administrador puede usar los métodos siguientes para permitir que un usuario que no es administrador instale una aplicación con privilegios elevados del sistema.

-   En Windows Vista con Windows Installer, un miembro del grupo Administradores puede proporcionar autorización para que un usuario que no sea administrador eleve la instalación a través del [*Control*](u-gly.md) de cuentas de usuario (UAC), tal como se describe en Uso del instalador de Windows con [UAC](using-windows-installer-with-uac.md).

    **Windows Vista:** Obligatorio.

Los métodos siguientes también se pueden usar para instalar una aplicación con privilegios elevados del sistema.

-   Un administrador puede anunciar una aplicación en el equipo de un usuario mediante la asignación o publicación del paquete Windows Installer mediante la implementación de la [aplicación directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page). El administrador anuncia el paquete para la instalación por máquina. Si un usuario que no es administrador instala la aplicación, la instalación se puede ejecutar con privilegios elevados. Los usuarios que no son administradores no pueden instalar paquetes sin invertir que requieran privilegios elevados del sistema.
-   Un administrador puede ir al equipo del usuario y [anunciar la](advertisement.md) aplicación para la instalación por equipo. Dado que el instalador de Windows siempre tiene privilegios elevados mientras se instala en el contexto de instalación por equipo [,](installation-context.md)si un usuario que no es administrador instala la aplicación anunciada, la instalación puede ejecutarse con privilegios elevados. Los usuarios que no son administradores todavía no pueden instalar paquetes sin invertir que requieren privilegios elevados.
-   Un usuario sin privilegios puede instalar una aplicación anunciada que requiere privilegios elevados si un agente del sistema local anuncia la aplicación. La aplicación se puede anunciar para una instalación por usuario o por equipo. Una aplicación instalada con este método se considera administrada. Para obtener más información, vea [Advertising a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).
-   Un administrador puede establecer la [directiva AlwaysInstallElevated](alwaysinstallelevated.md) para instalaciones por usuario y por máquina. Este método puede abrir un equipo con un riesgo de seguridad, ya que cuando se establece esta directiva, un usuario que no es administrador puede ejecutar instalaciones con privilegios elevados y acceder a ubicaciones seguras en el equipo, como SystemFolder o la clave del Registro **HKLM.**

    Si la aplicación se instala por máquina mientras se establece la [directiva AlwaysInstallElevated,](alwaysinstallelevated.md) el producto se trata como administrado. En este caso, la aplicación todavía puede realizar una reparación con privilegios elevados si se quita la directiva. Además, si la aplicación se instala por usuario mientras se establece la directiva AlwaysInstallElevated, la aplicación no puede realizar una reparación si se quita la directiva.

-   Un administrador puede ir al equipo de un usuario y realizar una instalación por equipo de la aplicación. Dado que se requieren privilegios para realizar este tipo de instalación, siempre se administran las instalaciones por máquina.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contexto de instalación](installation-context.md)
</dt> </dl>

 

 
