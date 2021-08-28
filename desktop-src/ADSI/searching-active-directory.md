---
title: Buscar Active Directory
description: Una función importante de Active Directory es resolver consultas de datos para personas, así como datos de configuración para equipos y servicios.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Búsqueda Active Directory ADSI
- ADSI ADSI , buscar Active Directory
- consulta ADSI y busca Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d3ec83268556ebcacd89efeca425db87e2c0cc06e69a1e6eea810bcd6a21de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005475"
---
# <a name="searching-active-directory"></a>Buscar Active Directory

Una función importante de Active Directory es resolver consultas de datos para personas, así como datos de configuración para equipos y servicios. Para escribir consultas eficaces para Active Directory, resulta útil estar familiarizado con lo siguiente:

-   Determinar el ámbito de la consulta: ¿Debe el cliente buscar propiedades para objetos que podrían encontrarse en cualquier lugar dentro de un bosque, solo dentro de un dominio o dentro de una unidad organizativa (OU)?
-   Determinación de la profundidad de la consulta: ¿la consulta solo debe buscar en un nivel o podría entrar en otros directorios LDAP?
-   Rendimiento y control de grandes conjuntos de resultados: ¿Cómo debe el cliente controlar eficazmente el potencial de un conjunto de resultados grande?
-   Determinar las mejores consultas: ¿Qué tipo de consultas proporcionan los resultados más eficaces? ¿Qué tipo de consultas debe evitar el desarrollador?
-   Descripción de la sintaxis de consulta: ADSI admite tanto la sintaxis LDAP como se documenta en RFC 2254, así como un subconjunto de SQL.
-   Elección de interfaces: ADSI proporciona compatibilidad OLE DB, así como una interfaz de C/C++ denominada [**IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Dado que ADSI funciona para varios espacios de nombres, puede usar estas interfaces para consultar otros espacios de nombres, como Exchange, así como Active Directory. Dado que ActiveX Data Object (ADO) es un modelo de objetos de acceso a datos que permite scripts sobre OLE DB, las interfaces de OLE DB funcionan bien para programadores de Visual Basic y escritores de scripts de páginas web. Las nuevas características de acceso a datos de las aplicaciones Visual Studio y Office que aprovechan ADO y OLE DB ahora pueden acceder Active Directory los datos de la misma manera que acceden a los datos de otros proveedores de OLE DB, como SQL Server. Sin embargo, si un desarrollador de C/C++ debe realizar una búsqueda de directorio simple, la interfaz **IDirectorySearch** podría ser más adecuada que las interfaces OLE DB usuario.

En los temas siguientes se describe cómo buscar Active Directory para asegurarse de que la aplicación emite la consulta más eficaz, dados los requisitos del cliente:

-   [Ámbito de la consulta](scope-of-query.md)
-   [Rendimiento y control de grandes conjuntos de resultados](performance-and-handling-large-result-sets.md)
-   [Sintaxis de filtro de búsqueda](search-filter-syntax.md)
-   [Interfaces de consulta](query-interfaces.md)
-   [Buscar datos binarios](searching-binary-data.md)
-   [Consulta distribuida](distributed-query.md)

 

 




