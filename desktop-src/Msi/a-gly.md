---
description: Obtenga información sobre Windows installer que comienzan con la letra A, como la fase de accesibilidad y adquisición.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715e051d584ada5c96fbc8ac5cdf717b666276f81ea6f94331217a766074bace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066485"
---
# <a name="a-windows-installer"></a>A (Windows instalador)

A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**Accesibilidad**
</dt> <dd>

Diseñe la implementación para que la interfaz de usuario del instalador sea accesible para todos los usuarios. Para obtener más información sobre la accesibilidad, vea el tema de información general: [Accesibilidad](accessibility.md).

</dd> <dt>

<span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**fase de adquisición**
</dt> <dd>

Fase de instalación durante la cual el instalador determina el procedimiento. La fase de adquisición comienza cuando una aplicación o un usuario [*Windows instalador para*](m-gly.md) instalar una aplicación o característica. A continuación, el instalador consulta [*la base de*](i-gly.md) datos para obtener información a medida que genera el script de [*ejecución*](e-gly.md) para la instalación. Para obtener más información sobre las fases de una instalación, vea [Mecanismo de instalación](installation-mechanism.md)de .

</dd> <dt>

<span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**Acción**
</dt> <dd>

Muchas de las funciones realizadas por Windows Installer se encapsulan en acciones. Cada acción especifica la ejecución de una función determinada y el flujo de procedimientos total de la instalación se prescribe mediante la secuencia de acciones de las [*tablas sequence*](s-gly.md). [*Las acciones estándar*](s-gly.md) están integradas en Windows Instalador. [*El autor*](c-gly.md) del paquete de instalación escribe acciones [*personalizadas.*](p-gly.md)

</dd> <dt>

<span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Modo de aprobación de administrador**
</dt> <dd>

Estado de aprobación habilitado por La protección de cuentas de usuario (UAC) que ejecuta todos los usuarios con privilegios mínimos, incluidos los administradores. Los usuarios deben dar su consentimiento para elevar las instalaciones que requieren privilegios de administrador.

</dd> <dt>

<span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**Publicidad**
</dt> <dd>

Capacidad para hacer que las interfaces necesarias para cargar y para que una aplicación esté disponible sin instalar la aplicación. Cuando un usuario o una aplicación activa una interfaz anunciada, el instalador continúa con la instalación de los componentes necesarios. Los dos tipos de publicidad son [*asignar*](/windows) y [*publicar*](p-gly.md). Para obtener más información, vea [*también instalación a petición.*](i-gly.md) Para obtener más información sobre cómo el instalador anuncia aplicaciones, vea [Anuncio](advertisement.md).

</dd> <dt>

<span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**
</dt> <dd>

Un servicio del sistema de Windows Vista que facilita el inicio de instalaciones que requieren privilegios elevados para ejecutarse. Proporciona la interfaz de usuario de consentimiento que usa el control de cuentas de usuario para solicitar autorización de administrador a un usuario.

</dd> <dt>

<span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**Asignar**
</dt> <dd>

Hace que una aplicación esté disponible y parezca que se ha instalado para un usuario, sin instalarla realmente. La asignación agrega accesos directos e iconos al **menú** Inicio, asocia los archivos adecuados y escribe entradas del Registro para la aplicación. Cuando un usuario intenta abrir una aplicación asignada, el instalador instala la aplicación. La asignación [*y publicación son*](p-gly.md) dos métodos de [*publicidad.*](/windows) Para obtener más información, vea [Anuncio](advertisement.md).

</dd> <dt>

<span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**ejecución asincrónica**
</dt> <dd>

[*Acción personalizada*](c-gly.md) durante la cual el instalador ejecuta subprocesos independientes de la acción personalizada y la instalación actual simultáneamente. Para obtener más información, vea [Acciones personalizadas sincrónicas y asincrónicas.](synchronous-and-asynchronous-custom-actions.md)

</dd> </dl>

 

 
