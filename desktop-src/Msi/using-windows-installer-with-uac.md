---
description: Windows El instalador cumple con el Control de cuentas de usuario (UAC) en Windows Vista.
ms.assetid: 13955ded-6b7f-475f-bb0f-6530a0b4963f
title: Usar Windows instalador con UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458d6265938f44a694366e8145d60aa5d031d47e715932502bd1b82e7012b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942285"
---
# <a name="using-windows-installer-with-uac"></a>Usar Windows instalador con UAC

Windows El instalador cumple con [*el Control de cuentas de*](u-gly.md) usuario (UAC) en Windows Vista. Con la autorización de un administrador, Windows Installer puede instalar aplicaciones o revisiones en nombre de un usuario que no sea miembro del grupo Administradores. Esto se conoce como [](e-gly.md) una instalación con privilegios elevados porque el instalador de Windows realiza cambios en el sistema en nombre del usuario que normalmente no se permitirían si el usuario realizara los cambios directamente.

-   Al usar Windows Vista en un entorno corporativo, las aplicaciones se pueden designar como aplicaciones administradas. Mediante la implementación de aplicaciones [y directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page), los administradores pueden bloquear directorios [](s-gly.md) y, a continuación, asignar o publicar las aplicaciones administradas en esos directorios a los usuarios estándar para su instalación, reparación o eliminación. Las aplicaciones administradas se registran en el subárbol del registro **HKEY \_ LOCAL \_ MACHINE.** Una vez que una aplicación se ha registrado como una aplicación administrada, las operaciones de instalación posteriores siempre se ejecutan con privilegios elevados. Si el usuario se ejecuta como administrador, no se requiere ningún aviso para continuar con la instalación. Si el usuario se ejecuta como un usuario estándar y la aplicación ya se ha asignado o publicado, la instalación de la aplicación administrada puede continuar sin preguntar.
-   Al usar Windows Vista en un entorno no corporativo, UAC controla la elevación de la instalación de la aplicación. Windows El instalador 4.0 puede llamar a [*Application Information Service*](a-gly.md) (AIS) para solicitar autorización de administrador para elevar una instalación. Antes de que se pueda ejecutar una instalación identificada como que requiere privilegios de administrador, UAC solicita al usuario su consentimiento para elevar la instalación. La solicitud de consentimiento se muestra de forma predeterminada, incluso si el usuario es miembro del grupo administradores local, porque los administradores se ejecutan como usuarios estándar hasta que una aplicación o componente del sistema que requiere credenciales administrativas solicita permiso para ejecutarse. Esta experiencia de usuario se denomina [*Modo de aprobación de*](a-gly.md) administrador (AAM). Si un usuario estándar intenta instalar la aplicación, el usuario tiene que obtener una persona con privilegios de administrador para proporcionarle sus credenciales de administrador para continuar con la instalación. Esta experiencia de usuario se denomina mensaje [*de credencial Over the Shoulder*](o-gly.md) (OTS).
-   Dado que UAC restringe los privilegios durante las fases de una instalación, los desarrolladores de paquetes del instalador de Windows no deben asumir que su instalación siempre tendrá acceso a todas las partes del sistema. Windows Por lo tanto, los desarrolladores de paquetes del instalador deben cumplir las directrices de paquetes descritas en [Directrices](guidelines-for-packages.md) para paquetes para asegurarse de que su paquete funciona con UAC y Windows Vista. Un paquete que se ha escrito y probado para cumplir con UAC debe contener la propiedad [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) establecida en 1.
-   Un administrador también puede usar los métodos descritos en la sección: Instalación de un paquete con [privilegios elevados](installing-a-package-with-elevated-privileges-for-a-non-admin.md) para que un usuario que no es administrador pueda instalar una aplicación con privilegios elevados del sistema.
-   Los privilegios son necesarios para instalar una aplicación en el contexto administrado por usuario y, por tanto, las reinstalaciones o reparaciones posteriores del instalador de Windows también se realizan mediante el instalador con privilegios elevados. Esto significa que solo se pueden aplicar revisiones de orígenes de confianza a una aplicación en estado administrado por usuario. A partir Windows Installer 3.0, puede aplicar una revisión a una aplicación administrada por usuario después de que la revisión se haya registrado como con privilegios elevados. Para obtener información, [consulte Aplicación de Per-User aplicaciones administradas.](patching-per-user-managed-applications.md)

> [!Note]  
> Cuando no se requieren privilegios elevados para instalar un paquete del instalador de Windows, el autor del paquete puede suprimir el cuadro de diálogo que muestra UAC para solicitar a los usuarios autorización de administrador. Para obtener más información, vea [Crear paquetes sin el cuadro de diálogo UAC](authoring-packages-without-the-uac-dialog-box.md).

 

 

 
