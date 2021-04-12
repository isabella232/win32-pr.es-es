---
title: Elección de la tecnología de búsqueda
description: En este tema se incluye una lista de tecnologías que se usan para buscar Active Directory.
ms.assetid: c9e887e3-7de4-4461-bc32-03db71c3e272
ms.tgt_platform: multiple
keywords:
- tecnologías de búsqueda en Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6edba5c87ed438bc0047e0381d7e366cd6cc865
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487495"
---
# <a name="choosing-the-search-technology"></a>Elección de la tecnología de búsqueda

Las tecnologías, que se enumeran en la tabla siguiente, se pueden usar para realizar búsquedas en Active Directory Domain Services.



| Technology                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1)<br/> | El espacio de nombres [System. DirectoryServices](/dotnet/api/system.directoryservices?view=dotnet-plat-ext-3.1) proporciona la clase [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1) para permitir la búsqueda dentro de Active Directory Domain Services con .NET Framework. Para obtener más información, vea [Buscar en el directorio](/previous-versions/ms180879(v=vs.90)).<br/>                                                                                                                                  |
| [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)<br/>                       | ADSI proporciona la interfaz [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para consultar un servidor de Active Directory, así como otros servicios de directorio como NDS, con LDAP. **IDirectorySearch** es una interfaz com que devuelve datos con tipo enriquecido, como un entero, una cadena de octetos, una cadena, un descriptor de seguridad, una hora UTC, un entero grande o un valor booleano. Para obtener más información sobre cómo usar **IDirectorySearch**, consulte [búsqueda con la interfaz IDirectorySearch](/windows/desktop/ADSI/searching-with-idirectorysearch).<br/> |
| OLE DB<br/>                                                              | OLE DB es un conjunto de interfaces COM que proporcionan a las aplicaciones acceso uniforme a los datos almacenados en diversos orígenes de datos, independientemente de la ubicación o el tipo. ADSI también proporciona un proveedor de OLE DB para ADSI que permite a las aplicaciones usar OLE DB para tener acceso a Active Directory Domain Services. El proveedor de OLE DB ADSI utiliza las interfaces [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para enviar consultas a Active Directory Domain Services y para recopilar los resultados.<br/>                                     |
| ADO y otras tecnologías de acceso a datos basadas en OLE DB<br/>                 | El proveedor de OLE DB ADSI habilita cualquier tecnología de acceso a datos basada en OLE DB, como ADO, para buscar en Active Directory Domain Services.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| API LDAP<br/>                                                            | Los controladores de dominio de Windows 2000 son servidores de directorio que son compatibles con la versión 3 de LDAP. La API de LDAP es una biblioteca de funciones de estilo C. Las aplicaciones pueden usar la API LDAP para buscar en Active Directory Domain Services.<br/>                                                                                                                                                                                                                                                                              |



 

Tenga en cuenta lo siguiente a la hora de elegir una tecnología:

-   Para Microsoft Visual Basic y Visual Basic Scripting Edition (VBScript), se recomienda ADO.
-   En C/C++, puede elegir cualquiera de las tecnologías.
-   Si la aplicación utiliza extensamente ADSI, puede ser más fácil usar [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch). Si usa [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) para administrar objetos en Active Directory Domain Services, use **IDirectorySearch** para facilitar el control de las propiedades devueltas de la búsqueda. **IDirectorySearch** utiliza las mismas estructuras [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) que **IDirectoryObject** para representar las propiedades. Además, **IDirectorySearch** se expone en casi todos los objetos com de ADSI. Si tiene un puntero a un objeto COM de ADSI, puede llamar a **QueryInterface** para obtener un puntero de **IDirectorySearch** que puede utilizar para realizar una búsqueda a partir del objeto de directorio representado por el objeto com de ADSI.
-   Si su aplicación ya usa OLE DB, ADO o la API LDAP, puede seguir usando esas tecnologías para buscar dentro de Active Directory Domain Services.
-   Si la aplicación debe combinar datos de un servicio de Dominio de Active Directory y una base de datos de SQL Server 7, use OLE DB. Mediante el uso de OLE DB, la aplicación puede realizar consultas distribuidas que hacen referencia a Active Directory Domain Services y tablas y conjuntos de filas de una o varias bases de datos de Microsoft SQL Server 7.

 

