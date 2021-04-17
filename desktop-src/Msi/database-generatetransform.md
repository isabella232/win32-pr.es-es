---
description: El método GenerateTransform del objeto Database crea una transformación que, cuando se aplica a la base de datos de objetos, da como resultado la base de datos de referencia. La transformación se almacena en el objeto de almacenamiento.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Database. GenerateTransform (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653529"
---
# <a name="databasegeneratetransform-method"></a><span data-ttu-id="089ff-104">Database. GenerateTransform (método)</span><span class="sxs-lookup"><span data-stu-id="089ff-104">Database.GenerateTransform method</span></span>

<span data-ttu-id="089ff-105">El método **GenerateTransform** del objeto [**Database**](database-object.md) crea una [*transformación*](t-gly.md) que, cuando se aplica a la base de datos de objetos, da como resultado la base de datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="089ff-105">The **GenerateTransform** method of the [**Database**](database-object.md) object creates a [*transform*](t-gly.md) that, when applied to the object database, results in the reference database.</span></span> <span data-ttu-id="089ff-106">La transformación se almacena en el objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="089ff-106">The transform is stored in the storage object.</span></span>

<span data-ttu-id="089ff-107">Si la transformación se va a aplicar durante una instalación, debe usar el método [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) para rellenar la secuencia de información de resumen.</span><span class="sxs-lookup"><span data-stu-id="089ff-107">If the transform is to be applied during an installation you must use the [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) method to populate the summary information stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="089ff-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="089ff-108">Syntax</span></span>


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a><span data-ttu-id="089ff-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="089ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="089ff-110">*reference*</span><span class="sxs-lookup"><span data-stu-id="089ff-110">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="089ff-111">Base de datos necesaria que no incluye los cambios.</span><span class="sxs-lookup"><span data-stu-id="089ff-111">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="089ff-112">*storage*</span><span class="sxs-lookup"><span data-stu-id="089ff-112">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="089ff-113">Nombre del archivo de transformación generado.</span><span class="sxs-lookup"><span data-stu-id="089ff-113">The name of the generated transform file.</span></span> <span data-ttu-id="089ff-114">Esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="089ff-114">This is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="089ff-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="089ff-115">Return value</span></span>

<span data-ttu-id="089ff-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="089ff-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="089ff-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="089ff-117">Remarks</span></span>

<span data-ttu-id="089ff-118">Una transformación puede Agregar columnas de clave no principal al final de una tabla.</span><span class="sxs-lookup"><span data-stu-id="089ff-118">A transform can add non-primary key columns to the end of a table.</span></span> <span data-ttu-id="089ff-119">No se puede crear una transformación que agregue columnas de clave principal a una tabla.</span><span class="sxs-lookup"><span data-stu-id="089ff-119">A transform cannot be created that adds primary key columns to a table.</span></span> <span data-ttu-id="089ff-120">No se puede crear una transformación que cambia el orden, los nombres o las definiciones de las columnas.</span><span class="sxs-lookup"><span data-stu-id="089ff-120">A transform cannot be created that changes the order, names, or definitions of columns.</span></span>

<span data-ttu-id="089ff-121">Este método devuelve un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="089ff-121">This method returns a Boolean value.</span></span> <span data-ttu-id="089ff-122">Devuelve TRUE si se genera una transformación.</span><span class="sxs-lookup"><span data-stu-id="089ff-122">It returns TRUE if a transform is generated.</span></span> <span data-ttu-id="089ff-123">Devuelve FALSE si no se genera una transformación porque no hay ninguna diferencia entre las dos bases de datos.</span><span class="sxs-lookup"><span data-stu-id="089ff-123">It returns FALSE if a transform is not generated because there are no differences between the two databases.</span></span> <span data-ttu-id="089ff-124">Si se produce un error en el método, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="089ff-124">If the method fails, it generates an error.</span></span>

<span data-ttu-id="089ff-125">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="089ff-125">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="089ff-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="089ff-126">Requirements</span></span>



| <span data-ttu-id="089ff-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="089ff-127">Requirement</span></span> | <span data-ttu-id="089ff-128">Value</span><span class="sxs-lookup"><span data-stu-id="089ff-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="089ff-129">Versión</span><span class="sxs-lookup"><span data-stu-id="089ff-129">Version</span></span><br/> | <span data-ttu-id="089ff-130">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="089ff-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="089ff-131">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="089ff-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="089ff-132">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="089ff-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="089ff-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="089ff-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="089ff-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="089ff-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="089ff-135">IID</span><span class="sxs-lookup"><span data-stu-id="089ff-135">IID</span></span><br/>     | <span data-ttu-id="089ff-136">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="089ff-136">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="089ff-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="089ff-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="089ff-138">**Base de datos**</span><span class="sxs-lookup"><span data-stu-id="089ff-138">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="089ff-139">Transformaciones de base de datos</span><span class="sxs-lookup"><span data-stu-id="089ff-139">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




