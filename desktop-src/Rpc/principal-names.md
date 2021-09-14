---
title: Nombres principales
description: Para que un cliente cree una sesión autenticada mutuamente con un programa de servidor, debe proporcionar el nombre principal esperado del servidor.
ms.assetid: 4d9977f8-0efb-4559-977e-3eba4e277bc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554ffecff6eb019b4712e6b2d9f5c6319db492e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169050"
---
# <a name="principal-names"></a>Nombres principales

Para que un cliente cree una sesión autenticada mutuamente con un programa de servidor, debe proporcionar el nombre principal esperado del servidor. Algunos protocolos, como Kerberos, requieren un nombre principal de servidor correcto para cualquier sesión autenticada. Una entidad de seguridad es una entidad que el sistema de seguridad reconoce. Esto incluye usuarios humanos, así como servicios del sistema. Todos los nombres principales tienen un formato similar para un proveedor de soporte técnico de seguridad (SSP) determinado. Un SSP es un módulo de software que realiza la validación de seguridad. Para obtener más información, vea [Información general sobre la arquitectura de SSPI.](sspi-architectural-overview.md) Para mantener la uniformidad, un proveedor de seguridad suele dar a los servicios del sistema nombres similares a los de los usuarios. En algunos proveedores de seguridad, es posible que los servicios del sistema no tengan un nombre principal.

El servidor registra su nombre principal para el proveedor de seguridad mediante la [**función RpcServerRegisterAuthInfo.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) Solo se puede usar un nombre principal de servidor para cada proveedor de seguridad. Si se registra más de un nombre, se elige y se usa aleatoriamente un nombre. El SSP determina el formato del nombre principal. Por ejemplo, los SSP Kerberos/Negotiate para un servicio del sistema tienen un aspecto aproximadamente parecido al siguiente: nombre \_ del equipo$ @childdomain.parentdomain1.parentdomain2.COM .

El procedimiento recomendado para generar nombres principales es usar API documentadas (como la función **DsMakeSpn),** en lugar de crear circularmente el nombre principal a partir de cadenas. El uso de API documentadas aumenta la portabilidad entre diferentes entornos de implementación y elimina la posibilidad de errores.

Especificar un nombre principal incorrecto puede impedir que el cliente y el servidor establezcan una sesión autenticada. SCHANNEL SSP toma nombres principales en cualquiera de las dos formas:

-   El primer formulario de nombre principal de SCHANNEL es [*el formulario msstd.*](m-glos.md) Los nombres con formato msstd suelen seguir el patrón msstd:servername@serverdomain.com . Esto se conoce como una propiedad de nombre de correo electrónico. Si el certificado contiene una propiedad de nombre de correo electrónico y contiene el valor de at sign (@), el nombre principal es msstd:email name. De lo contrario, debe contener la propiedad de nombre común. Las barras diagonales inversas internas se duplican, igual que en los enlaces de cadena.
-   El segundo formulario de nombre principal de SCHANNEL es [*el formato completo.*](f-glos.md) Se trata de una serie de nombres compatibles con RFC1779 delimitados por corchetes angulares y separados por barras diagonales inversas. Normalmente sigue el patrón fullsic: \\ < \\ Authority \\ SubAuthority \\ ...... \\ Person> o fullsic: \\ < \\ Authority \\ SubAuthority \\ ...... \\ ServerProgram>.

Si el nombre no coincide con el certificado, se devuelve ERROR \_ ACCESS \_ DENIED. Si el formato de nombre no es válido, SCHANNEL SSP devuelve el código ERROR \_ INVALID \_ PARAMETER.

Para consultar el nombre principal del servidor, las aplicaciones pueden llamar a [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname). Esto asigna una cadena terminada en NULL para contener el nombre principal. Antes de finalizar, la aplicación debe invocar [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para liberar la memoria que ocupa esta cadena.

La consulta del nombre del servidor de esta manera no es segura y debe evitarse. Para la autenticación del servidor, el programa cliente debe saber a qué servidor se está conectando y debe crear el nombre principal del servidor desde cero.

 

 




