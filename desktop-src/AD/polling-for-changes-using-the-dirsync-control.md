---
title: Sondeo de cambios mediante el control DirSync
description: Active Directory sincronización de directorios (DirSync) es una extensión de servidor LDAP que permite a una aplicación buscar en una partición de directorio objetos que han cambiado desde un estado anterior.
ms.assetid: f77caeb3-bfc9-4ae6-8d1d-73f4ee554336
ms.tgt_platform: multiple
keywords:
- Sondeo de cambios mediante dirsync control AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b95e9fed93a962ef95e8cdbe08c202bd8e46df21959d9e1fcabe8eac033b6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185412"
---
# <a name="polling-for-changes-using-the-dirsync-control"></a>Sondeo de cambios mediante el control DirSync

Active Directory sincronización de directorios (DirSync) es una extensión de servidor LDAP que permite a una aplicación buscar en una partición de directorio objetos que han cambiado desde un estado anterior.

Use el control DirSync a través de ADSI especificando la preferencia de búsqueda **\_ SEARCHPREF \_ DIRSYNC de ADS** al usar [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch). Para obtener más información y un ejemplo de código, vea Ejemplo de código [mediante \_ ADS SEARCHPREF \_ DIRSYNC](example-code-using-ads-searchpref-dirsync.md). También puede realizar una búsqueda de DirSync mediante la API LDAP. A continuación se describe la implementación de ADSI, la mayoría de las cuales también se aplica al uso de LDAP directamente, excepto como se describe al final de este tema.

Al realizar una búsqueda de DirSync, se pasa un elemento de datos específico del proveedor (cookie) que identifica el estado del directorio en el momento de la búsqueda anterior de DirSync. Para la primera búsqueda, se pasa una cookie null y la búsqueda devuelve todos los objetos que coinciden con el filtro. La búsqueda también devuelve una cookie válida. Almacene la cookie en el mismo almacenamiento que está sincronizando con el Active Directory servidor. En las búsquedas posteriores, obtenga la cookie del almacenamiento y pásala con la solicitud de búsqueda. Los resultados de la búsqueda ahora incluyen solo los objetos y atributos que han cambiado desde el estado anterior identificado por la cookie. La búsqueda también devuelve una nueva cookie que se almacenará para la siguiente búsqueda.

En la tabla siguiente se enumeran los parámetros de búsqueda que puede especificar la solicitud de búsqueda de cliente.



| Parámetro          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Base de la búsqueda | La base de una búsqueda de DirSync debe ser la raíz de una partición de directorio, que puede ser una partición de dominio, la partición de configuración o la partición de esquema.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Ámbito              | El ámbito de una búsqueda de DirSync debe ser **ADS \_ SCOPE \_ SUBTREE**, es decir, el subárbol completo de la partición. Tenga en cuenta que, para realizar una búsqueda de una partición de dominio, el subárbol incluye las caras, pero no el contenido, de las particiones de configuración y esquema. Para sondear los cambios en un ámbito más pequeño, use la **técnica USNChanged** en lugar de DirSync.                                                                                                                                                                                                                                                                                                                                                                                 |
| Filtrar             | Puede especificar cualquier filtro de búsqueda válido. Para una búsqueda inicial con una cookie null, los resultados incluyen todos los objetos que coinciden con el filtro. Para las búsquedas posteriores con una cookie válida, los resultados de la búsqueda incluyen datos solo para los objetos que coinciden con el filtro y han cambiado desde el estado indicado por la cookie. Para obtener más información sobre los filtros de búsqueda, vea [Crear un filtro de consulta.](creating-a-query-filter.md)                                                                                                                                                                                                                                                                                                                |
| Atributos         | Puede especificar una lista de atributos que se devolverán cuando se produzca un cambio. Para cada objeto, los resultados iniciales incluyen todos los atributos solicitados establecidos en el objeto . Los resultados de búsqueda posteriores incluyen solo los atributos especificados que han cambiado. Los atributos sin modificar no se incluyen en los resultados de la búsqueda. En la implementación de ADSI, los resultados de la búsqueda siempre incluyen **el objectGUID** **y instanceType** de cada objeto. Además, la lista de atributos especificada actúa como filtro adicional: los resultados de búsqueda iniciales incluyen solo objetos que tienen al menos uno de los atributos especificados establecidos; Las búsquedas posteriores incluyen solo objetos en los que uno o varios de los atributos han cambiado (valores agregados o eliminados). |



 

Además, tenga en cuenta que:

-   Para las búsquedas incrementales, el procedimiento recomendado es enlazar con el mismo controlador de dominio (DC) usado en la búsqueda anterior, es decir, el controlador de dominio que generó la cookie. Si el mismo controlador de dominio no está disponible, espere hasta que esté o enlace a un nuevo controlador de dominio y realice una sincronización completa. Almacene el nombre DNS del controlador de dominio en el almacenamiento secundario con la cookie.

    Puede pasar una cookie generada por un controlador de dominio a otro controlador de dominio que hospeda una réplica de la misma partición de directorio. No hay ninguna posibilidad de que un cliente pierda los cambios mediante el uso de una cookie de un controlador de dominio en otro controlador de dominio. Sin embargo, es posible que los resultados de la búsqueda del nuevo controlador de dominio puedan incluir cambios notificados por el controlador de dominio anterior. En algunos casos, el nuevo controlador de dominio puede devolver todos los objetos y atributos, como con una sincronización completa. El cliente debe hacer que su base de datos sea coherente con los resultados de búsqueda notificados para cualquier llamada a DirSync determinada, es decir, controlar todos los resultados incrementales como si fueran el estado más reciente. No importa si ha visto el cambio antes o si va a volver a un estado anterior porque las sincronizaciones incrementales repetidas convergerán en la coherencia.

-   Cuando se cambia el nombre de un objeto o se mueve, sus objetos secundarios, si los hay, no se incluyen en los resultados de la búsqueda, aunque los nombres distintivos de los objetos secundarios han cambiado. Del mismo modo, cuando se modifica una ACE heredable en un descriptor de seguridad de objeto, los objetos secundarios del objeto no se incluyen en los resultados de la búsqueda, aunque los descriptores de seguridad de los objetos secundarios han cambiado.
-   Use el **atributo objectGUID** para identificar los objetos de los que se realiza el seguimiento. El **objectGUID de** cada objeto permanece sin cambios, independientemente de dónde se mueve el objeto dentro del bosque.
-   Tenga en cuenta que los resultados de la búsqueda de una búsqueda de DirSync indican el estado de los objetos en una réplica de la partición de directorio en el momento de la búsqueda. Esto significa que los cambios realizados en otros DC no se incluirán si no se han replicado en el controlador de dominio de destino. También significa que los atributos de un objeto pueden haber cambiado varias veces desde la búsqueda anterior de DirSync, pero la búsqueda mostrará solo el estado final, no la secuencia de cambios.
-   En la implementación de ADSI, la aplicación debe controlar la cookie como opaca y no hacer suposiciones sobre su organización o valor interno.
-   Tenga en cuenta que el cliente almacena la cookie, la longitud de la cookie y el nombre DNS del controlador de dominio en el mismo almacenamiento que contiene los datos del objeto sincronizado. Esto garantiza que la cookie y otros parámetros permanecen sincronizados con los datos del objeto si el almacenamiento se restaura alguna vez a partir de una copia de seguridad.
-   Para recuperar el [**atributo parentGUID,**](/windows/desktop/ADSchema/a-parentguid) que se construye para el control DirSync, también es necesario solicitar el atributo [**name.**](/windows/desktop/ADSchema/a-name)

Para usar el control DirSync, el autor de la llamada debe tener asignado el derecho "directory get changes" en la raíz de la partición que se está supervisando. De forma predeterminada, este derecho se asigna a las cuentas Administrador y LocalSystem en controladores de dominio. El autor de la llamada también debe tener el derecho de acceso extendido de control [**DS-Replication-Get-Changes.**](/windows/desktop/ADSchema/r-ds-replication-get-changes) Para obtener más información sobre cómo implementar un mecanismo de seguimiento de cambios para las aplicaciones que deben ejecutarse con una cuenta que no tiene este derecho, vea Sondeo de cambios mediante [USNChanged](polling-for-changes-using-usnchanged.md). Para obtener más información sobre los privilegios, vea [Privileges](/windows/desktop/SecAuthZ/privileges).

## <a name="retrieving-deleted-objects-with-a-dirsync-search"></a>Recuperar objetos eliminados con una búsqueda de DirSync

Los **resultados \_ de búsqueda DE ADS SEARCHPREF \_ DIRSYNC** incluyen automáticamente objetos eliminados (objetos de desecho) que coinciden con el filtro de búsqueda especificado. Sin embargo, es posible que un filtro de búsqueda que coincida con un objeto cuando esté en directo no coincida con el objeto después de eliminarlo. Esto se debe a que los objetos de desecho conservan solo un subconjunto de los atributos presentes en el objeto original. Por ejemplo, normalmente usaría el siguiente filtro para los objetos de usuario.


```C++
(&(objectClass=user)(objectCategory=person))
```



El **atributo objectCategory** se quita cuando se elimina un objeto, por lo que el filtro anterior no coincidiría con ningún objeto de lápida. Por el contrario, el atributo **objectClass** se conserva en objetos de desecho, por lo que un filtro de "(objectClass=user)" coincidiría con los objetos de usuario eliminados.

La lista de atributos que especifique con una búsqueda de DirSync también actúa como filtro; Los resultados de la búsqueda incluyen solo objetos en los que uno o varios de los atributos especificados han cambiado desde la búsqueda anterior de DirSync. Si la lista de atributos no incluye ningún atributo que se conserve en los objetos de desecho, los resultados de la búsqueda no incluirán los de desecho. Para controlar esto, solicite todos los atributos especificando una lista de atributos NULL; o bien puede solicitar el **atributo isDeleted,** establecido en **TRUE** en todos los objetos de desecho. Los atributos de desecho tienen el 0x8 bits establecido en el atributo **searchFlags** de la **definición attributeSchema.**

Para obtener más información, [vea Recuperar objetos eliminados.](retrieving-deleted-objects.md)

## <a name="ldap-implementation-of-the-dirsync-control"></a>Implementación LDAP del control DirSync

También puede realizar una búsqueda de DirSync mediante la API LDAP con el control [ \_ \_ \_ OID LDAP SERVER DIRSYNC.](/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid) Si usa la API LDAP, especifique también los controles [ \_ \_ \_ \_ OID DE LDAP SERVER EXTENDED DN](/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid) y [LDAP SERVER SHOW DELETED \_ \_ \_ \_ OID.](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) El control OID de DN EXTENDIDO DE LDAP SERVER hace que una búsqueda LDAP devuelva una forma extendida del nombre distintivo que incluye \_ \_ \_ \_ **objectGUID** y **objectSID** para objetos de entidad de seguridad como usuarios, grupos y equipos. El control OID SHOW DELETED de LDAP SERVER hace que los resultados de \_ \_ la búsqueda \_ \_ incluyan datos para los objetos eliminados. Tenga en cuenta que estos controles se incluyen automáticamente en la implementación de ADSI.

 

 