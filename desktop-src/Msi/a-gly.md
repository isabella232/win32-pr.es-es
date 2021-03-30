---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46677d8823c5298307db922f2d61285564add437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156360"
---
# <a name="a-windows-installer"></a>A (Windows Installer)

A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [o](o-gly.md) [p](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**Consejos**
</dt> <dd>

Diseñar la implementación para que la interfaz de usuario del instalador sea accesible para todos los usuarios. Para obtener más información sobre la accesibilidad, vea el tema de información general: [accesibilidad](accessibility.md).

</dd> <dt>

<span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**fase de adquisición**
</dt> <dd>

Fase de instalación durante la cual el instalador determina el procedimiento. La fase de adquisición comienza cuando una aplicación o un usuario indica [*Windows Installer*](m-gly.md) para instalar una aplicación o una característica. A continuación, el instalador consulta la [*base*](i-gly.md) de datos para obtener información, ya que genera el [*script de ejecución*](e-gly.md) para la instalación. Para obtener más información acerca de las fases de una instalación, vea [mecanismo de instalación](installation-mechanism.md).

</dd> <dt>

<span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**actuar**
</dt> <dd>

Muchas de las funciones realizadas por Windows Installer se encapsulan en acciones. Cada acción especifica la ejecución de una función determinada y el flujo total de procedimientos de la instalación viene determinado por la secuencia de acciones de las [*tablas de secuencia*](s-gly.md). [*Las acciones estándar*](s-gly.md) están integradas en Windows Installer. El autor del [*paquete*](p-gly.md)de instalación escribe las [*acciones personalizadas*](c-gly.md) .

</dd> <dt>

<span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Modo de aprobación de administrador**
</dt> <dd>

El estado de aprobación habilitado por la protección de cuentas de usuario (UAC) que ejecuta todos los usuarios con privilegios mínimos, incluidos los administradores. Los usuarios deben dar su consentimiento para elevar las instalaciones que requieran privilegios de administrador.

</dd> <dt>

<span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**Anunciar**
</dt> <dd>

Capacidad de hacer que las interfaces sean necesarias para cargar y hacer que una aplicación esté disponible sin necesidad de instalar la aplicación. Cuando un usuario o una aplicación activa una interfaz anunciada, el instalador continúa con la instalación de los componentes necesarios. Los dos tipos de publicidad son la [*asignación*](/windows) y [*publicación*](p-gly.md). Para obtener más información, consulte también [*instalación a petición*](i-gly.md). Para obtener más información acerca de cómo el instalador anuncia las aplicaciones, consulte el [anuncio](advertisement.md).

</dd> <dt>

<span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Servicio de información de la aplicación (AIS)**
</dt> <dd>

Servicio de sistema de Windows Vista que facilita el inicio de las instalaciones que requieren privilegios elevados para ejecutarse. Proporciona la interfaz de usuario de consentimiento utilizada por el control de cuentas de usuario para solicitar a un usuario autorización de administrador.

</dd> <dt>

<span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**asignar**
</dt> <dd>

Hace que una aplicación esté disponible y hace que parezca que se ha instalado para un usuario, sin instalarla realmente. La asignación agrega accesos directos e iconos al menú **Inicio** , asocia los archivos adecuados y escribe entradas del registro para la aplicación. Cuando un usuario intenta abrir una aplicación asignada, el instalador instala la aplicación. La asignación y [*publicación*](p-gly.md) son dos métodos de [*publicidad*](/windows). Para obtener más información, vea el [anuncio](advertisement.md).

</dd> <dt>

<span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**ejecución asincrónica**
</dt> <dd>

[*Acción personalizada*](c-gly.md) durante la cual el instalador ejecuta subprocesos independientes de la acción personalizada y la instalación actual simultáneamente. Para obtener más información, vea [acciones personalizadas sincrónicas y asincrónicas](synchronous-and-asynchronous-custom-actions.md).

</dd> </dl>

 

 
