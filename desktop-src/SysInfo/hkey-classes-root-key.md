---
description: La clave de la \_ raíz de clases HKEY \_ (HKCR) contiene asociaciones de extensión de nombre de archivo e información de registro de la clase com, como ProgID, CLSID y IID. Está pensado principalmente para la compatibilidad con el registro en Windows de 16 bits.
ms.assetid: b404875f-11e1-48f2-98d2-0378a0646ed3
title: Clave de HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7aebe0e59424eb5ff7584fe61c2c5089eb887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912782"
---
# <a name="hkey_classes_root-key"></a>\_Clase HKEY \_ clave raíz

La clave de la **\_ \_ raíz de clases HKEY** (**HKCR**) contiene asociaciones de extensión de nombre de archivo e información de registro de la clase com, como [ProgID](../com/-progid--key.md), [CLSID](../com/clsid-key-hklm.md)y [IID](../com/interface-key.md). Está pensado principalmente para la compatibilidad con el registro en Windows de 16 bits.

El registro de clases y la información de la extensión de nombre de archivo se almacenan en las claves **HKEY \_ local \_ Machine** y **HKEY \_ Current \_ User** . La clave **HKEY \_ local \_ Machine \\ software \\ classes** contiene la configuración predeterminada que se puede aplicar a todos los usuarios del equipo local. La clave de **\_ clases de \_ \\ software \\ del usuario actual de HKEY** contiene opciones que solo se aplican al usuario interactivo. La **clave \_ \_ raíz de las clases HKEY** proporciona una vista del registro que combina la información de estos dos orígenes. **HKEY \_ La \_ raíz de clases** también proporciona esta vista combinada para las aplicaciones diseñadas para versiones anteriores de Windows.

La configuración específica del usuario tiene prioridad sobre la configuración predeterminada. Por ejemplo, la configuración predeterminada puede especificar una aplicación determinada para administrar los archivos. doc. Pero un usuario puede invalidar esta configuración especificando una aplicación diferente en el registro.

Las funciones del registro como [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) o [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) permiten especificar la clave **\_ \_ raíz de las clases HKEY** . Cuando se llama a estas funciones desde un proceso que se ejecuta en la cuenta de usuario interactiva, el sistema combina la configuración predeterminada en **\_ \_ \\ \\ las clases de software de máquina local HKEY** con la configuración del usuario interactivo en **HKEY clases de \_ \_ software de usuario \\ \\ actuales**. Para obtener más información sobre cómo se combinan estas opciones, vea [vista combinada de clases HKEY \_ \_ root](merged-view-of-hkey-classes-root.md).

Para cambiar la configuración del usuario interactivo, almacene los cambios en **HKEY \_ Current \_ User \\ software \\ classes** en lugar de **HKEY \_ classes \_ root**.

Para cambiar la configuración predeterminada, almacene los cambios en **HKEY \_ local \_ Machine \\ software \\ classes**. Si escribe claves en una clave en la **\_ \_ raíz de las clases HKEY**, el sistema almacena la información en **HKEY \_ local \_ Machine \\ software \\ classes**. Si escribe valores en una clave en la **\_ \_ raíz de las clases HKEY** y la clave ya existe **en \_ \_ \\ \\ las clases de software de usuario actuales de HKEY**, el sistema almacenará la información allí, en lugar de en **HKEY \_ local \_ Machine \\ software \\ classes**.

Los procesos que se ejecutan en un contexto de seguridad distinto del usuario interactivo no deben usar la clave **\_ \_ raíz de las clases HKEY** con las funciones del registro. En su lugar, estos procesos pueden abrir explícitamente la clave **HKEY \_ local \_ Machine \\ software \\ classes** para tener acceso a la configuración predeterminada. Para abrir una clave del registro que combina el contenido de **\_ \_ \\ \\ las clases de software del equipo local HKEY** con la configuración de un usuario especificado, estos procesos pueden llamar a la función [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) . Por ejemplo, un subproceso que [suplanta](/windows/desktop/SecAuthZ/client-impersonation) a un cliente puede llamar a **RegOpenUserClassesRoot** si necesita recuperar una vista combinada para el cliente que se va a suplantar. Tenga en cuenta que **RegOpenUserClassesRoot** produce un error si no se ha cargado el perfil de usuario para el usuario especificado. El sistema carga automáticamente el perfil para el usuario interactivo al iniciar sesión. Para otros usuarios, debe llamar a la función [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) para cargar explícitamente el perfil del usuario.

Si una aplicación se ejecuta con derechos de administrador y el control de cuentas de usuario está deshabilitado, el tiempo de ejecución de COM omite la configuración de COM por usuario y solo tiene acceso a la configuración COM por equipo. Las aplicaciones que requieren derechos de administrador deben registrar objetos COM dependientes durante la instalación en el almacén de configuración COM por equipo (**\_ clases de \_ \\ software \\ de máquina local HKEY**). Para obtener más información, vea [AC: UAC: COM Per-User configuración](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 y Windows XP/2000:** Las aplicaciones pueden registrar objetos COM dependientes en el almacén de configuración COM por equipo o por usuario **( \_ \_ clases de \\ software \\ de máquina local HKEY** o **\_ \_ \\ \\ clases de software de usuario actual HKEY**).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_Clase HKEY \_ raíz (referencia del registro del kit de recursos)](/previous-versions/windows/it-pro/windows-server-2003/cc739822(v=ws.10))
</dt> </dl>

 

 
