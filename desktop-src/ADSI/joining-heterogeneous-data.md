---
title: Unión de datos heterogéneos
description: Las organizaciones típicas almacenan datos en varias bases de datos heterogéneos. Los datos de recursos humanos se pueden almacenar en SQL Server, mientras que los datos de administración de cuentas se almacenan en el directorio . Otros datos se pueden almacenar en formatos propietarios.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409ac4e82d735f5099bb8846a59683075007c3fbdf56600bc5ae01e6863ffa2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657005"
---
# <a name="joining-heterogeneous-data"></a>Unión de datos heterogéneos

Las organizaciones típicas almacenan datos en varias bases de datos heterogéneos. Los datos de recursos humanos se pueden almacenar en SQL Server, mientras que los datos de administración de cuentas se almacenan en el directorio . Otros datos se pueden almacenar en formatos propietarios.

Con SQL Server 7.0, ADSI y el proveedor de OLE DB, es posible unir datos de Active Directory a los datos de SQL Server y crear una vista de los datos unidos.

**Para unir Active Directory Data con SQL Server Data**

1.  Ejecutar el **analizador SQL consultas (Iniciar** \| programas Microsoft SQL Server \| 7.0)
2.  Inicie sesión en el SQL Server equipo.
3.  Ejecute la línea siguiente (resalte y presione CTRL+E):

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    En esta línea, los argumentos del procedimiento almacenado del sistema [sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) son los siguientes:

    -   "ADSI" es el **argumento del** servidor, que será el nombre de este servidor vinculado.
    -   "Active Directory Services" es el argumento **srvproduct,** que es el nombre del origen de datos OLE DB que se va a agregar como servidor vinculado.
    -   "ADSDSOObject" es el argumento de nombre **\_ del** proveedor e indica que usa el OLE DB proveedor.
    -   "adsdatasource" es el argumento de origen de datos , que es el nombre del origen de datos interpretado por el proveedor OLE DB datos. **\_**

    Ahora puede usar el servidor vinculado para acceder a Active Directory desde SQL Server.

4.  En el ejemplo siguiente se realiza una consulta mediante la [instrucción OPENQUERY.](https://msdn.microsoft.com/library/Aa276848.aspx) Esta instrucción tiene dos argumentos: ADSI, que es el nombre del servidor vinculado que acaba de crear, y una instrucción de consulta. La instrucción query contiene los siguientes elementos:

    -   La [instrucción SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) contiene la lista de datos que se obtendrán del servicio de directorio. Tendrá que usar el nombre para mostrar LDAP para indicar qué datos está buscando.
    -   La [instrucción FROM](https://msdn.microsoft.com/library/Aa258869.aspx) contiene el nombre del servidor de directorio vinculado del que se obtendrá esta información.
    -   La [instrucción WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) proporciona las condiciones de búsqueda. En este ejemplo, busca usuarios.

    Escriba y ejecute:

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    También puede usar el [dialecto LDAP](ldap-dialect.md)ADSI . Por ejemplo:

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    En el ejemplo anterior, la consulta LDAP tiene cuatro partes:

    -   " \<LDAP://DC=Fabrikam,DC=COM> " es el nombre distintivo del servidor de directorios que se va a buscar.
    -   "(&(objectCategory=Person)(objectClass=user))" es el filtro de búsqueda LDAP (vea Sintaxis [de filtro de búsqueda](search-filter-syntax.md)).
    -   "name, adspath" son los nombres (con el formato de nombre para mostrar LDAP) de los atributos que se van a recuperar.
    -   "subárbol" indica el [ámbito](scope-of-query.md) de la búsqueda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear y ejecutar una vista](creating-and-executing-a-view.md)
</dt> </dl>

 

 




