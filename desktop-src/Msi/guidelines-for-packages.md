---
description: Dado que el Control de cuentas de usuario (UAC) de Windows Vista restringe los privilegios durante una instalación, los desarrolladores de paquetes del instalador de Windows no deben asumir que su instalación siempre tiene acceso a todas las partes del sistema.
ms.assetid: 8e3b4ad8-b978-4e27-b060-1d023846718f
title: Directrices para paquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930cb97cd2bb01a2bd69c5950a7e054c73d355e534ab67c812bcde44b7495b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649325"
---
# <a name="guidelines-for-packages"></a>Directrices para paquetes

Dado que [*el Control*](u-gly.md) de cuentas de usuario (UAC) de Windows Vista restringe los privilegios durante una instalación, los desarrolladores de paquetes del instalador de Windows no deben asumir que su instalación siempre tiene acceso a todas las partes del sistema.

En la mayoría de los casos, [](/previous-versions/windows/desktop/Policy/group-policy-start-page) un paquete de instalador que se pueda implementar correctamente para los usuarios estándar a través de directiva de grupo también debe funcionar con UAC en Windows Vista. Pueden producirse excepciones si la tabla [InstallUISequence](installuisequence-table.md) contiene la acción [LaunchConditions](launchconditions-action.md) o la tabla [LaunchCondition](launchcondition-table.md) contiene una condición basada en la [propiedad Privileged](privileged.md). Windows Por lo tanto, los desarrolladores de paquetes del instalador deben cumplir las siguientes directrices para asegurarse de que su paquete funciona con UAC y Windows Vista.

-   Al incluir una [*condición de contexto de*](i-gly.md) instalación con una acción en la tabla [InstallUISequence](installuisequence-table.md), use una instrucción condicional basada en la [propiedad Privileged](privileged.md). No use una condición basada en la [**propiedad AdminUser.**](adminuser.md)
-   Al incluir el contexto de instalación con las condiciones de inicio de la instalación, use un tipo de acción personalizada [19](custom-action-type-19.md) en la tabla [InstallExecuteSequence](installexecutesequence-table.md) y haga que la acción personalizada sea condicional a la propiedad [Privileged](privileged.md). No use una acción en la [tabla LaunchCondition con](launchcondition-table.md) una condición basada en la [propiedad AdminUser](adminuser.md) o la propiedad Privileged.
-   Para leer o modificar la configuración del sistema, use una acción personalizada de ejecución [aplazada](deferred-execution-custom-actions.md) en la [tabla InstallExecuteSequence](installexecutesequence-table.md). No use acciones personalizadas de ejecución inmediata en [la tabla InstallUISequence](installuisequence-table.md) para modificar la configuración del sistema.
-   Para modificar partes del sistema que no son específicas del usuario, use una acción personalizada diferida en la [tabla InstallExecuteSequence](installexecutesequence-table.md). Debe incluir el bit msidbCustomActionTypeNoImpersonate en el tipo de acción personalizada.
-   Omita el bit 3 del valor de la propiedad [**Resumen**](word-count-summary.md) de recuento de palabras para indicar que se puede tener que elevar el paquete. No incluya este bit a menos que no se requieran privilegios elevados para instalar este paquete.
-   Incluya un manifiesto con el nivel de ejecución solicitado de la aplicación.
-   Incluya un certificado en la [tabla MsiPatchCertificate](msipatchcertificate-table.md) del paquete original y firme todas las revisiones con el mismo certificado.
-   Si se requieren privilegios elevados para instalar un paquete del instalador de Windows, el autor del paquete debe incluir el atributo [ElevationShield](elevationshield-attribute.md) para el [control PushButton](pushbutton-control.md) usado para iniciar la instalación. Esto avisará al usuario de que al hacer clic en el botón se mostrará el cuadro de diálogo UAC que solicita autorización de administrador para continuar con la instalación.
-   Establezca la [**propiedad MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) en 1 para indicar al instalador de Windows que el paquete se ha escrito y probado para cumplir con UAC en Windows Vista. Si no se establece esta propiedad, el instalador determina si el paquete cumple con UAC.

Fuera de [directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page), se puede usar la siguiente comprobación del cumplimiento de UAC en Windows XP.

**Para comprobar el cumplimiento de UAC fuera de directiva de grupo**

1.  Inicie una sesión en el equipo como administrador.
2.  Anuncie el paquete para una instalación por máquina:

    **msiexec /jm** *package.msi*

3.  Cierre la sesión del equipo.
4.  Inicie sesión en el equipo como usuario estándar.
5.  Intente instalar el paquete anunciado:

    **msiexec /i** *package.msi*

6.  En la mayoría de los casos, si la instalación se realiza correctamente, el paquete es compatible con UAC.
7.  Establezca la [**propiedad MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) del paquete en 1.
8.  Pruebe la instalación correcta del paquete mediante Windows Vista.

 

 
