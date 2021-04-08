---
title: Sondear los cambios mediante el control DirSync
description: Active Directory control de sincronización de directorios (DirSync) es una extensión de servidor LDAP que permite que una aplicación busque en una partición de directorio objetos que han cambiado desde un estado anterior.
ms.assetid: f77caeb3-bfc9-4ae6-8d1d-73f4ee554336
ms.tgt_platform: multiple
keywords:
- Sondear los cambios mediante el control DirSync AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d105757d39bc25bd10df21ab68c4d1d1202be
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789502"
---
# <a name="polling-for-changes-using-the-dirsync-control"></a>Sondear los cambios mediante el control DirSync

Active Directory control de sincronización de directorios (DirSync) es una extensión de servidor LDAP que permite que una aplicación busque en una partición de directorio objetos que han cambiado desde un estado anterior.

Use el control DirSync a través de ADSI especificando la preferencia de búsqueda de **\_ \_ DirSync de ADS SEARCHPREF** al usar [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch). Para obtener más información y un ejemplo de código, vea [código de ejemplo con ADS \_ SEARCHPREF \_ DirSync](example-code-using-ads-searchpref-dirsync.md). También puede realizar una búsqueda de DirSync mediante la API de LDAP. A continuación se describe la implementación de ADSI, la mayoría de las cuales también se aplica al uso de LDAP directamente, excepto como se describe al final de este tema.

Al realizar una búsqueda de DirSync, se pasa un elemento de datos específico del proveedor (cookie) que identifica el estado del directorio en el momento de la búsqueda de DirSync anterior. En la primera búsqueda, se pasa una cookie NULL y la búsqueda devuelve todos los objetos que coinciden con el filtro. La búsqueda también devuelve una cookie válida. Almacene la cookie en el mismo almacenamiento que está sincronizando con el servidor de Active Directory. En las búsquedas posteriores, obtenga la cookie del almacenamiento y pásela con la solicitud de búsqueda. Los resultados de la búsqueda ahora incluyen solo los objetos y atributos que han cambiado desde el estado anterior identificado por la cookie. La búsqueda también devuelve una cookie nueva que se va a almacenar para la siguiente búsqueda.

En la tabla siguiente se enumeran los parámetros de búsqueda que la solicitud de búsqueda de cliente puede especificar.



| Parámetro          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Base de la búsqueda | La base de una búsqueda de DirSync debe ser la raíz de una partición de directorio, que puede ser una partición de dominio, la partición de configuración o la partición de esquema.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Ámbito              | El ámbito de una búsqueda de DirSync debe **ser \_ \_ subárbol de ámbito de ADS**, es decir, todo el subárbol de la partición. Tenga en cuenta que para una búsqueda de una partición de dominio, el subárbol incluye los cabezales, pero no el contenido, de las particiones de esquema y de configuración. Para sondear los cambios en un ámbito más pequeño, use la técnica de **USNChanged** en lugar de DirSync.                                                                                                                                                                                                                                                                                                                                                                                 |
| Filter             | Puede especificar cualquier filtro de búsqueda válido. En el caso de una búsqueda inicial con una cookie null, los resultados incluyen todos los objetos que coinciden con el filtro. En las búsquedas posteriores con una cookie válida, los resultados de la búsqueda incluyen datos solo de los objetos que coinciden con el filtro y que han cambiado desde el estado indicado por la cookie. Para obtener más información acerca de los filtros de búsqueda, consulte [crear un filtro de consulta](creating-a-query-filter.md).                                                                                                                                                                                                                                                                                                                |
| Atributos         | Puede especificar una lista de atributos que se devolverán cuando se produzca un cambio. Para cada objeto, los resultados iniciales incluyen todos los atributos solicitados establecidos en el objeto. Los resultados de búsqueda posteriores incluyen solo los atributos especificados que han cambiado. Los atributos sin modificar no se incluyen en los resultados de la búsqueda. En la implementación de ADSI, los resultados de la búsqueda siempre incluyen **objectGUID** y **instanceType** de cada objeto. Además, la lista de atributos especificada actúa como filtro adicional: los resultados de la búsqueda inicial incluyen solo los objetos que tienen al menos uno de los atributos especificados. las búsquedas posteriores incluyen solo los objetos en los que han cambiado uno o varios de los atributos (valores agregados o eliminados). |



 

Además, tenga en cuenta lo siguiente:

-   En las búsquedas incrementales, el procedimiento recomendado es enlazar al mismo controlador de dominio (DC) usado en la búsqueda anterior, es decir, el controlador de dominio que generó la cookie. Si el mismo controlador de dominio no está disponible, espere hasta que sea o enlace a un nuevo controlador de dominio y realice una sincronización completa. Almacene el nombre DNS del controlador de dominio en el almacenamiento secundario con la cookie.

    Puede pasar una cookie generada por un controlador de dominio a otro controlador de dominio que hospede una réplica de la misma partición de directorio. No existe la posibilidad de que un cliente no se pierda los cambios mediante una cookie de un controlador de dominio en otro controlador de dominio. Sin embargo, es posible que los resultados de la búsqueda del nuevo controlador de dominio incluyan cambios detectados por el controlador de dominio antiguo. en algunos casos, el nuevo controlador de dominio puede devolver todos los objetos y atributos, como con una sincronización completa. El cliente solo debe hacer que su base de datos sea coherente con los resultados de la búsqueda detectada para cualquier llamada de DirSync determinada, es decir, controlar todos los resultados incrementales como si fueran el estado más reciente. No importa si ha detectado el cambio antes o incluso si vuelve a un estado anterior, ya que las sincronizaciones incrementales repetidas convergerán en la coherencia.

-   Cuando se cambia el nombre de un objeto o se mueve, sus objetos secundarios, si los hay, no se incluyen en los resultados de la búsqueda, aunque los nombres distintivos de los objetos secundarios hayan cambiado. Del mismo modo, cuando se modifica una ACE heredable en un descriptor de seguridad de objeto, los objetos secundarios del objeto no se incluyen en los resultados de la búsqueda, aunque los descriptores de seguridad de los objetos secundarios hayan cambiado.
-   Use el atributo **objectGUID** para identificar los objetos sometidos a seguimiento. El **objectGUID** de cada objeto permanece sin modificar, independientemente de dónde se mueva el objeto dentro del bosque.
-   Tenga en cuenta que los resultados de la búsqueda de una búsqueda de DirSync indican el estado de los objetos en una réplica de la partición de directorio en el momento de la búsqueda. Esto significa que los cambios realizados en otros controladores de dominio no se incluirán si no se han replicado en el controlador de dominio de destino. También significa que los atributos de un objeto pueden haber cambiado varias veces desde la búsqueda de DirSync anterior, pero la búsqueda solo mostrará el estado final, no la secuencia de cambios.
-   En la implementación de ADSI, la aplicación debe controlar la cookie como opaca y no hacer ninguna suposición sobre su valor o organización interna.
-   Tenga en cuenta que el cliente almacena la cookie, la longitud de la cookie y el nombre DNS del controlador de dominio en el mismo almacenamiento que contiene los datos del objeto sincronizado. Esto garantiza que la cookie y otros parámetros permanecen sincronizados con los datos del objeto si el almacenamiento se restaura a partir de una copia de seguridad.
-   Para recuperar el atributo [**parentGUID**](/windows/desktop/ADSchema/a-parentguid) , que se construye para el control DirSync, también es necesario solicitar el atributo [**Name**](/windows/desktop/ADSchema/a-name) .

Para usar el control DirSync, el autor de la llamada debe tener el derecho "obtener cambios de directorio" asignado en la raíz de la partición que se está supervisando. De forma predeterminada, este derecho se asigna a las cuentas de administrador y LocalSystem en los controladores de dominio. El autor de la llamada también debe tener el derecho de acceso de control extendido [**DS-Replication-Get-Changes**](/windows/desktop/ADSchema/r-ds-replication-get-changes) . Para obtener más información acerca de la implementación de un mecanismo de seguimiento de cambios para las aplicaciones que se deben ejecutar en una cuenta que no tiene este derecho, consulte [sondear los cambios con USNChanged](polling-for-changes-using-usnchanged.md). Para obtener más información sobre los privilegios, vea [privilegios](/windows/desktop/SecAuthZ/privileges).

## <a name="retrieving-deleted-objects-with-a-dirsync-search"></a>Recuperar objetos eliminados con una búsqueda de DirSync

Los resultados de búsqueda de **\_ SEARCHPREF de \_ DirSync de ADS** incluyen automáticamente los objetos eliminados (marcadores de exclusión) que coinciden con el filtro de búsqueda especificado. Sin embargo, un filtro de búsqueda que coincida con un objeto cuando esté activo puede no coincidir con el objeto después de eliminarlo. Esto se debe a que los marcadores de exclusión conservan solo un subconjunto de los atributos presentes en el objeto original. Por ejemplo, normalmente usaría el siguiente filtro para objetos de usuario.


```C++
(&(objectClass=user)(objectCategory=person))
```



El atributo **objectCategory** se quita cuando se elimina un objeto, por lo que el filtro anterior no coincidiría con ninguno de los objetos de desecho. Por el contrario, el atributo **objectClass** se conserva en los objetos de desecho, por lo que un filtro de "(objectClass = User)" coincidiría con los objetos de usuario eliminados.

La lista de atributos que se especifica con una búsqueda de DirSync también actúa como filtro; los resultados de la búsqueda incluyen solo los objetos en los que uno o varios de los atributos especificados han cambiado desde la última búsqueda de DirSync. Si la lista de atributos no incluye ningún atributo que se retenga en los marcadores de exclusión, los resultados de la búsqueda no incluirán marcadores de exclusión. Para controlar esto, solicite todos los atributos especificando una lista de atributos null. o bien, puede solicitar el atributo **IsDeleted** , establecido en **true** en todos los marcadores de exclusión. Los atributos de desecho tienen el bit 0x8 establecido en el atributo **searchFlags** de la definición de **attributeSchema** .

Para obtener más información, vea [recuperar objetos eliminados](retrieving-deleted-objects.md).

## <a name="ldap-implementation-of-the-dirsync-control"></a>Implementación LDAP del control DirSync

También puede realizar una búsqueda de DirSync mediante la API LDAP con el control [ \_ OID de \_ DirSync \_ del servidor LDAP](/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid) . Si usa la API de LDAP, especifique también el [ \_ \_ \_ \_ OID DN extendido del servidor LDAP](/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid) y el [ \_ servidor LDAP Mostrar controles \_ \_ \_ OID eliminados](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) . El \_ \_ control OID DN extendido del servidor LDAP \_ hace que \_ una búsqueda LDAP devuelva una forma extendida del nombre distintivo que incluye **objectGUID** y **objectSid** para objetos de entidad de seguridad, como usuarios, grupos y equipos. El \_ servidor LDAP \_ Mostrar \_ \_ control de OID eliminado hace que los resultados de la búsqueda incluyan los datos de los objetos eliminados. Tenga en cuenta que estos controles se incluyen automáticamente en la implementación de ADSI.

 

 