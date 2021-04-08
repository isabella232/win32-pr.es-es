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
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a><span data-ttu-id="35b30-103">Crear una combinación heterogénea entre SQL Server & Active Directory</span><span class="sxs-lookup"><span data-stu-id="35b30-103">Creating a Heterogeneous Join between SQL Server & Active Directory</span></span>

<span data-ttu-id="35b30-104">Todos los empleados de Fabrikam Corporation se revisan cada seis meses.</span><span class="sxs-lookup"><span data-stu-id="35b30-104">All employees at the Fabrikam corporation are reviewed every six months.</span></span> <span data-ttu-id="35b30-105">Las clasificaciones de revisión se almacenan en la base de datos de recursos humanos en SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35b30-105">Review ratings are stored in the Human Resource database in SQL Server.</span></span> <span data-ttu-id="35b30-106">Para crear una vista de estos datos, Joe Worden, el administrador de la empresa, debe crear primero una tabla de revisión de rendimiento de empleado.</span><span class="sxs-lookup"><span data-stu-id="35b30-106">To create a view of this data, Joe Worden, the enterprise administrator, must first create an employee performance review table.</span></span>

<span data-ttu-id="35b30-107">En el analizador de consultas de SQL, Joe va a crear una tabla llamada EMP \_ Review que contendrá tres columnas para contener el nombre del empleado, la fecha de la revisión y la clasificación recibida por el empleado.</span><span class="sxs-lookup"><span data-stu-id="35b30-107">In the SQL Query Analyzer, Joe is going to create a table called EMP\_REVIEW that will contain three columns to hold the name of the employee, the date of the review, and the rating that the employee received.</span></span>


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



<span data-ttu-id="35b30-108">A continuación, Joe puede insertar algunos registros.</span><span class="sxs-lookup"><span data-stu-id="35b30-108">Joe can then insert a few records.</span></span>


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



<span data-ttu-id="35b30-109">Ahora, Joe puede unir el Active Directory objetos de usuario a la tabla SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35b30-109">Now Joe can join the Active Directory user objects to the SQL Server table.</span></span>

<span data-ttu-id="35b30-110">En este ejemplo, la instrucción [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene la lista de datos que se obtendrán del servicio de directorio y SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35b30-110">In this example, the [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service and SQL Server.</span></span> <span data-ttu-id="35b30-111">La instrucción [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene el nombre del servidor de directorio vinculado del que se obtendrá esta información, en este caso, viewADUsers.</span><span class="sxs-lookup"><span data-stu-id="35b30-111">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from, in this case, viewADUsers.</span></span> <span data-ttu-id="35b30-112">La instrucción [Where](https://msdn.microsoft.com/library/Aa260674.aspx) proporciona las condiciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="35b30-112">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="35b30-113">En este ejemplo, busca por el nombre en el servicio de directorio, que se establece en el nombre de usuario de SQL especificado en la tarea anterior.</span><span class="sxs-lookup"><span data-stu-id="35b30-113">In this example, it is searching by the name in the directory service, which is set to the SQL userName entered in the previous task.</span></span>


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



<span data-ttu-id="35b30-114">El comando anterior obtiene el resultado de SQL Server y Active Directory.</span><span class="sxs-lookup"><span data-stu-id="35b30-114">The previous command gets the result from both SQL Server and Active Directory.</span></span> <span data-ttu-id="35b30-115">AdsPath y title son de Active Directory, mientras que el nombre de usuario, ReviewDate y clasificación proceden de la tabla SQL.</span><span class="sxs-lookup"><span data-stu-id="35b30-115">AdsPath and title are from Active Directory, whereas userName, ReviewDate, and Rating are from the SQL table.</span></span> <span data-ttu-id="35b30-116">Incluso puede crear otra vista para esta combinación.</span><span class="sxs-lookup"><span data-stu-id="35b30-116">He can even create another view for this join.</span></span>


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




