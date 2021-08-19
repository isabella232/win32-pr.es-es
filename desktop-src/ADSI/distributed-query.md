---
title: Consulta distribuida
description: Dado que ADSI es un OLE DB, puede participar en la consulta distribuida introducida en Microsoft SQL Server 7.0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- consulta ADSI, consulta distribuida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46ab174565d8a02ae9058792aa36ef7c3379453e0ba0f861cddf150abf662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428706"
---
# <a name="distributed-query"></a>Consulta distribuida

Dado que ADSI es un OLE DB, puede participar en la consulta distribuida introducida en Microsoft SQL Server 7.0. Estos son los escenarios posibles:

-   Unir Active Directory objetos con SQL Server datos.
-   Actualizar SQL datos de Active Directory objetos.
-   Creación de combinaciones de tres o cuatro vías con otros OLE DB proveedores. Por ejemplo, Index Server, SQL Server y Active Directory.

El proveedor OLE DB admite dos dialectos de comandos, LDAP y SQL, para acceder al servicio de directorio y devolver resultados en un formato tabular que se puede consultar con SQL Server consultas distribuidas.

**Para iniciar el analizador SQL consultas**

1.  En primer lugar, [abra SQL analizador](https://msdn.microsoft.com/library/Aa216983.aspx) de consultas en el SQL Server que está vinculado al servicio de directorio (consulte Creación de un servidor vinculado).
2.  Ejecutar el **analizador SQL consultas (Iniciar** \| programas Microsoft SQL Server \| 7.0)
3.  Inicie sesión en el SQL Server equipo.
4.  Escriba la SQL consulta en el panel Editor de la ventana de consulta.
5.  Presione F5 para ejecutar la consulta.

Las secciones siguientes proporcionan más detalles:

-   [Creación de un servidor vinculado](#creating-a-linked-server)
-   [Crear un inicio de SQL Server autenticado](#creating-a-sql-server-authenticated-login)
-   [Consultar el servicio de directorio](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a>Creación de un servidor vinculado

Para configurar una combinación distribuida en un servicio de Windows 2000 Server, cree un servidor vinculado. Para ello, configure la asignación adsi mediante el procedimiento almacenado del sistema [sp \_ addlinkedserver.](https://msdn.microsoft.com/library/Aa259589.aspx) Este procedimiento vincula un nombre a un nombre OLE DB proveedor.

En el ejemplo siguiente, tenga en cuenta que hay varios argumentos usados con el procedimiento almacenado del sistema [sp \_ addlinkedserver:](https://msdn.microsoft.com/library/Aa259589.aspx)

-   "ADSI" es el **argumento del** servidor y será el nombre de este servidor vinculado.
-   "Active Directory Services 2.5" es el argumento **srvproduct,** que es el nombre del origen de datos OLE DB que se va a agregar como servidor vinculado.
-   "ADSDSOObject" es el argumento **de \_ nombre del** proveedor.
-   "adsdatasource" es el argumento **del \_** origen de datos, que es el nombre del origen de datos interpretado por el proveedor OLE DB datos.

El [comando EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) se usa para ejecutar procedimientos almacenados del sistema.


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



Para Windows autenticados, la autoa asignación es suficiente para acceder al directorio con SQL Server delegación de seguridad. Dado que la autoa asignación se crea de forma predeterminada para los servidores vinculados creados a través de [sp \_ addlinkedserver,](https://msdn.microsoft.com/library/Aa259589.aspx)no es necesaria ninguna otra asignación de inicio de sesión.

Para SQL Server inicios de sesión autenticados, puede configurar inicios de sesión y contraseñas adecuados para conectarse al servicio de directorio mediante el procedimiento almacenado del sistema [sp \_ addlinkedsrvlogin.](https://msdn.microsoft.com/library/Aa259581.aspx)

> [!Note]  
> Siempre que sea posible, utilice la autenticación de Windows.

 

## <a name="creating-a-sql-server-authenticated-login"></a>Crear un inicio de SQL Server autenticado

Si prefiere usar un inicio de sesión SQL Server autenticado en lugar de Windows Authentication, agregue un inicio de sesión al servidor vinculado (consulte la sección anterior). Para ello, use el procedimiento almacenado del sistema [ \_ sp addlinkedsrvlogin.](https://msdn.microsoft.com/library/Aa259581.aspx)

En el ejemplo siguiente, hay varios argumentos que se usan con el procedimiento almacenado del sistema [sp \_ addlinkedsrvlogin:](https://msdn.microsoft.com/library/Aa259581.aspx)

-   "ADSI" es el **argumento rmtsvrname,** que es el nombre del servidor vinculado creado en el ejemplo anterior.
-   "Administrador de Fabrikam" es el argumento \\ **locallogin,** que es el inicio de sesión en el servidor local y puede ser el inicio de sesión SQL Server o un Windows NT.
-   "CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" es el **argumento rmtuser,** que es el nombre de usuario que se usa para conectarse porque **useself** es **false.**
-   "secret \* \* 2000" es **rmtpassword**, que es la contraseña asociada a **rmtuser**

El [comando EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) se usa para ejecutar procedimientos almacenados del sistema.


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a>Consultar el servicio de directorio

Después de crear un servidor vinculado, use una [instrucción OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) para enviar una consulta al servicio de directorio. La siguiente SQL consulta crea una tabla virtual para contener los resultados de la consulta mediante la [instrucción CREATE VIEW.](https://msdn.microsoft.com/library/Aa258253.aspx) La vista que se crea se denomina "viewADContacts".

La primera [instrucción SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) define la información que se consulta desde el servicio de directorio y la asigna a una columna de la tabla. La información entre corchetes indica los datos que se ponen en la tabla virtual. La información que no está entre corchetes indica los datos que se recuperan del servicio de directorio. Observe que su nombre para mostrar LDAP debe hacer referencia a la información que se está recuperando del servicio de directorio.

La siguiente instrucción es la [instrucción OPENQUERY.](https://msdn.microsoft.com/library/Aa276848.aspx) Esta instrucción tiene dos argumentos: ADSI, que es el nombre del servidor vinculado que creó, y una instrucción de consulta. La instrucción query contiene los siguientes elementos:

-   La [instrucción SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) contiene la lista de datos que se obtendrán del servicio de directorio. Deberá usar el nombre para mostrar ldap para indicar qué datos está buscando.
-   La [instrucción FROM](https://msdn.microsoft.com/library/Aa258869.aspx) contiene el nombre del servidor de directorio vinculado del que se obtendrá esta información.
-   La [instrucción WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) proporciona las condiciones de búsqueda. En este ejemplo, busca contactos.

La instrucción [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) final se usa para recoger los resultados de la vista que se va a mostrar.


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 




