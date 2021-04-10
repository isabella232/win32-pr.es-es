---
description: Windows Installer cumple con el control de cuentas de usuario (UAC) en Windows Vista.
ms.assetid: 13955ded-6b7f-475f-bb0f-6530a0b4963f
title: Uso de Windows Installer con UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a05dcd2fb33eff24fb17702af1cb306f81002d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155113"
---
# <a name="using-windows-installer-with-uac"></a>Uso de Windows Installer con UAC

Windows Installer cumple con el [*control de cuentas de usuario*](u-gly.md) (UAC) en Windows Vista. Con la autorización de un administrador, el Windows Installer puede instalar aplicaciones o revisiones en nombre de un usuario que no sea miembro del grupo administradores. Esto se conoce como una instalación con [*privilegios elevados*](e-gly.md) porque el Windows Installer realiza cambios en el sistema en nombre del usuario que normalmente no se permitiría si el usuario realizara los cambios directamente.

-   Cuando se usa Windows Vista en un entorno corporativo, las aplicaciones se pueden designar como aplicaciones administradas. Mediante la implementación de la aplicación y el [Directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page), los administradores pueden bloquear directorios y, a continuación, asignar o publicar las aplicaciones administradas en esos directorios a [*los usuarios estándar*](s-gly.md) para su instalación, reparación o eliminación. Las aplicaciones administradas se registran en el subárbol del registro **HKEY \_ local \_ Machine** . Una vez que se ha registrado una aplicación como una aplicación administrada, las operaciones de instalación posteriores siempre se ejecutan con privilegios elevados. Si el usuario se ejecuta como administrador, no se requiere ninguna solicitud para continuar con la instalación. Si el usuario se ejecuta como un usuario estándar y la aplicación ya se ha asignado o publicado, la instalación de la aplicación administrada puede continuar sin preguntar.
-   Al usar Windows Vista en un entorno no corporativo, UAC controla la elevación de la instalación de la aplicación. Windows Installer 4,0 puede llamar al [*servicio de información*](a-gly.md) de la aplicación (AIS) para solicitar la autorización del administrador para elevar una instalación. Antes de que se pueda ejecutar una instalación identificada como que requiere privilegios de administrador, UAC solicita al usuario que dé su consentimiento para elevar la instalación. La solicitud de consentimiento se muestra de forma predeterminada, incluso si el usuario es miembro del grupo local de administradores, ya que los administradores ejecutan como usuarios estándar hasta que una aplicación o un componente del sistema que requiere credenciales administrativas solicita permiso para ejecutarse. Esta experiencia de usuario se denomina [*modo de aprobación de administrador*](a-gly.md) (AAM). Si un usuario estándar intenta instalar la aplicación, el usuario tiene que obtener privilegios de administrador para proporcionarle sus credenciales de administrador para continuar con la instalación. Esta experiencia de usuario se denomina [*a través de la petición de credenciales de hombro*](o-gly.md) (OTS).
-   Dado que UAC restringe los privilegios durante las fases de una instalación, los desarrolladores de Windows Installer paquetes no deben suponer que su instalación siempre tendrá acceso a todas las partes del sistema. Por lo tanto, los desarrolladores de paquetes de Windows Installer deben cumplir las directrices de los paquetes que se describen en las [instrucciones para asegurarse de](guidelines-for-packages.md) que su paquete funciona con UAC y Windows Vista. Un paquete que se ha creado y probado para cumplir con UAC debe contener la propiedad [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) establecida en 1.
-   Un administrador también puede usar los métodos descritos en la sección: [instalar un paquete con privilegios elevados para un usuario que no sea](installing-a-package-with-elevated-privileges-for-a-non-admin.md) de administrador para permitir a un usuario que no sea administrador instalar una aplicación con privilegios del sistema elevados.
-   Los privilegios son necesarios para instalar una aplicación en el contexto administrado por el usuario y, Windows Installer por lo tanto, las reinstalaciones o reparaciones de la aplicación también se realizan mediante el instalador con privilegios elevados. Esto significa que solo se pueden aplicar revisiones de orígenes de confianza a una aplicación en el estado administrado por usuario. A partir de Windows Installer 3,0, puede aplicar una revisión a una aplicación administrada por usuario después de haber registrado la revisión como con privilegios elevados. Para obtener información, consulte [aplicación de revisiones Per-User aplicaciones administradas](patching-per-user-managed-applications.md).

> [!Note]  
> Cuando no se necesitan privilegios elevados para instalar un paquete de Windows Installer, el autor del paquete puede suprimir el cuadro de diálogo que UAC muestra para solicitar autorización de administrador al usuario. Para obtener más información, vea [crear paquetes sin el cuadro de diálogo de UAC](authoring-packages-without-the-uac-dialog-box.md).

 

 

 
