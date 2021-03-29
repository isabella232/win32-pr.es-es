---
description: El método OpenView del objeto de base de datos devuelve un objeto de vista que representa la consulta especificada por una cadena SQL.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Método Database. OpenView (Certview. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653983"
---
# <a name="databaseopenview-method"></a><span data-ttu-id="4ae0b-103">Database. OpenView (método)</span><span class="sxs-lookup"><span data-stu-id="4ae0b-103">Database.OpenView method</span></span>

<span data-ttu-id="4ae0b-104">El método **OpenView** del objeto de [**base de datos**](database-object.md) devuelve un objeto de [**vista**](view-object.md) que representa la consulta especificada por una cadena SQL.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-104">The **OpenView** method of the [**Database**](database-object.md) object returns a [**View**](view-object.md) object that represents the query specified by a SQL string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae0b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ae0b-105">Syntax</span></span>


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a><span data-ttu-id="4ae0b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ae0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ae0b-107">*sql*</span><span class="sxs-lookup"><span data-stu-id="4ae0b-107">*sql*</span></span> 
</dt> <dd>

<span data-ttu-id="4ae0b-108">Cadena de consulta SQL necesaria.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-108">Required SQL query string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ae0b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ae0b-109">Return value</span></span>

<span data-ttu-id="4ae0b-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ae0b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ae0b-111">Remarks</span></span>

<span data-ttu-id="4ae0b-112">Para obtener información sobre la sintaxis de SQL implementada en el instalador, vea [Sintaxis de SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="4ae0b-112">For information about SQL syntax implemented in the installer, see [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="4ae0b-113">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="4ae0b-113">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae0b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ae0b-114">Requirements</span></span>



| <span data-ttu-id="4ae0b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ae0b-115">Requirement</span></span> | <span data-ttu-id="4ae0b-116">Value</span><span class="sxs-lookup"><span data-stu-id="4ae0b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae0b-117">Versión</span><span class="sxs-lookup"><span data-stu-id="4ae0b-117">Version</span></span><br/> | <span data-ttu-id="4ae0b-118">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4ae0b-119">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4ae0b-120">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ae0b-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4ae0b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ae0b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4ae0b-122"><dt>Certview. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae0b-122"><dt>Certview.h</dt></span></span> </dl>                                                                                                                                                                   |
| <span data-ttu-id="4ae0b-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ae0b-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="4ae0b-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ae0b-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4ae0b-125">IID</span><span class="sxs-lookup"><span data-stu-id="4ae0b-125">IID</span></span><br/>     | <span data-ttu-id="4ae0b-126">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4ae0b-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="4ae0b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ae0b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae0b-128">**Base de datos**</span><span class="sxs-lookup"><span data-stu-id="4ae0b-128">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="4ae0b-129">Sintaxis de SQL</span><span class="sxs-lookup"><span data-stu-id="4ae0b-129">SQL Syntax</span></span>](sql-syntax.md)
</dt> </dl>

 

 




