---
title: Buscar Active Directory
description: Una función importante de Active Directory consiste en resolver las consultas de datos para los usuarios, así como los datos de configuración de los equipos y servicios.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Buscar Active Directory ADSI
- ADSI ADSI, buscar Active Directory
- consultas ADSI, buscar Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356692"
---
# <a name="searching-active-directory"></a>Buscar Active Directory

Una función importante de Active Directory consiste en resolver las consultas de datos para los usuarios, así como los datos de configuración de los equipos y servicios. Para escribir consultas eficaces para Active Directory, resulta útil estar familiarizado con lo siguiente:

-   Determinar el ámbito de la consulta: ¿debe encontrar el cliente las propiedades de los objetos que pueden encontrarse en cualquier lugar dentro de un bosque, solo dentro de un dominio o en una unidad organizativa (OU) determinada?
-   Determinar la profundidad de la consulta: ¿la consulta solo debe buscar un nivel o podría cruzarse en otros directorios LDAP?
-   Rendimiento y control de grandes conjuntos de resultados: ¿Cómo debe el cliente controlar eficazmente el potencial de un conjunto de resultados grande?
-   Determinar las mejores consultas: ¿Qué tipo de consultas proporcionan los resultados más eficaces? ¿Qué tipo de consultas debe evitar el desarrollador?
-   Descripción de la sintaxis de las consultas: ADSI admite la sintaxis LDAP tal y como se documenta en RFC 2254, así como un subconjunto de SQL.
-   Elección de interfaces: ADSI proporciona compatibilidad con OLE DB, así como una interfaz de C/C++ denominada [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). Dado que ADSI funciona para varios espacios de nombres, puede utilizar estas interfaces para consultar otros espacios de nombres, como Exchange, así como Active Directory. Dado que el objeto de datos ActiveX (ADO) es un modelo de objetos de acceso a datos sencillo que se puede incluir en scripts sobre OLE DB, las interfaces de OLE DB funcionan bien para los programadores de Visual Basic y los escritores de scripts de página web. Las nuevas características de acceso a datos dentro de Visual Studio y las aplicaciones de Office que aprovechan las ventajas de ADO y OLE DB ahora pueden tener acceso a los datos de Active Directory de la misma manera que obtienen acceso a los datos de otros proveedores de OLE DB, como SQL Server. Sin embargo, si un desarrollador de C/C++ debe realizar una búsqueda de directorio simple, la interfaz **IDirectorySearch** podría ser más adecuada que las interfaces OLE DB.

En los temas siguientes se describe cómo buscar Active Directory para asegurarse de que la aplicación emite la consulta más eficaz, dados los requisitos del cliente:

-   [Ámbito de la consulta](scope-of-query.md)
-   [Rendimiento y control de grandes conjuntos de resultados](performance-and-handling-large-result-sets.md)
-   [Sintaxis de filtro de búsqueda](search-filter-syntax.md)
-   [Interfaces de consulta](query-interfaces.md)
-   [Buscar datos binarios](searching-binary-data.md)
-   [Consulta distribuida](distributed-query.md)

 

 




