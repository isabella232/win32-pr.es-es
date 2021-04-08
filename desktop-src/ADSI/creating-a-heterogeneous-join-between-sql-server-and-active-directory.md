---
title: Crear una combinación heterogénea entre SQL Server & Active Directory
description: Todos los empleados de Fabrikam Corporation se revisan cada seis meses.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e4e6b7f3bfd9c853d9ff262365d49c1f3a8d5c
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103994969"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>Crear una combinación heterogénea entre SQL Server & Active Directory

Todos los empleados de Fabrikam Corporation se revisan cada seis meses. Las clasificaciones de revisión se almacenan en la base de datos de recursos humanos en SQL Server. Para crear una vista de estos datos, Joe Worden, el administrador de la empresa, debe crear primero una tabla de revisión de rendimiento de empleado.

En el analizador de consultas de SQL, Joe va a crear una tabla llamada EMP \_ Review que contendrá tres columnas para contener el nombre del empleado, la fecha de la revisión y la clasificación recibida por el empleado.


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



A continuación, Joe puede insertar algunos registros.


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



Ahora, Joe puede unir el Active Directory objetos de usuario a la tabla SQL Server.

En este ejemplo, la instrucción [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene la lista de datos que se obtendrán del servicio de directorio y SQL Server. La instrucción [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene el nombre del servidor de directorio vinculado del que se obtendrá esta información, en este caso, viewADUsers. La instrucción [Where](https://msdn.microsoft.com/library/Aa260674.aspx) proporciona las condiciones de búsqueda. En este ejemplo, busca por el nombre en el servicio de directorio, que se establece en el nombre de usuario de SQL especificado en la tarea anterior.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



El comando anterior obtiene el resultado de SQL Server y Active Directory. AdsPath y title son de Active Directory, mientras que el nombre de usuario, ReviewDate y clasificación proceden de la tabla SQL. Incluso puede crear otra vista para esta combinación.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




