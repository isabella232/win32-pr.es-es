---
title: Nombres principales
description: Para que un cliente cree una sesión autenticada mutuamente con un programa de servidor, debe proporcionar el nombre de la entidad de seguridad esperada del servidor.
ms.assetid: 4d9977f8-0efb-4559-977e-3eba4e277bc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554ffecff6eb019b4712e6b2d9f5c6319db492e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486987"
---
# <a name="principal-names"></a>Nombres principales

Para que un cliente cree una sesión autenticada mutuamente con un programa de servidor, debe proporcionar el nombre de la entidad de seguridad esperada del servidor. Algunos protocolos, como Kerberos, requieren un nombre de entidad de seguridad de servidor correcto para cualquier sesión autenticada. Una entidad de seguridad es una entidad que el sistema de seguridad reconoce. Esto incluye a los usuarios humanos, así como a los servicios del sistema. Todos los nombres principales tienen un formato similar para un proveedor de compatibilidad de seguridad (SSP) determinado. Un SSP es un módulo de software que realiza la validación de seguridad. Para obtener más información, vea [información general sobre la arquitectura de SSPI](sspi-architectural-overview.md). Para mantener la uniformidad, un proveedor de seguridad suele proporcionar nombres similares a los servicios del sistema como usuarios. En algunos proveedores de seguridad, es posible que los servicios del sistema no tengan un nombre principal.

El servidor registra su nombre principal para el proveedor de seguridad mediante la función [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) . Solo se puede usar un nombre principal de servidor para cada proveedor de seguridad. Si se registra más de un nombre, se elige y se utiliza un nombre de forma aleatoria. El SSP dicta el formato del nombre de la entidad de seguridad. Por ejemplo, el SSP de Kerberos/Negotiate para un servicio de sistema de tiene una apariencia similar a la siguiente: nombre del equipo \_ $ @childdomain.parentdomain1.parentdomain2.COM .

El procedimiento recomendado para generar nombres principales es usar API documentadas (como la función **DsMakeSpn** ), en lugar de juntar juntas el nombre principal de las cadenas. El uso de API documentadas aumenta la portabilidad entre distintos entornos de implementación y elimina la posibilidad de que se produzcan errores.

Si se especifica un nombre de entidad de seguridad incorrecto, puede impedir que el cliente y el servidor establezcan una sesión autenticada. SCHANNEL SSP toma los nombres principales en cualquiera de las dos formas siguientes:

-   El primer formulario de nombre principal de SCHANNEL es el formulario [*msstd*](m-glos.md) . Los nombres en forma de msstd suelen seguir el patrón msstd:servername@serverdomain.com . Esto se conoce como una propiedad de nombre de correo electrónico. Si el certificado contiene una propiedad de nombre de correo electrónico y contiene el signo (@), el nombre de la entidad de seguridad es msstd: nombre de correo electrónico. En caso contrario, debe contener la propiedad common name. Las barras diagonales inversas internas se duplican, al igual que en los enlaces de cadena.
-   El segundo formulario de nombre principal de SCHANNEL es el formulario [*fullsic*](f-glos.md) . Se trata de una serie de nombres compatibles con RFC1779 delimitados por corchetes angulares y separados por barras diagonales inversas. Normalmente sigue el patrón fullsic: \\ < \\ entidad de \\ subautor \\ .. \\ .. Person> o fullsic: \\ < \\ entidad de \\ subautor \\ .. \\ ..> ServerProgram.

Si el nombre no coincide con el certificado, \_ se devuelve el error acceso \_ denegado. Si el formato de nombre no es válido, SCHANNEL SSP devuelve el parámetro de ERROR de código \_ no válido \_ .

Para consultar el nombre de la entidad de seguridad del servidor, las aplicaciones pueden llamar a [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname). Esto asigna una cadena terminada en null para contener el nombre de la entidad de seguridad. Antes de que finalice, la aplicación debe invocar [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para liberar la memoria que ocupa esta cadena.

La consulta del nombre del servidor de esta manera no es segura y debe evitarse. Para la autenticación de servidor, el programa cliente debe saber a qué servidor se está conectando y debe crear el nombre de la entidad de seguridad del servidor desde el principio.

 

 




