---
description: Dado que el control de cuentas de usuario (UAC) de Windows Vista restringe los privilegios durante una instalación, los desarrolladores de Windows Installer paquetes no deben suponer que su instalación siempre tenga acceso a todas las partes del sistema.
ms.assetid: 8e3b4ad8-b978-4e27-b060-1d023846718f
title: Directrices para paquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db228c2dff443d421ddc089074f0fcce6ae93e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910941"
---
# <a name="guidelines-for-packages"></a>Directrices para paquetes

Dado que el [*control de cuentas de usuario*](u-gly.md) (UAC) de Windows Vista restringe los privilegios durante una instalación, los desarrolladores de Windows Installer paquetes no deben suponer que su instalación siempre tenga acceso a todas las partes del sistema.

Un paquete del instalador que se puede implementar correctamente en los usuarios estándar a través de [Directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page) debe, en la mayoría de los casos, funcionar con UAC en Windows Vista. Las excepciones a esto pueden producirse si la [tabla InstallUISequence](installuisequence-table.md) contiene la [acción LaunchConditions](launchconditions-action.md) o la [tabla LaunchCondition](launchcondition-table.md) contiene una condición basada en la [propiedad privileged](privileged.md). Por lo tanto, los desarrolladores de paquetes de Windows Installer deben cumplir las siguientes directrices para asegurarse de que su paquete funciona con UAC y Windows Vista.

-   Al incluir una condición de [*contexto de instalación*](i-gly.md) con una acción en la [tabla InstallUISequence](installuisequence-table.md), use una instrucción condicional basada en la [propiedad privileged](privileged.md). No use una condición basada en la propiedad [**AdminUser**](adminuser.md) .
-   Al incluir el contexto de instalación con las condiciones de inicio de la instalación, use una [acción personalizada tipo 19](custom-action-type-19.md) en la [tabla InstallExecuteSequence](installexecutesequence-table.md) y haga que la acción personalizada sea condicional en función de la [propiedad privilegiada](privileged.md). No utilice una acción en la [tabla LaunchCondition](launchcondition-table.md) con una condición basada en la [propiedad AdminUser](adminuser.md) o la propiedad privilegiada.
-   Para leer o modificar la configuración del sistema, utilice una [acción personalizada de ejecución aplazada](deferred-execution-custom-actions.md) en la [tabla InstallExecuteSequence](installexecutesequence-table.md). No use acciones personalizadas de ejecución inmediata en la [tabla InstallUISequence](installuisequence-table.md) para modificar la configuración del sistema.
-   Para modificar partes del sistema que no son específicas del usuario, use una acción personalizada diferida en la [tabla InstallExecuteSequence](installexecutesequence-table.md). Debe incluir el bit msidbCustomActionTypeNoImpersonate en el tipo de acción personalizada.
-   Omita el bit 3 del valor de la propiedad de Resumen de [**recuento de palabras**](word-count-summary.md) para indicar que el paquete puede ser necesario para ser elevado. No incluya este bit a menos que no se requieran privilegios elevados para instalar este paquete.
-   Incluya un manifiesto con el nivel de ejecución solicitado de la aplicación.
-   Incluya un certificado en la tabla [MsiPatchCertificate](msipatchcertificate-table.md) de paquete original y firme todas las revisiones con el mismo certificado.
-   Si se requieren privilegios elevados para instalar un paquete de Windows Installer, el autor del paquete debe incluir el atributo [ElevationShield](elevationshield-attribute.md) para el [control Pushbutton](pushbutton-control.md) que se usa para iniciar la instalación. Esto le avisará al usuario de que al hacer clic en el botón se mostrará el cuadro de diálogo de UAC que solicita la autorización del administrador para continuar con la instalación.
-   Establezca la propiedad [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) en 1 para indicar al Windows Installer que el paquete se ha creado y probado para cumplir con UAC en Windows Vista. Si no se establece esta propiedad, el instalador determina si el paquete cumple con UAC.

Fuera de [Directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page), se puede usar la siguiente comprobación de compatibilidad con UAC en Windows XP.

**Para comprobar la compatibilidad de UAC fuera de directiva de grupo**

1.  Inicie una sesión en el equipo como administrador.
2.  Anunciar el paquete para una instalación por equipo:

    **msiexec/jm** *package.msi*

3.  Cierre la sesión del equipo.
4.  Inicie sesión en el equipo como usuario estándar.
5.  Intente instalar el paquete anunciado:

    **msiexec/i** *package.msi*

6.  En la mayoría de los casos, si la instalación se realiza correctamente, el paquete es compatible con UAC.
7.  Establezca la propiedad [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) del paquete en 1.
8.  Compruebe si la instalación del paquete es correcta mediante Windows Vista.

 

 
