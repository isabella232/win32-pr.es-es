---
title: Cómo un servicio registra sus SPN
description: Para que un cliente pueda usar un SPN para autenticar una instancia de un servicio, el SPN debe estar registrado en la cuenta de usuario o equipo que usará la instancia de servicio para iniciar sesión.
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- Cómo un servicio registra sus SPN AD
- nombre de entidad de seguridad de servicio ad , cómo un servicio registra sus SPN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ebf33ed0f28dff3acffdcdc96a880c21ec532ff677801dd52ac1801f44c80e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188588"
---
# <a name="how-a-service-registers-its-spns"></a>Cómo un servicio registra sus SPN

Para que un cliente pueda usar un SPN para autenticar una instancia de un servicio, el SPN debe estar registrado en la cuenta de usuario o equipo que usará la instancia de servicio para iniciar sesión. Normalmente, el registro de SPN se realiza mediante un programa de instalación de servicio que se ejecuta con privilegios de administrador de dominio.

El instalador de servicio que instala una instancia de servicio en un equipo host suele realizar el procedimiento siguiente.

**Para registrar SPN para una instancia de servicio**

1.  Llame a [**la función DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para crear uno o varios SPN únicos para la instancia de servicio. Para obtener más información, vea [Formatos de nombre para SPN únicos.](name-formats-for-unique-spns.md)
2.  Llame a [**la función DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar los nombres en la cuenta de inicio de sesión del servicio.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) registra los SPN como una propiedad de un objeto de cuenta de usuario o equipo en el directorio. **Los** objetos **user y computer** tienen un atributo **servicePrincipalName,** que es un atributo de varios valores para almacenar todos los SPN asociados a una cuenta de usuario o equipo. Si el servicio se ejecuta con una cuenta de usuario, los SPN se almacenan en el atributo **servicePrincipalName** de esa cuenta. Si el servicio se ejecuta en la cuenta LocalSystem, los SPN se almacenan en el atributo **servicePrincipalName** de la cuenta del equipo host del servicio. El **autor de la llamada DsWriteAccountSpn** debe especificar el nombre distintivo del objeto de cuenta en el que se almacenan los SPN.

Para asegurarse de que los SPN registrados son seguros, el atributo **servicePrincipalName** no se puede escribir directamente; solo se puede escribir llamando a [**DsWriteAccountSpn.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) El autor de la llamada debe tener acceso de escritura al **atributo servicePrincipalName** de la cuenta de destino. Normalmente, el acceso de escritura solo se concede de forma predeterminada a los administradores de dominio. Sin embargo, hay un caso especial en el que el sistema permite que un servicio que se ejecuta en la cuenta LocalSystem registre sus propios SPN en la cuenta de equipo del host del servicio. En este caso, el SPN que se escribe debe tener el formato " " y " host " debe ser el <service class> / <host> nombre DNS del &lt; equipo &gt; local.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) también puede quitar SPN de una cuenta. Un parámetro de operación indica si los SPN se van a agregar a la cuenta, quitarse de la cuenta o usarse para reemplazar completamente todos los SPN actuales de la cuenta. Cuando se desinstale una instancia de servicio, quite los SPN registrados para esa instancia.

Para obtener más información y un ejemplo de código que registra o anula el registro de los SPN de un servicio, vea Registrar los [SPN para un servicio](registering-the-spns-for-a-service.md).

Los servicios basados en host que usan el formato SPN simple " ", tienen la opción de usar la función <service class> / <host> [**DsServerRegisterSpn,**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) que crea y registra SPN para una instancia de servicio. **DsServerRegisterSpn es** una función auxiliar que llama a [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) y [**DsWriteAccountSpn.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)

Para obtener más información, vea [Cuentas de inicio de sesión de servicio](service-logon-accounts.md).

 

 




