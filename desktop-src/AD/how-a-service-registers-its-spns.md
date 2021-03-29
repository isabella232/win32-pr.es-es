---
title: Cómo un servicio registra sus SPN
description: Para que un cliente pueda utilizar un SPN para autenticar una instancia de un servicio, el SPN debe estar registrado en la cuenta de usuario o de equipo que la instancia de servicio usará para iniciar sesión.
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- Cómo un servicio registra sus SPN AD
- nombre de entidad de seguridad de servicio AD, cómo un servicio registra sus SPN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74410be3a024fc6accd1d8394e2ba8335be9f550
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903115"
---
# <a name="how-a-service-registers-its-spns"></a>Cómo un servicio registra sus SPN

Para que un cliente pueda utilizar un SPN para autenticar una instancia de un servicio, el SPN debe estar registrado en la cuenta de usuario o de equipo que la instancia de servicio usará para iniciar sesión. Normalmente, el registro de SPN se realiza mediante un programa de instalación de servicio que se ejecuta con privilegios de administrador de dominio.

El instalador del servicio que instala una instancia de servicio en un equipo host normalmente realiza el procedimiento siguiente.

**Para registrar los SPN para una instancia de servicio**

1.  Llame a la función [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para crear uno o varios SPN únicos para la instancia de servicio. Para obtener más información, vea [formatos de nombre para SPN únicos](name-formats-for-unique-spns.md).
2.  Llame a la función [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar los nombres en la cuenta de inicio de sesión del servicio.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) registra los SPN como una propiedad de un usuario o un objeto de cuenta de equipo en el directorio. los objetos de **usuario** y **equipo** tienen un atributo **ServicePrincipalName** , que es un atributo de varios valores para almacenar todos los SPN asociados a una cuenta de usuario o de equipo. Si el servicio se ejecuta bajo una cuenta de usuario, los SPN se almacenan en el atributo **ServicePrincipalName** de esa cuenta. Si el servicio se ejecuta en la cuenta LocalSystem, los SPN se almacenan en el atributo **ServicePrincipalName** de la cuenta del equipo host del servicio. El autor de la llamada **DsWriteAccountSpn** debe especificar el nombre distintivo del objeto de cuenta en el que se almacenan los SPN.

Para asegurarse de que los SPN registrados están seguros, el atributo **ServicePrincipalName** no se puede escribir directamente; solo se puede escribir llamando a [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna). El autor de la llamada debe tener acceso de escritura al atributo **ServicePrincipalName** de la cuenta de destino. Normalmente, el acceso de escritura solo se concede de forma predeterminada a los administradores de dominio. Sin embargo, hay un caso especial en el que el sistema permite que un servicio que se ejecuta con la cuenta LocalSystem registre sus propios SPN en la cuenta de equipo del host del servicio. En este caso, el SPN que se está escribiendo debe tener el formato " <service class> / <host> " y " &lt; host &gt; " debe ser el nombre DNS del equipo local.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) también puede quitar SPN de una cuenta. Un parámetro de operación indica si los SPN se van a agregar a la cuenta, se han quitado de la cuenta o se han utilizado para reemplazar completamente todos los SPN actuales de la cuenta. Cuando se desinstala una instancia de servicio, quite los SPN registrados para esa instancia.

Para obtener más información y un ejemplo de código que registre o anule el registro de los SPN de un servicio, consulte [registrar los SPN para un servicio](registering-the-spns-for-a-service.md).

Los servicios basados en host que usan el formato SPN simple " <service class> / <host> " tienen la opción de usar la función [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) , que crea y registra los SPN para una instancia de servicio. **DsServerRegisterSpn** es una función auxiliar que llama a [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) y [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna).

Para obtener más información, consulte [cuentas de inicio de sesión de servicio](service-logon-accounts.md).

 

 




