---
description: Una aplicación no puede cambiar la lista de control de acceso de un objeto a menos que la aplicación tenga los derechos para hacerlo.
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Derechos de acceso para Access-Token objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469081d2caa4e5ff7c9b7c55b4c09c31cff1acac
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327200"
---
# <a name="access-rights-for-access-token-objects"></a>Derechos de acceso para Access-Token objetos

Una aplicación no puede cambiar la lista de control de acceso de un objeto a menos que la aplicación tenga los derechos para hacerlo. Estos derechos se controlan mediante un descriptor de seguridad en el token de acceso para el objeto . Para obtener más información sobre la seguridad, [vea Access Control Model](access-control-model.md).

Para obtener o establecer el [descriptor de seguridad de](security-descriptors.md) un [*token*](/windows/desktop/SecGloss/a-gly)de acceso, llame a las funciones [**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) y [**SetKernelObjectSecurity.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)

Cuando se llama a la función [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) o [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obtener [](access-rights-and-access-masks.md) un identificador de un token de acceso, el sistema comprueba los derechos de acceso solicitados con la DACL en el descriptor de seguridad del token.

Los siguientes son derechos de acceso válidos para los objetos de token de acceso:

-   Los derechos de acceso estándar DELETE, READ CONTROL, WRITE DAC y \_ \_ WRITE OWNER \_ . [](standard-access-rights.md) Los tokens de acceso no admiten el derecho de acceso estándar SYNCHRONIZE.
-   Derecho [ACCESS \_ SYSTEM \_ SECURITY](sacl-access-right.md) para obtener o establecer la SACL en el descriptor de seguridad del objeto.
-   Derechos de acceso específicos para los tokens de acceso, que se enumeran en la tabla siguiente.

    | Valor                     | Significado                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | TOKEN \_ ADJUST \_ DEFAULT    | Necesario para cambiar el propietario predeterminado, el grupo principal o la DACL de un token de acceso.                                                                                                                                                                                                  |
    | GRUPOS \_ DE AJUSTE DE \_ TOKEN     | Necesario para ajustar los atributos de los grupos en un token de acceso.                                                                                                                                                                                                               |
    | PRIVILEGIOS \_ DE \_ AJUSTE DE TOKEN | Necesario para habilitar o deshabilitar los privilegios en un token de acceso.                                                                                                                                                                                                                  |
    | TOKEN \_ ADJUST \_ SESSIONID  | Necesario para ajustar el identificador de sesión de un token de acceso. Se requiere el privilegio SE \_ TCB \_ NAME.                                                                                                                                                                                    |
    | TOKEN \_ ASSIGN \_ PRIMARY    | Necesario para adjuntar un [*token principal*](/windows/desktop/SecGloss/p-gly) a un [*proceso*](/windows/desktop/SecGloss/p-gly). El privilegio SE \_ ASSIGNPRIMARYTOKEN \_ NAME también es necesario para realizar esta tarea. |
    | TOKEN \_ DUPLICADO          | Necesario para duplicar un token de acceso.                                                                                                                                                                                                                                            |
    | TOKEN \_ EXECUTE            | Igual que STANDARD \_ RIGHTS \_ EXECUTE.                                                                                                                                                                                                                                                |
    | \_SUPLANTACIÓN DE TOKEN        | Necesario para adjuntar un token de acceso de suplantación a un proceso.                                                                                                                                                                                                                    |
    | CONSULTA DE \_ TOKEN              | Necesario para consultar un token de acceso.                                                                                                                                                                                                                                                |
    | ORIGEN DE \_ CONSULTA \_ DE TOKEN      | Necesario para consultar el origen de un token de acceso.                                                                                                                                                                                                                                  |
    | LECTURA DEL \_ TOKEN               | Combina STANDARD \_ RIGHTS READ y TOKEN \_ \_ QUERY.                                                                                                                                                                                                                                 |
    | ESCRITURA DE \_ TOKENS              | Combina STANDARD \_ RIGHTS \_ WRITE, TOKEN ADJUST \_ \_ PRIVILEGES, TOKEN \_ ADJUST GROUPS y TOKEN ADJUST \_ \_ \_ DEFAULT.                                                                                                                                                                   |
    | TOKEN \_ ALL \_ ACCESS        | Combina todos los derechos de acceso posibles para un token.                                                                                                                                                                                                                                  |

    

     

 

 
