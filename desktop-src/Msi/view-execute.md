---
description: El método Execute del objeto View utiliza el token de signo de interrogación para representar los parámetros en una instrucción SQL. Para obtener más información, vea sintaxis de SQL. Los valores de estos parámetros se pasan como los campos correspondientes de un registro de parámetros.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exe(método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653363"
---
# <a name="viewexecute-method"></a><span data-ttu-id="67c96-105">View.Exe(método)</span><span class="sxs-lookup"><span data-stu-id="67c96-105">View.Execute method</span></span>

<span data-ttu-id="67c96-106">El método **Execute** del objeto [**View**](view-object.md) utiliza el token de signo de interrogación para representar los parámetros en una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="67c96-106">The **Execute** method of the [**View**](view-object.md) object uses the question mark token to represent parameters in an SQL statement.</span></span> <span data-ttu-id="67c96-107">Para obtener más información, vea [Sintaxis de SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="67c96-107">For more information, see [SQL Syntax](sql-syntax.md).</span></span> <span data-ttu-id="67c96-108">Los valores de estos parámetros se pasan como los campos correspondientes de un registro de parámetros.</span><span class="sxs-lookup"><span data-stu-id="67c96-108">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c96-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67c96-109">Syntax</span></span>


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="67c96-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67c96-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c96-111">*record*</span><span class="sxs-lookup"><span data-stu-id="67c96-111">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="67c96-112">Objetos de [**registro**](record-object.md) opcionales que contienen los valores que reemplazan los tokens de parámetro (?) en la consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="67c96-112">Optional [**Record**](record-object.md) objects that contains the values that replace the parameter tokens (?) in the SQL query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67c96-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67c96-113">Return value</span></span>

<span data-ttu-id="67c96-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="67c96-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67c96-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67c96-115">Remarks</span></span>

<span data-ttu-id="67c96-116">Se debe llamar a este método antes de cualquier llamada al método [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="67c96-116">This method must be called before any calls to the [**Fetch**](view-fetch.md) method.</span></span>

<span data-ttu-id="67c96-117">Si la consulta SQL especifica valores con marcadores de parámetros (?), se debe proporcionar un registro que contenga todos los valores de reemplazo, que deben estar en el mismo orden y del mismo tipo de datos que los marcadores de parámetros.</span><span class="sxs-lookup"><span data-stu-id="67c96-117">If the SQL query specifies values with parameter markers (?), a record must be supplied that contains all of the replacement values, which must be in the same order and of the same data type as the parameter markers.</span></span> <span data-ttu-id="67c96-118">Cuando este método se usa con consultas INSERT y UPDATE, los tokens de signo de interrogación deben preceder a todos los valores sin parámetros.</span><span class="sxs-lookup"><span data-stu-id="67c96-118">When this method is used with INSERT and UPDATE queries, the question mark tokens must precede all the non-parameterized values.</span></span>

<span data-ttu-id="67c96-119">Por ejemplo, estas consultas son válidas:</span><span class="sxs-lookup"><span data-stu-id="67c96-119">For example, these queries are valid:</span></span>

<span data-ttu-id="67c96-120">Actualice {Table-List} SET {Column} =?</span><span class="sxs-lookup"><span data-stu-id="67c96-120">UPDATE {table-list} SET {column}= ?</span></span> <span data-ttu-id="67c96-121">, {Column} = {Constant}</span><span class="sxs-lookup"><span data-stu-id="67c96-121">, {column}= {constant}</span></span>

<span data-ttu-id="67c96-122">Inserte INTO {Table} ({Column-List}) VALUEs (?, {Constant-List})</span><span class="sxs-lookup"><span data-stu-id="67c96-122">INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})</span></span>

<span data-ttu-id="67c96-123">Sin embargo, estas consultas no son válidas:</span><span class="sxs-lookup"><span data-stu-id="67c96-123">However these queries are invalid:</span></span>

<span data-ttu-id="67c96-124">Actualice {Table-List} SET {Column} = {Constant}, {Column} =?</span><span class="sxs-lookup"><span data-stu-id="67c96-124">UPDATE {table-list} SET {column}= {constant}, {column}=?</span></span>

<span data-ttu-id="67c96-125">Inserte INTO {Table} ({Column-List}) VALUEs ({Constant-List},?</span><span class="sxs-lookup"><span data-stu-id="67c96-125">INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ?</span></span> <span data-ttu-id="67c96-126">)</span><span class="sxs-lookup"><span data-stu-id="67c96-126">)</span></span>

<span data-ttu-id="67c96-127">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="67c96-127">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="67c96-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67c96-128">Requirements</span></span>



| <span data-ttu-id="67c96-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="67c96-129">Requirement</span></span> | <span data-ttu-id="67c96-130">Value</span><span class="sxs-lookup"><span data-stu-id="67c96-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c96-131">Versión</span><span class="sxs-lookup"><span data-stu-id="67c96-131">Version</span></span><br/> | <span data-ttu-id="67c96-132">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="67c96-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="67c96-133">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67c96-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="67c96-134">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="67c96-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="67c96-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67c96-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="67c96-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67c96-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="67c96-137">IID</span><span class="sxs-lookup"><span data-stu-id="67c96-137">IID</span></span><br/>     | <span data-ttu-id="67c96-138">IID \_ iView se define como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="67c96-138">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




