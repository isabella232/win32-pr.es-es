---
title: Combinar datos heterogéneos
description: Las organizaciones típicas almacenan datos en varias bases de datos heterogéneas. Los datos de recursos humanos se pueden almacenar en SQL Server, mientras que los datos de administración de cuentas se almacenan en el directorio. Otros datos pueden almacenarse en formatos de propiedad.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6d0303ee933b81f0c8553b6b0adae64db7f48d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103904417"
---
# <a name="joining-heterogeneous-data"></a>Combinar datos heterogéneos

Las organizaciones típicas almacenan datos en varias bases de datos heterogéneas. Los datos de recursos humanos se pueden almacenar en SQL Server, mientras que los datos de administración de cuentas se almacenan en el directorio. Otros datos pueden almacenarse en formatos de propiedad.

Con, SQL Server 7,0, ADSI y el proveedor de OLE DB, es posible combinar datos de Active Directory con los datos de SQL Server y crear una vista de los datos combinados.

**Para combinar datos de Active Directory con datos de SQL Server**

1.  Ejecutar el **analizador de consultas de SQL** (iniciar \| programas \| Microsoft SQL Server 7,0)
2.  Inicie sesión en el equipo SQL Server.
3.  Ejecute la línea siguiente (resáltela y presione CTRL + E):

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    En esta línea, los argumentos para el procedimiento almacenado del sistema [Sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) son los siguientes:

    -   "ADSI" es el argumento **Server** , que será el nombre de este servidor vinculado.
    -   "Active Directory Services" es el argumento **srvproduct** , que es el nombre del OLE DB origen de datos que se va a agregar como servidor vinculado.
    -   "ADSDSOObject" es el argumento de **\_ nombre de proveedor** e indica que se está usando el proveedor de OLE DB.
    -   "adsdatasource" es el **\_ argumento de origen de datos**, que es el nombre del origen de datos tal como lo interpreta el proveedor de OLE DB.

    Ahora puede usar el servidor vinculado para obtener acceso a Active Directory desde SQL Server.

4.  En el ejemplo siguiente se realiza una consulta mediante la instrucción [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) . Esta instrucción tiene dos argumentos: ADSI, que es el nombre del servidor vinculado que acaba de crear y una instrucción de consulta. La instrucción de consulta contiene los elementos siguientes:

    -   La instrucción [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene la lista de datos que se obtendrán del servicio de directorio. Tendrá que usar el nombre para mostrar LDAP para indicar qué datos está buscando.
    -   La instrucción [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene el nombre del servidor de directorio vinculado del que se obtendrá esta información.
    -   La instrucción [Where](https://msdn.microsoft.com/library/Aa260674.aspx) proporciona las condiciones de búsqueda. En este ejemplo, está buscando usuarios.

    Escriba y ejecute:

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    También puede usar el [dialecto LDAP](ldap-dialect.md)de ADSI. Por ejemplo:

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    En el ejemplo anterior, la consulta LDAP tiene cuatro partes:

    -   " <LDAP://DC=Fabrikam,DC=COM> " es el nombre distintivo del servidor de directorio en el que se va a buscar.
    -   "(& (objectCategory = person) (objectClass = User))" es el filtro de búsqueda LDAP (consulte [Sintaxis de filtro de búsqueda](search-filter-syntax.md)).
    -   "Name, ADsPath" son los nombres (con el formato de nombre para mostrar LDAP) de los atributos que se van a recuperar.
    -   "subárbol" indica el [ámbito](scope-of-query.md) de la búsqueda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear y ejecutar una vista](creating-and-executing-a-view.md)
</dt> </dl>

 

 




