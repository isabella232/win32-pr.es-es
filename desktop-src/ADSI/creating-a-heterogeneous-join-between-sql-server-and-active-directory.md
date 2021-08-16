---
title: Crear una combinación heterogéneo entre SQL Server & Active Directory
description: Todos los empleados de fabrikam corporation se revisan cada seis meses.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8620706db56124b83c8cd8151c067a548d5a73d557fa6523ed82167647450b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840295"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>Crear una combinación heterogéneo entre SQL Server & Active Directory

Todos los empleados de fabrikam corporation se revisan cada seis meses. Las clasificaciones de revisión se almacenan en la base de datos de recursos humanos SQL Server. Para crear una vista de estos datos, Joe Worden, el administrador de la empresa, primero debe crear una tabla de revisión del rendimiento de los empleados.

En el Analizador de consultas de SQL, Joe va a crear una tabla denominada EMP REVIEW que contendrá tres columnas que contendrán el nombre del empleado, la fecha de la revisión y la clasificación que recibió \_ el empleado.


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



Ahora Joe puede unir los objetos Active Directory usuario a la SQL Server tabla.

En este ejemplo, la [instrucción SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) contiene la lista de datos que se obtendrán del servicio de directorio y SQL Server. La [instrucción FROM](https://msdn.microsoft.com/library/Aa258869.aspx) contiene el nombre del servidor de directorio vinculado del que se obtendrá esta información, en este caso, viewADUsers. La [instrucción WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) proporciona las condiciones de búsqueda. En este ejemplo, busca por el nombre en el servicio de directorio, que se establece en el valor SQL userName especificado en la tarea anterior.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



El comando anterior obtiene el resultado de SQL Server y Active Directory. AdsPath y title son de Active Directory, mientras que userName, ReviewDate y Rating son de SQL tabla. Incluso puede crear otra vista para esta combinación.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




