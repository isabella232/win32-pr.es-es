---
title: Buscar con OLE DB
description: En el caso de los clientes de automatización que utilizan Objetos de datos ActiveX (ADO) y todos los clientes que no son de automatización, ADSI proporciona un proveedor de OLE DB que admite un subconjunto de OLE DB interfaces de consulta.
ms.assetid: f4e48b60-82dd-4c39-879b-0bc8f40747d2
ms.tgt_platform: multiple
keywords:
- Buscar con OLE DB ADSI
- consultas ADSI, buscar con OLE DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b6b0c056a63174233271b9b059ebffa9d4d841
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793893"
---
# <a name="searching-with-ole-db"></a>Buscar con OLE DB

En el caso de los clientes de automatización que utilizan Objetos de datos ActiveX (ADO) y todos los clientes que no son de automatización, ADSI proporciona un proveedor de OLE DB que admite un subconjunto de OLE DB interfaces de consulta. El código de cliente que ya usa OLE DB interfaces para las consultas puede usar las mismas interfaces para consultar los servicios de directorio.

En la implementación de OLE DB, un servicio de directorio se expone como un objeto de origen de datos. Los objetos de origen de datos son generadores de objetos de sesión y admiten [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) para conectarse al directorio, [IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) para crear el objeto de sesión, [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) para proporcionar datos de autenticación al espacio de nombres subyacente y proporcionar el comando de consulta y [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) para guardar los datos necesarios para crear el objeto de origen de datos en el servicio de directorio subyacente.

**Para realizar una consulta Active Directory mediante OLE DB**

1.  Recupere la interfaz [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) del proveedor de OLE DB. En el caso de Active Directory, utilice el identificador de clase **CLSID \_ ADsDSOObject**.
2.  Cree una matriz de [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) de datos de conexión que especifique el nombre de usuario y la contraseña.
3.  Consulte la interfaz [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) recuperada en el paso 1 para la interfaz [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) .
4.  Llame al método [IDBProperties:: SetProperties](/previous-versions/windows/desktop/ms723049(v=vs.85)) pasando la matriz [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) creada en el paso 2.
5.  Llame al método [IDBInitialize:: Initialize](/previous-versions/windows/desktop/ms718026(v=vs.85)) para establecer la conexión con el proveedor de OLE DB; es decir, el proveedor de Active Directory, en este caso.
6.  Consulte la interfaz [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) para la interfaz [IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) .
7.  Llame al método [IDBCreateSession:: createSession](/previous-versions/windows/desktop/ms714942(v=vs.85)) solicitando una nueva interfaz de tipo [IDBCreateCommand](/previous-versions/windows/desktop/ms711625(v=vs.85)).
8.  Llame al método [IDBCreateCommand:: CreateCommand](/previous-versions/windows/desktop/ms709772(v=vs.85)) para crear una interfaz [ICommandText](/previous-versions/windows/desktop/ms714914(v=vs.85)) .
9.  Llame al método [ICommandText:: SetCommandText](/previous-versions/windows/desktop/ms709757(v=vs.85)) . Pase el dialecto preferido y el texto del comando de consulta real en dicho dialecto. **DBGUID \_ LDAPDialect** o **DBGUID \_ DBSQL** se pueden usar como dialecto.
10. Llamar a [ICommand:: Execute](/previous-versions/windows/desktop/ms718095(v=vs.85)); se devuelve una interfaz [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) que es la interfaz para el conjunto de resultados.
11. Consulte la interfaz [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) para la interfaz [IColumnsInfo](/previous-versions/windows/desktop/ms725401(v=vs.85)) .
12. Llame al método [IColumnsInfo:: GetColumnInfo](/previous-versions/windows/desktop/ms722704(v=vs.85)) para recuperar los datos de columna del conjunto de resultados.
13. Rellene una matriz de estructuras [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) , que describe al proveedor de OLE DB cómo exponer los tipos de datos cada columna al código de la aplicación. Este paso le permite especificar qué tipo se incluye en una columna determinada. Además, los desplazamientos de las columnas, con respecto a la fila devuelta, se establecen aquí columna por columna.
14. Consulte la interfaz [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) para la interfaz [IAccessor](/previous-versions/windows/desktop/ms719672(v=vs.85)) .
15. Llame al método [IAccessor:: CreateAccessor](/previous-versions/windows/desktop/ms720969(v=vs.85)) , que devuelve una matriz de identificadores de descriptor de acceso. Esta matriz se utiliza a continuación para tener acceso a las filas del conjunto de resultados.
16. Llame a [IRowset:: GetNextRows](/previous-versions/windows/desktop/ms709827(v=vs.85)) pasando los identificadores de fila y el número de filas que se van a obtener.
17. Llame a [IRowset:: GetData](/previous-versions/windows/desktop/ms716988(v=vs.85)) pasando un identificador de fila, del conjunto devuelto en el paso 16. Se devuelve un puntero sin formato a la fila.

Para obtener más información sobre la sintaxis del filtro de búsqueda, consulte [Sintaxis de filtro de búsqueda](search-filter-syntax.md).

Para leer los datos de fila no procesados devueltos, use la estructura [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) , creada en el paso 13, calcule los desplazamientos de columna en el puntero de datos sin procesar devueltos en el paso 17. Lea la parte de estado de la columna para obtener un resultado de recuperación en esa columna.

Para obtener más información y un ejemplo de código que muestra cómo buscar Active Directory mediante el proveedor de OLE DB ADSI, vea el [código de ejemplo para usar OLE DB para buscar Active Directory](example-code-for-using-ole-db-to-search-active-directory.md).

 

 