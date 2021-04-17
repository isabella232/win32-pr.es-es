---
description: 'A continuación se muestra la sintaxis básica de la instrucción SELECT para una consulta local:'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Instrucción SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05832dab0184870a626fa4bce502d908c9b05f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705475"
---
# <a name="select-statement"></a><span data-ttu-id="31cee-103">Instrucción SELECT</span><span class="sxs-lookup"><span data-stu-id="31cee-103">SELECT Statement</span></span>

<span data-ttu-id="31cee-104">A continuación se muestra la sintaxis básica de la instrucción SELECT para una consulta local:</span><span class="sxs-lookup"><span data-stu-id="31cee-104">The following shows the basic syntax of the SELECT statement for a local query:</span></span>


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



<span data-ttu-id="31cee-105">A continuación se muestra la parte de la columna de la sintaxis de la instrucción SELECT:</span><span class="sxs-lookup"><span data-stu-id="31cee-105">The following shows the column portion of the SELECT statement syntax:</span></span>


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



<span data-ttu-id="31cee-106">Los especificadores de columna deben ser columnas de nombre de propiedad válidos, separados por comas.</span><span class="sxs-lookup"><span data-stu-id="31cee-106">The column specifier(s) must be valid property name columns, separated by commas.</span></span> <span data-ttu-id="31cee-107">Los nombres de columna válidos son descripciones de propiedades registradas o se definen mediante el esquema del sistema de propiedades del shell.</span><span class="sxs-lookup"><span data-stu-id="31cee-107">Valid column names are registered property descriptions or are defined by the Shell's Property System Schema.</span></span> <span data-ttu-id="31cee-108">Puede seleccionar solo las columnas que están marcadas como recuperables en el esquema del sistema de propiedades.</span><span class="sxs-lookup"><span data-stu-id="31cee-108">You can select only those columns that are marked as retrievable in the Property System Schema.</span></span> <span data-ttu-id="31cee-109">Si usa una combinación de mayúsculas y minúsculas mixta para identificar propiedades que no son propiedades definidas por el sistema, debe incluir el especificador de columna entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="31cee-109">If you use mixed case to identify properties that are not system-defined properties, you must enclose the column specifier in double quotation marks.</span></span> <span data-ttu-id="31cee-110">Los nombres de propiedad definidos por el sistema incluyen todas las propiedades que comienzan por "System" (por ejemplo, System. contact. FirstName) y no requieren comillas.</span><span class="sxs-lookup"><span data-stu-id="31cee-110">System-defined property names include all properties beginning with "System" (for example, System.Contact.FirstName) and do not require quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="31cee-111">También puede escribir los nombres de propiedad definidos por el sistema entre comillas dobles para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="31cee-111">You can also enclose system-defined property names in double quotation marks for readability.</span></span> <span data-ttu-id="31cee-112">Esto no afecta a la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="31cee-112">This does not affect compatibility.</span></span>

 

<span data-ttu-id="31cee-113">Cuando la consulta devuelve un documento que no tiene la columna solicitada, el valor de esa columna para el documento es **null**.</span><span class="sxs-lookup"><span data-stu-id="31cee-113">When the query returns a document that does not have the requested column, the value of that column for the document is **NULL**.</span></span>

<span data-ttu-id="31cee-114">Debe proporcionar al menos un nombre de columna en una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="31cee-114">You must provide at least one column name in a SELECT statement.</span></span> <span data-ttu-id="31cee-115">En la consulta Lenguaje de consulta estructurado (SQL), se le permite usar el asterisco ( \* ) para especificar que se devuelvan todas las columnas de una tabla.</span><span class="sxs-lookup"><span data-stu-id="31cee-115">In the Structured Query Language (SQL) query, you are allowed to use the asterisk (\*) to specify that all columns in a table are to be returned.</span></span> <span data-ttu-id="31cee-116">Sin embargo, ningún conjunto de propiedades definido y fijo se aplica a todos los documentos.</span><span class="sxs-lookup"><span data-stu-id="31cee-116">However, no defined and fixed set of properties applies to all documents.</span></span> <span data-ttu-id="31cee-117">Por esta razón, no se permite el asterisco SQL en el <columns> especificador de la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="31cee-117">For this reason, the SQL asterisk is not permitted in the <columns> specifier of the SELECT statement.</span></span>

## <a name="getting-the-top-n-results"></a><span data-ttu-id="31cee-118">Obtener los n resultados principales</span><span class="sxs-lookup"><span data-stu-id="31cee-118">Getting the Top n Results</span></span>

<span data-ttu-id="31cee-119">Puede especificar un número máximo de resultados que se van a devolver mediante la sintaxis superior:</span><span class="sxs-lookup"><span data-stu-id="31cee-119">You can specify a maximum number of results to return by using the TOP syntax:</span></span>


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a><span data-ttu-id="31cee-120">Convertir tipos de datos de columna</span><span class="sxs-lookup"><span data-stu-id="31cee-120">Casting Column Data Types</span></span>

<span data-ttu-id="31cee-121">En ocasiones, puede que necesite convertir los datos de cadena extraídos de los documentos como otro tipo de datos para que se pueda realizar una comparación adecuada.</span><span class="sxs-lookup"><span data-stu-id="31cee-121">At times, you might need to cast string data extracted from documents as another data type so that an appropriate comparison can be made.</span></span> <span data-ttu-id="31cee-122">Para obtener más información, consulte [conversión del tipo de datos de una columna](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="31cee-122">For more information, refer to [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="31cee-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="31cee-123">Examples</span></span>

<span data-ttu-id="31cee-124">Los ejemplos siguientes devuelven el nombre y la dirección URL de los documentos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="31cee-124">The following examples return the name and URL of matching documents.</span></span>


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a><span data-ttu-id="31cee-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31cee-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="31cee-126">**Vista**</span><span class="sxs-lookup"><span data-stu-id="31cee-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="31cee-127">Conversión del tipo de datos de una columna</span><span class="sxs-lookup"><span data-stu-id="31cee-127">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)
</dt> <dt>

<span data-ttu-id="31cee-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="31cee-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="31cee-129">[Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="31cee-129">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 



