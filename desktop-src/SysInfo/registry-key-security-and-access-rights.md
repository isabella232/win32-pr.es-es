---
description: El Windows de seguridad le permite controlar el acceso a las claves del Registro. Para obtener más información sobre la seguridad, vea Access-Control modelo.
ms.assetid: 266d5c8e-1bcd-48e5-bc06-2fbc956d8658
title: Derechos de acceso y seguridad de la clave del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0797eeff4923574007c2e1d7751121767c894f91a42316ff5d581ee2d18b6d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885208"
---
# <a name="registry-key-security-and-access-rights"></a>Derechos de acceso y seguridad de la clave del Registro

El Windows de seguridad le permite controlar el acceso a las claves del Registro. Para obtener más información sobre la seguridad, vea [Modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model).

Puede especificar un [descriptor de seguridad para](/windows/desktop/SecAuthZ/security-descriptors) una clave del Registro al llamar a la función [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) [**o RegSetKeySecurity.**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity) Si especifica **NULL,** la clave obtiene un descriptor de seguridad predeterminado. Las ACL de un descriptor de seguridad predeterminado para una clave se heredan de su clave primaria directa.

Para obtener el descriptor de seguridad de una clave del Registro, llame a la [**función RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity), [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa)o [**GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo)

Los derechos de acceso válidos para las claves del Registro incluyen los derechos de acceso estándar DELETE, READ \_ CONTROL, WRITE \_ DAC y WRITE OWNER \_ . [](/windows/desktop/SecAuthZ/standard-access-rights) Las claves del Registro no admiten el derecho de acceso estándar SYNCHRONIZE.

En la tabla siguiente se enumeran los derechos de acceso específicos para los objetos de clave del Registro.



| Valor                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACCESO \_ A KEY ALL \_ (0xF003F)<br/>         | Combina los derechos ESTÁNDAR NECESARIOS, VALOR DE CONSULTA DE CLAVE, VALOR DE CONJUNTO DE \_ \_ \_ \_ \_ \_ CLAVES, KEY \_ CREATE SUB \_ \_ KEY, KEY \_ ENUMERATE SUB \_ \_ KEYS, KEY NOTIFY y KEY CREATE \_ \_ \_ LINK.<br/>                                                                                                                                                                                                                                                                           |
| KEY \_ CREATE \_ LINK (0x0020)<br/>         | Reservado para uso del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| KEY \_ CREATE SUB KEY \_ \_ (0x0004)<br/>     | Necesario para crear una subclave de una clave del Registro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ SUBCLAVE ENUMERACIÓN DE CLAVES \_ (0x0008)<br/> | Necesario para enumerar las subclaves de una clave del Registro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| KEY \_ EXECUTE (0x20019)<br/>             | Equivalente a KEY \_ READ.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| KEY \_ NOTIFY (0x0010)<br/>               | Necesario para solicitar notificaciones de cambio para una clave del Registro o para subclaves de una clave del Registro.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| VALOR \_ DE CONSULTA DE CLAVE \_ (0x0001)<br/>         | Necesario para consultar los valores de una clave del Registro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| KEY \_ READ (0x20019)<br/>                | Combina los valores DE STANDARD \_ RIGHTS \_ READ, KEY \_ QUERY \_ VALUE, KEY \_ ENUMERATE SUB KEYS y KEY \_ \_ \_ NOTIFY.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| VALOR \_ DE CONJUNTO DE CLAVES \_ (0x0002)<br/>           | Necesario para crear, eliminar o establecer un valor del Registro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| KEY \_ WOW64 \_ 32KEY (0x0200)<br/>         | Indica que una aplicación de 64 Windows debe funcionar en la vista del Registro de 32 bits. Esta marca se omite mediante una Windows de 32 Windows. Para obtener más información, vea [Accessing an Alternate Registry View](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).<br/> Esta marca debe combinarse mediante el operador OR con las otras marcas de esta tabla que consultan o acceden a los valores del Registro.<br/> **Windows 2000:** Esta marca no se admite.<br/> |
| KEY \_ WOW64 \_ 64KEY (0x0100)<br/>         | Indica que una aplicación de 64 Windows debe funcionar en la vista del Registro de 64 bits. Esta marca se omite mediante una Windows de 32 Windows. Para obtener más información, vea [Accessing an Alternate Registry View](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).<br/> Esta marca debe combinarse mediante el operador OR con las otras marcas de esta tabla que consultan o acceden a los valores del Registro.<br/> **Windows 2000:** Esta marca no se admite.<br/> |
| KEY \_ WRITE (0x20006)<br/>               | Combina los derechos de acceso STANDARD \_ RIGHTS \_ WRITE, KEY \_ SET VALUE y KEY CREATE SUB \_ \_ \_ \_ KEY.<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

Al llamar a la [**función RegOpenKeyEx,**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad de la clave. Si el usuario no tiene el acceso correcto a la clave del Registro, se produce un error en la operación de apertura. Si un administrador necesita acceso a la clave, la solución es habilitar el privilegio SE TAKE OWNERSHIP NAME y abrir la clave del Registro con acceso \_ \_ WRITE \_ \_ OWNER. Para obtener más información, vea [Habilitación y deshabilitación de privilegios.](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--)

Puede solicitar el derecho de acceso ACCESS SYSTEM SECURITY a una clave del Registro si desea leer o escribir la lista de control de acceso del sistema \_ (SACL) de la \_ clave. Para obtener más información, vea [Listas de control de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y Derecho de acceso [sacl](/windows/desktop/SecAuthZ/sacl-access-right).

Para ver los derechos de acceso actuales de una clave, incluidas las claves predefinidas, use el Editor del Registro (Regedt32.exe). Después de navegar a la clave deseada, vaya al **menú Editar** y seleccione **Permisos.**

 

