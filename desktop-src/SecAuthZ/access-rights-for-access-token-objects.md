---
description: Una aplicación no puede cambiar la lista de control de acceso de un objeto a menos que la aplicación tenga los derechos para hacerlo.
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Derechos de acceso para objetos de Access-Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb6a62a8c1518dca30f2abbc4481fa5e11cf081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360629"
---
# <a name="access-rights-for-access-token-objects"></a>Derechos de acceso para objetos de Access-Token

Una aplicación no puede cambiar la lista de control de acceso de un objeto a menos que la aplicación tenga los derechos para hacerlo. Estos derechos se controlan mediante un descriptor de seguridad en el token de acceso para el objeto. Para obtener más información sobre la seguridad, vea [modelo de Access Control](access-control-model.md).

Para obtener o establecer el [descriptor de seguridad](security-descriptors.md) de un [*token de acceso*](/windows/desktop/SecGloss/a-gly), llame a las funciones [**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) y [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) .

Cuando se llama a la función [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) o [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obtener un identificador de un token de acceso, el sistema comprueba los [derechos de acceso](access-rights-and-access-masks.md) solicitados en la DACL en el descriptor de seguridad del token.

Los siguientes son derechos de acceso válidos para los objetos de token de acceso:

-   Los derechos de acceso de eliminación, \_ control de lectura, \_ DAC de escritura y propietario de escritura \_ [estándar](standard-access-rights.md). Los tokens de acceso no admiten el derecho SINCRONIZAr el acceso estándar.
-   [Derecho de \_ \_ seguridad del sistema de acceso](sacl-access-right.md) para obtener o establecer la SACL en el descriptor de seguridad del objeto.
-   Los derechos de acceso específicos para los tokens de acceso, que se enumeran en la tabla siguiente.

    | Value                     | Significado                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_valor predeterminado de ajuste de token \_    | Se requiere para cambiar el propietario, el grupo primario o la DACL predeterminados de un token de acceso.                                                                                                                                                                                                  |
    | \_ajustar \_ grupos de tokens     | Necesario para ajustar los atributos de los grupos en un token de acceso.                                                                                                                                                                                                               |
    | \_privilegios de ajuste de token \_ | Necesario para habilitar o deshabilitar los privilegios en un token de acceso.                                                                                                                                                                                                                  |
    | TOKEN \_ ADJUST \_ SESSIONID  | Necesario para ajustar el identificador de sesión de un token de acceso. \_Se requiere el privilegio del nombre de la TCB \_ .                                                                                                                                                                                    |
    | asignación de TOKEN \_ \_ principal    | Necesario para asociar un [*token primario*](/windows/desktop/SecGloss/p-gly) a un [*proceso*](/windows/desktop/SecGloss/p-gly). \_ \_ También se requiere el privilegio de nombre de ASSIGNPRIMARYTOKEN se para realizar esta tarea. |
    | TOKEN \_ duplicado          | Obligatorio para duplicar un token de acceso.                                                                                                                                                                                                                                            |
    | ejecución de TOKEN \_            | Combina la \_ ejecución de los derechos estándar \_ y la \_ suplantación de tokens.                                                                                                                                                                                                                        |
    | suplantación de TOKEN \_        | Necesario para adjuntar un token de acceso de suplantación a un proceso.                                                                                                                                                                                                                    |
    | consulta de TOKEN \_              | Obligatorio para consultar un token de acceso.                                                                                                                                                                                                                                                |
    | origen de la consulta de TOKEN \_ \_      | Obligatorio para consultar el origen de un token de acceso.                                                                                                                                                                                                                                  |
    | lectura de TOKEN \_               | Combina la \_ \_ consulta de token y lectura de derechos estándar \_ .                                                                                                                                                                                                                                 |
    | escritura de TOKENs \_              | Combina la \_ \_ escritura de derechos estándar, los \_ \_ privilegios de ajuste de tokens, los grupos de ajuste de token \_ \_ y el \_ valor predeterminado de ajuste de token \_ .                                                                                                                                                                   |
    | acceso de TOKEN \_ todo \_        | Combina todos los derechos de acceso posibles para un token.                                                                                                                                                                                                                                  |

    

     

 

 
