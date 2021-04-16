---
description: La propiedad PrimaryKeys del objeto de base de datos devuelve un objeto de registro que contiene el nombre de tabla en el campo 0 y los nombres de columna (que comprenden las claves principales) en los campos que corresponden a sus números de columna.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Propiedad Database. PrimaryKeys
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671680"
---
# <a name="databaseprimarykeys-property"></a><span data-ttu-id="4f67a-103">Propiedad Database. PrimaryKeys</span><span class="sxs-lookup"><span data-stu-id="4f67a-103">Database.PrimaryKeys property</span></span>

<span data-ttu-id="4f67a-104">La propiedad **PrimaryKeys** del objeto de [**base de datos**](database-object.md) devuelve un objeto de [**registro**](record-object.md) que contiene el nombre de tabla en el campo 0 y los nombres de columna (que comprenden las claves principales) en los campos que corresponden a sus números de columna.</span><span class="sxs-lookup"><span data-stu-id="4f67a-104">The **PrimaryKeys** property of the [**Database**](database-object.md) object returns a [**Record**](record-object.md) object containing the table name in field 0 and the column names (comprising the primary keys) in succeeding fields corresponding to their column numbers.</span></span> <span data-ttu-id="4f67a-105">El recuento de campos del registro es el recuento de las columnas de clave principal.</span><span class="sxs-lookup"><span data-stu-id="4f67a-105">The field count of the record is the count of primary key columns.</span></span>

<span data-ttu-id="4f67a-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4f67a-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f67a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f67a-107">Syntax</span></span>


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a><span data-ttu-id="4f67a-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4f67a-108">Property value</span></span>

<span data-ttu-id="4f67a-109">Nombre necesario de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="4f67a-109">Required name of an existing table.</span></span> <span data-ttu-id="4f67a-110">Si la tabla no existe, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="4f67a-110">An error is generated if the table does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f67a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f67a-111">Remarks</span></span>

<span data-ttu-id="4f67a-112">La propiedad **PrimaryKeys** no se puede usar con [ \_ la tabla TABLES o la](-tables-table.md) [ \_ tabla Columns](-columns-table.md).</span><span class="sxs-lookup"><span data-stu-id="4f67a-112">The **PrimaryKeys** property cannot be used with the [\_Tables table](-tables-table.md) or the [\_Columns table](-columns-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f67a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f67a-113">Requirements</span></span>



| <span data-ttu-id="4f67a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f67a-114">Requirement</span></span> | <span data-ttu-id="4f67a-115">Value</span><span class="sxs-lookup"><span data-stu-id="4f67a-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f67a-116">Versión</span><span class="sxs-lookup"><span data-stu-id="4f67a-116">Version</span></span><br/> | <span data-ttu-id="4f67a-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4f67a-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4f67a-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4f67a-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4f67a-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="4f67a-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4f67a-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f67a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="4f67a-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f67a-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4f67a-122">IID</span><span class="sxs-lookup"><span data-stu-id="4f67a-122">IID</span></span><br/>     | <span data-ttu-id="4f67a-123">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4f67a-123">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




