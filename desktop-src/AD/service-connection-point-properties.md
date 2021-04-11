---
title: Propiedades de punto de conexión de servicio
description: Los atributos de la clase serviceConnectionPoint son suficientes para la mayoría de los servicios.
ms.assetid: 08888d2c-b46e-4b86-87e4-0c061ea147a0
ms.tgt_platform: multiple
keywords:
- Propiedades de punto de conexión de servicio
- puntos de conexión de servicio AD, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511bbba8acf50a185f1bdd8b55d9b7f8ce684817
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149165"
---
# <a name="service-connection-point-properties"></a>Propiedades de punto de conexión de servicio

Los atributos de la clase **serviceConnectionPoint** son suficientes para la mayoría de los servicios. Active Directory Domain Services no definen cómo se usan los atributos, por lo que los clientes de su servicio deben ser capaces de interpretar y usar los datos de los SCP de servicio. Los servicios que deben publicar datos adicionales sobre sí mismos pueden extender el esquema de Active Directory mediante la creación de una subclase de la clase **serviceConnectionPoint** , lo que asigna a la subclase un nombre distinto. Para obtener más información acerca de las extensiones de esquema, consulte [extender el esquema](extending-the-schema.md).

Los atributos más importantes de un SCP son **Keywords**, **serviceDNSName**, **serviceDNSNameType**, **serviceClassName** y **serviceBindingInformation**. Las aplicaciones cliente buscan valores de **palabras clave** en el directorio para buscar el SCP. Cuando se encuentra el SCP, los clientes pueden leer otros atributos para recuperar los datos del servicio.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>palabra</strong><br/></td>
<td>El atributo <strong>Keywords</strong> puede contener varios valores de cadena que identifican el servicio. Este atributo se incluye en el catálogo global, lo que significa que los clientes de cualquier dominio de un bosque de empresa pueden buscar palabras clave asociadas con el servicio en el catálogo global. Este atributo también está indexado, lo que mejora el rendimiento de las consultas. El instalador que crea el SCP establece los valores del atributo <strong>Keywords</strong> . Normalmente, estos valores no son modificados por el servicio activo.<br/> Las palabras clave exactas que debe incluir en el SCP dependen de cómo los clientes buscan su servicio. Las mejores palabras clave que se usan son cadenas GUID porque se garantiza que los GUID son únicos en un bosque. Use el formato de cadena de GUID devuelto por la función <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>UuidToString</strong></a> de la biblioteca RPC. También puede incluir nombres legibles, si los clientes pueden usarlos para buscar el servicio. Las palabras clave de un SCP deben incluir cadenas de GUID y/o nombres que identifiquen los siguientes datos sobre el servicio:
<ul>
<li>Su empresa u organización: por ejemplo, fabrikam.</li>
<li>El producto o servicio: por ejemplo, SQL Server. Esto permite a las aplicaciones cliente buscar SCP para los servicios de ese tipo.</li>
<li>La versión específica del producto o servicio, como 7,5.</li>
<li>En el caso de los SCP que publican un conjunto específico de datos o funcionalidades para un tipo de servicio, incluya una cadena o un nombre GUID que identifique la instancia específica. Por ejemplo, un servicio de base de datos podría publicar un SCP para una base de datos específica. En este caso, el SCP incluiría un GUID del producto para identificar el servicio y otro GUID para identificar la base de datos.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>serviceDNSName</strong> y <strong>serviceDNSNameType</strong><br/></td>
<td>Las aplicaciones cliente usan los atributos <strong>serviceDNSName</strong> y <strong>serviceDNSNameType</strong> para determinar el equipo host del servicio. El valor <strong>serviceDNSNameType</strong> indica el tipo de nombre DNS especificado por <strong>serviceDNSName</strong> normalmente &quot; un &quot; si <strong>serviceDNSName</strong> contiene un nombre de host o &quot; SRV &quot; si <strong>serviceDNSName</strong> contiene un nombre de registro SRV.<br/> El valor de <strong>serviceDNSName</strong> es normalmente el nombre DNS del equipo host del servicio. El instalador del servicio puede llamar a la función <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>GetComputerNameEx</strong></a> para obtener el nombre DNS del equipo local.<br/> En el caso de los servicios que tienen registros de servidor DNS, <strong>serviceDNSName</strong> puede ser el nombre del registro SRV. Una aplicación cliente utiliza las API de DNS para recuperar todos los registros SRV que coinciden con este nombre. A continuación, el cliente recupera el nombre de host DNS de uno de los registros SRV. Esta técnica es útil para los servicios replicados porque los registros SRV también incluyen datos que permiten al cliente seleccionar la mejor réplica.<br/></td>
</tr>
<tr class="odd">
<td><strong>serviceBindingInformation</strong><br/></td>
<td>Propiedad de varios valores que contiene valores de cadena que almacenan los datos necesarios para enlazar a un servicio. Esta propiedad está indizada y se replica en el catálogo global.<br/> El contenido de <strong>serviceBindingInformation</strong> es específico del servicio que publicó el SCP; los clientes deben interpretar los datos de enlace. En el caso más común, los datos de enlace se componen de un número de puerto en el equipo host del servicio.<br/></td>
</tr>
<tr class="even">
<td><strong>serviceClassName</strong><br/></td>
<td>Propiedad de un solo valor que identifica la clase de servicio representada por el SCP. Se trata de una cadena descriptiva específica del servicio que publicó el SCP; por ejemplo, SqlServer. En el caso de los servicios que admiten la autenticación mutua, los clientes pueden usar esta propiedad, junto con el nombre DNS del equipo host del servicio, para formar un nombre de entidad de seguridad de servicio. Para obtener más información, vea <a href="mutual-authentication-using-kerberos.md">autenticación mutua mediante Kerberos</a>.<br/></td>
</tr>
</tbody>
</table>



 

 

