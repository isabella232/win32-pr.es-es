---
title: Consulta distribuida
description: Como ADSI es un proveedor de OLE DB, puede participar en la consulta distribuida introducida en Microsoft SQL Server 7,0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- consultas ADSI, consulta distribuida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8675f0a5ba9faa6ece78783eb4f61f17aafabc8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "105656309"
---
# <a name="distributed-query"></a>Consulta distribuida

Como ADSI es un proveedor de OLE DB, puede participar en la consulta distribuida introducida en Microsoft SQL Server 7,0. Los escenarios posibles son los siguientes:

-   Combinar objetos de Active Directory con datos de SQL Server.
-   Actualizar datos SQL desde objetos Active Directory.
-   Crear combinaciones tridireccionales o bidireccionales con otros proveedores de OLE DB. Por ejemplo, Index Server, SQL Server y Active Directory.

El proveedor de OLE DB admite dos dialectos de comandos, LDAP y SQL, para tener acceso al servicio de directorio y devolver los resultados en un formato tabular que se puede consultar con SQL Server consultas distribuidas.

**Para iniciar el analizador de consultas de SQL**

1.  En primer lugar, abra el [analizador de consultas de SQL](https://msdn.microsoft.com/library/Aa216983.aspx) en el SQL Server que está vinculado al servicio de directorio (consulte Creación de un servidor vinculado).
2.  Ejecutar el **analizador de consultas de SQL** (iniciar \| programas \| Microsoft SQL Server 7,0)
3.  Inicie sesión en el equipo SQL Server.
4.  Escriba la consulta SQL en el panel del editor de la ventana de consulta.
5.  Ejecute la consulta presionando F5.

En las secciones siguientes se proporcionan más detalles:

-   [Creación de un servidor vinculado](#creating-a-linked-server)
-   [Creación de un inicio de sesión autenticado de SQL Server](#creating-a-sql-server-authenticated-login)
-   [Consultar el servicio de directorio](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a>Creación de un servidor vinculado

Para configurar una combinación distribuida en un servicio de directorio de Windows 2000 Server, cree un servidor vinculado. Para ello, configure la asignación ADSI mediante el procedimiento almacenado del sistema [ \_ addlinkedserver de SP](https://msdn.microsoft.com/library/Aa259589.aspx) . Este procedimiento vincula un nombre a un nombre de proveedor de OLE DB.

En el ejemplo siguiente, tenga en cuenta que hay varios argumentos que se usan con el procedimiento almacenado del sistema [Sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) :

-   "ADSI" es el argumento **Server** y será el nombre de este servidor vinculado.
-   "Active Directory Services 2,5" es el argumento **srvproduct** , que es el nombre del origen de datos OLE DB que se va a agregar como servidor vinculado.
-   "ADSDSOObject" es el argumento de **\_ nombre del proveedor** .
-   "adsdatasource" es el argumento de **\_ origen de datos** , que es el nombre del origen de datos tal como lo interpreta el proveedor de OLE DB.

El comando [exec](https://msdn.microsoft.com/library/Aa258848.aspx) se usa para ejecutar procedimientos almacenados del sistema.


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



En el caso de los inicios de sesión autenticados por Windows, la asignación automática es suficiente para tener acceso al directorio con SQL Server la delegación de seguridad. Dado que la asignación automática se crea de forma predeterminada para los servidores vinculados creados a través de [Sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), no es necesario ninguna otra asignación de inicio de sesión.

En el caso de los inicios de sesión autenticados de SQL Server, puede configurar inicios de sesión y contraseñas adecuados para conectarse al servicio de directorio mediante el procedimiento almacenado del sistema [ \_ addlinkedsrvlogin de SP](https://msdn.microsoft.com/library/Aa259581.aspx) .

> [!Note]  
> Siempre que sea posible, utilice la autenticación de Windows.

 

## <a name="creating-a-sql-server-authenticated-login"></a>Creación de un inicio de sesión autenticado de SQL Server

Si prefiere usar un inicio de sesión autenticado SQL Server en lugar de la autenticación de Windows, agregue un inicio de sesión al servidor vinculado (vea la sección anterior). Para ello, use el procedimiento almacenado del sistema [Sp \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .

En el ejemplo siguiente, hay varios argumentos que se usan con el procedimiento almacenado del sistema [Sp \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) :

-   "ADSI" es el argumento **rmtsvrname** , que es el nombre del servidor vinculado creado en el ejemplo anterior.
-   " \\ Administrador de Fabrikam" es el argumento **locallogin** , que es el inicio de sesión en el servidor local y puede ser el inicio de sesión de SQL Server o un usuario de Windows NT.
-   "CN = Administrator, OU = sales, DC = activeds, DC = Fabrikam, DC = com" es el argumento **rmtuser** , que es el nombre de usuario que se usa para conectarse porque **useself** es **false**.
-   "Secret \* \* 2000" es el **rmtpassword**, que es la contraseña asociada a **rmtuser**

El comando [exec](https://msdn.microsoft.com/library/Aa258848.aspx) se usa para ejecutar procedimientos almacenados del sistema.


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a>Consultar el servicio de directorio

Después de crear un servidor vinculado, utilice una instrucción [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) para enviar una consulta al servicio de directorio. La siguiente consulta SQL crea una tabla virtual para almacenar los resultados de la consulta mediante la instrucción [Create View](https://msdn.microsoft.com/library/Aa258253.aspx) . La vista que se crea se denomina "viewADContacts".

La primera instrucción [Select](https://msdn.microsoft.com/library/Aa259187.aspx) define la información que se consulta desde el servicio de directorio y la asigna a una columna de la tabla. La información entre corchetes indica los datos que se colocan en la tabla virtual. La información que no está entre corchetes indica los datos que se recuperan del servicio de directorio. Tenga en cuenta que se debe hacer referencia a la información que se recupera del servicio de directorio mediante su nombre para mostrar LDAP.

La siguiente instrucción es la instrucción [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) . Esta instrucción tiene dos argumentos: ADSI, que es el nombre del servidor vinculado que ha creado y una instrucción de consulta. La instrucción de consulta contiene los elementos siguientes:

-   La instrucción [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene la lista de datos que se obtendrán del servicio de directorio. Tendrá que usar el nombre para mostrar LDAP para indicar qué datos está buscando.
-   La instrucción [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene el nombre del servidor de directorio vinculado del que se obtendrá esta información.
-   La instrucción [Where](https://msdn.microsoft.com/library/Aa260674.aspx) proporciona las condiciones de búsqueda. En este ejemplo, busca contactos.

La instrucción [Select](https://msdn.microsoft.com/library/Aa259187.aspx) final se usa para recopilar los resultados de la vista que se va a mostrar.


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



 

 




