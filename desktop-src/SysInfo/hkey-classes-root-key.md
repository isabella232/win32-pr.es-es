---
description: La clave HKEY CLASSES ROOT (HKCR) contiene asociaciones de extensión de nombre de archivo e información de registro de clases COM, como \_ \_ ProgID, CLSID y IID. Está pensado principalmente para la compatibilidad con el Registro en aplicaciones de 16 Windows.
ms.assetid: b404875f-11e1-48f2-98d2-0378a0646ed3
title: HKEY_CLASSES_ROOT clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7aebe0e59424eb5ff7584fe61c2c5089eb887b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371882"
---
# <a name="hkey_classes_root-key"></a>Clave RAÍZ DE CLASES HKEY \_ \_

La **clave HKEY \_ CLASSES \_ ROOT** **(HKCR)** contiene asociaciones de extensión de nombre de archivo e información de registro de clases COM, como [ProgIDs,](../com/-progid--key.md) [CLSID y](../com/clsid-key-hklm.md) [IID.](../com/interface-key.md) Está pensado principalmente para la compatibilidad con el Registro en aplicaciones de 16 Windows.

La información de extensión de nombre de archivo y registro de clases se almacena en las claves **HKEY \_ LOCAL MACHINE \_ y** **HKEY CURRENT \_ \_ USER.** La **clave HKEY \_ LOCAL MACHINE \_ Software \\ \\ Classes** contiene la configuración predeterminada que se puede aplicar a todos los usuarios del equipo local. La **clave HKEY \_ CURRENT USER \_ Software \\ \\ Classes** contiene valores que solo se aplican al usuario interactivo. La **clave RAÍZ \_ HKEY CLASSES \_** proporciona una vista del Registro que combina la información de estos dos orígenes. **HKEY \_ CLASSES \_ ROOT** también proporciona esta vista combinada para aplicaciones diseñadas para versiones anteriores de Windows.

La configuración específica del usuario tiene prioridad sobre la configuración predeterminada. Por ejemplo, la configuración predeterminada podría especificar una aplicación determinada para controlar .doc archivos. Pero un usuario puede invalidar esta configuración especificando una aplicación diferente en el Registro.

Las funciones del Registro [**como RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) [**o RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) permiten especificar la **clave RAÍZ HKEY \_ CLASSES. \_** Cuando se llama a estas funciones desde un proceso que se ejecuta en la cuenta de usuario interactiva, el sistema combina la configuración predeterminada en HKEY LOCAL MACHINE Software Classes con la configuración del usuario interactivo en **HKEY \_ CURRENT USER Software \_ \\ \\** **\_ \_ \\ \\ Classes** . Para obtener más información sobre cómo se combinan estas opciones, vea [Vista combinada de HKEY CLASSES \_ \_ ROOT](merged-view-of-hkey-classes-root.md).

Para cambiar la configuración del usuario interactivo, almacene los cambios en **HKEY \_ CURRENT USER Software \_ \\ \\ Classes** en lugar de **HKEY CLASSES \_ \_ ROOT**.

Para cambiar la configuración predeterminada, almacene los cambios en **Clases de software HKEY LOCAL \_ \_ \\ \\ MACHINE**. Si escribe claves en una clave en **HKEY \_ CLASSES \_ ROOT**, el sistema almacena la información en clases de **software HKEY LOCAL \_ \_ MACHINE \\ \\**. Si escribe valores en una clave en **HKEY \_ CLASSES \_ ROOT** y la clave ya existe en HKEY CURRENT USER Software Classes , el sistema almacenará la información allí en lugar de en **HKEY \_ LOCAL MACHINE Software \_ \\ \\** **\_ \_ \\ \\ Classes**.

Los procesos que se ejecutan en un contexto de seguridad distinto del del usuario interactivo no deben usar la clave RAÍZ **HKEY \_ CLASSES \_** con las funciones del Registro. En su lugar, estos procesos pueden abrir explícitamente la **clave HKEY \_ LOCAL MACHINE \_ Software \\ \\ Classes** para acceder a la configuración predeterminada. Para abrir una clave del Registro que combine el contenido de **HKEY \_ LOCAL MACHINE \_ Software \\ \\ Classes** con la configuración de un usuario especificado, estos procesos pueden llamar a la [**función RegOpenUserClassesRoot.**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) Por ejemplo, un subproceso que suplanta [a](/windows/desktop/SecAuthZ/client-impersonation) un cliente puede llamar a **RegOpenUserClassesRoot** si necesita recuperar una vista combinada para el cliente que se está suplantando. Tenga en **cuenta que RegOpenUserClassesRoot produce** un error si no se ha cargado el perfil de usuario para el usuario especificado. El sistema carga automáticamente el perfil del usuario interactivo al iniciar sesión. Para otros usuarios, debe llamar a la [**función LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) para cargar explícitamente el perfil del usuario.

Si una aplicación se ejecuta con derechos de administrador y el control de cuentas de usuario está deshabilitado, el tiempo de ejecución com omite la configuración COM por usuario y solo tiene acceso a la configuración COM por equipo. Las aplicaciones que requieren derechos de administrador deben registrar objetos COM dependientes durante la instalación en el almacén de configuración COM por máquina ( clases de **software HKEY \_ LOCAL \_ MACHINE \\ \\**). Para obtener más información, [vea AC: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 y Windows XP/2000:** Las aplicaciones pueden registrar objetos COM dependientes en el almacén de configuración COM por equipo o por usuario ( clases de **software HKEY \_ LOCAL \_ MACHINE \\ \\** o clases de **software HKEY \_ CURRENT \_ USER \\ \\**).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[HKEY \_ CLASSES \_ ROOT (Referencia del Registro del Kit de recursos)](/previous-versions/windows/it-pro/windows-server-2003/cc739822(v=ws.10))
</dt> </dl>

 

 
