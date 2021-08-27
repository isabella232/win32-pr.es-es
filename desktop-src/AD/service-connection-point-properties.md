---
title: Propiedades del punto de conexión de servicio
description: Los atributos de la clase serviceConnectionPoint son suficientes para la mayoría de los servicios.
ms.assetid: 08888d2c-b46e-4b86-87e4-0c061ea147a0
ms.tgt_platform: multiple
keywords:
- Propiedades del punto de conexión de servicio
- puntos de conexión de servicio ad , propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1343833d1a61e4df6dfc44238f9f094b00844f0b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473491"
---
# <a name="service-connection-point-properties"></a>Propiedades del punto de conexión de servicio

Los atributos de la **clase serviceConnectionPoint** son suficientes para la mayoría de los servicios. Active Directory Domain Services definir cómo se usan los atributos, por lo que los clientes del servicio deben ser capaces de interpretar y usar los datos en los SCP de servicio. Los servicios que deben publicar datos adicionales sobre sí mismos pueden extender el esquema Active Directory mediante la creación de una subclase de la **clase serviceConnectionPoint,** dando a la subclase un nombre distinto. Para obtener más información sobre las extensiones de esquema, vea [Extender el esquema](extending-the-schema.md).

Los atributos más importantes de un SCP son las palabras clave **,** **serviceDNSName**, **serviceDNSNameType**, **serviceClassName** y **serviceBindingInformation**. Las aplicaciones cliente buscan en el directorio **valores de palabras clave** para buscar el SCP. Cuando se encuentra el SCP, los clientes pueden leer otros atributos para recuperar los datos del servicio.




| Atributo | Descripción | 
|-----------|-------------|
| <strong>Palabras clave</strong><br /> | El <strong>atributo keywords</strong> puede contener varios valores de cadena que identifican el servicio. Este atributo se incluye en el catálogo global, lo que significa que los clientes de cualquier dominio de un bosque empresarial pueden buscar en el catálogo global palabras clave asociadas al servicio. Este atributo también está indexado, lo que mejora el rendimiento de las consultas. El instalador que crea el SCP establece los valores del atributo <strong>keywords.</strong> Normalmente, el servicio activo no modifica estos valores.<br /> Las palabras clave exactas que debe incluir en el SCP dependen de cómo los clientes busquen el servicio. Las mejores palabras clave para usar son cadenas GUID porque se garantiza que los GUID sean únicos en un bosque. Use el formato de cadena GUID devuelto por <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>la función UuidToString</strong></a> en la biblioteca RPC. También puede incluir nombres legibles para personas, si los clientes pueden usarlos para buscar el servicio. Las palabras clave de un SCP deben incluir cadenas GUID o nombres que identifiquen los datos siguientes sobre el servicio:<ul><li>Su empresa u organización: por ejemplo, Fabrikam.</li><li>El producto o servicio: por ejemplo, SQL Server. Esto permite a las aplicaciones cliente buscar SCP para servicios de ese tipo.</li><li>Versión específica del producto o servicio, como 7.5.</li><li>Para los SCP que publican un conjunto específico de datos o funcionalidades para un tipo de servicio, incluya una cadena o un nombre GUID que identifique la instancia específica. Por ejemplo, un servicio de base de datos podría publicar un SCP para una base de datos específica. En este caso, el SCP incluiría un GUID de producto para identificar el servicio y otro GUID para identificar la base de datos.</li></ul><br /> | 
| <strong>serviceDNSName y</strong> <strong>serviceDNSNameType</strong><br /> | Las aplicaciones cliente usan <strong>los atributos serviceDNSName</strong> y <strong>serviceDNSNameType</strong> para determinar el equipo host del servicio. El valor <strong>serviceDNSNameType</strong> indica el tipo de nombre DNS especificado por <strong>serviceDNSName</strong> normalmente "A" si <strong>serviceDNSName</strong> contiene un nombre de host o "SRV" si <strong>serviceDNSName</strong> contiene un nombre de registro SRV.<br /> El <strong>valor serviceDNSName</strong> suele ser el nombre DNS del equipo host del servicio. El instalador del servicio puede llamar a <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>la función GetComputerNameEx</strong></a> para obtener el nombre DNS del equipo local.<br /> Para los servicios que tienen registros SRV de DNS, <strong>serviceDNSName</strong> puede ser el nombre del registro SRV. Una aplicación cliente usa las API dns para recuperar todos los registros SRV que coinciden con este nombre. A continuación, el cliente recupera el nombre de host DNS de uno de los registros SRV. Esta técnica es útil para los servicios replicados porque los registros SRV también incluyen datos que permiten al cliente seleccionar la mejor réplica.<br /> | 
| <strong>serviceBindingInformation</strong><br /> | Propiedad de varios valores que contiene valores de cadena que almacenan los datos necesarios para enlazar a un servicio. Esta propiedad se indexa y se replica en el catálogo global.<br /> El contenido de <strong>serviceBindingInformation</strong> es específico del servicio que publicó el SCP; los clientes deben interpretar los datos de enlace. En el caso más común, los datos de enlace constan de un número de puerto en el equipo host de servicio.<br /> | 
| <strong>serviceClassName</strong><br /> | Propiedad de un solo valor que identifica la clase de servicio representada por el SCP. Se trata de una cadena descriptiva específica del servicio que publicó el SCP; por ejemplo, SqlServer. En el caso de los servicios que admiten la autenticación mutua, los clientes pueden usar esta propiedad, junto con el nombre DNS del equipo host del servicio, para formar un nombre de entidad de seguridad de servicio. Para obtener más información, vea <a href="mutual-authentication-using-kerberos.md">Autenticación mutua mediante Kerberos.</a><br /> | 




 

 

