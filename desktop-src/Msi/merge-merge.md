---
description: El método Merge del objeto Merge ejecuta una combinación de la base de datos actual y el módulo actual.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Merge. Merge (método) (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653903"
---
# <a name="mergemerge-method"></a><span data-ttu-id="b5e93-103">Merge. Merge (método)</span><span class="sxs-lookup"><span data-stu-id="b5e93-103">Merge.Merge method</span></span>

<span data-ttu-id="b5e93-104">El método **Merge** del objeto [**Merge**](merge-object.md) ejecuta una combinación de la base de datos actual y el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="b5e93-104">The **Merge** method of the [**Merge**](merge-object.md) object executes a merge of the current database and current module.</span></span> <span data-ttu-id="b5e93-105">La combinación adjunta los componentes del módulo a la característica identificada por la *característica*.</span><span class="sxs-lookup"><span data-stu-id="b5e93-105">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="b5e93-106">La raíz del árbol de directorios del módulo se redirige a la ubicación especificada por *RedirectDir*.</span><span class="sxs-lookup"><span data-stu-id="b5e93-106">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

<span data-ttu-id="b5e93-107">Solo se puede llamar una vez al método **Merge** para combinar una combinación determinada de archivos. msi y. msm.</span><span class="sxs-lookup"><span data-stu-id="b5e93-107">The **Merge** method can only be called once to merge a particular combination of .msi and .msm files.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5e93-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5e93-108">Syntax</span></span>


```JScript
Merge.Merge(
  Feature,
  RedirectDir
)
```



## <a name="parameters"></a><span data-ttu-id="b5e93-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5e93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5e93-110">*Característica*</span><span class="sxs-lookup"><span data-stu-id="b5e93-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="b5e93-111">El nombre de una característica en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b5e93-111">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="b5e93-112">*RedirectDir*</span><span class="sxs-lookup"><span data-stu-id="b5e93-112">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="b5e93-113">La clave de una entrada en la [tabla de directorios](directory-table.md) de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b5e93-113">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="b5e93-114">Este parámetro puede ser null o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="b5e93-114">This parameter may be null or an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5e93-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5e93-115">Return value</span></span>

<span data-ttu-id="b5e93-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b5e93-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5e93-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5e93-117">Remarks</span></span>

<span data-ttu-id="b5e93-118">Una vez completada la combinación, los componentes del módulo se adjuntan a la característica identificada por la *característica*.</span><span class="sxs-lookup"><span data-stu-id="b5e93-118">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="b5e93-119">Esta característica no se crea y debe ser una característica existente.</span><span class="sxs-lookup"><span data-stu-id="b5e93-119">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="b5e93-120">Tenga en cuenta que el método **Merge** obtiene todas las referencias de características en el módulo y sustituye la referencia de características de todas las apariciones del GUID null en la base de datos del módulo.</span><span class="sxs-lookup"><span data-stu-id="b5e93-120">Note that the **Merge** method gets all the feature references in the module and substitutes the feature reference for all occurrences of the null GUID in the module database.</span></span> <span data-ttu-id="b5e93-121">Para obtener más información, vea [hacer referencia a características en módulos de combinación](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="b5e93-121">For more information, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>

<span data-ttu-id="b5e93-122">El módulo se puede adjuntar a características adicionales mediante el método [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="b5e93-122">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span> <span data-ttu-id="b5e93-123">Tenga en cuenta que llamar al método **Connect** solo crea asociaciones de componentes de características.</span><span class="sxs-lookup"><span data-stu-id="b5e93-123">Note that calling the **Connect** method only creates feature-component associations.</span></span> <span data-ttu-id="b5e93-124">No modifica las filas que ya se han combinado en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b5e93-124">It does not modify the rows that have already been merged in to the database.</span></span>

<span data-ttu-id="b5e93-125">Los cambios realizados en la base de datos se guardan si y solo si se llama al método [**CerrarBaseDeDatos**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) con *BCommit* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="b5e93-125">Changes made to the database are saved if and only if the [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="b5e93-126">Si se producen conflictos de combinación, incluidas las exclusiones, se colocan en el enumerador de errores para su posterior recuperación, pero no se produce un error en la combinación.</span><span class="sxs-lookup"><span data-stu-id="b5e93-126">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="b5e93-127">Los errores se pueden recuperar a través de la propiedad [**errores**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b5e93-127">Errors may be retrieved through the [**Errors**](error-object.md) property.</span></span> <span data-ttu-id="b5e93-128">Los errores y los mensajes informativos se publican en el archivo de registro actual.</span><span class="sxs-lookup"><span data-stu-id="b5e93-128">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="b5e93-129">C++</span><span class="sxs-lookup"><span data-stu-id="b5e93-129">C++</span></span>

<span data-ttu-id="b5e93-130">Vea función [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) .</span><span class="sxs-lookup"><span data-stu-id="b5e93-130">See [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5e93-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5e93-131">Requirements</span></span>



| <span data-ttu-id="b5e93-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5e93-132">Requirement</span></span> | <span data-ttu-id="b5e93-133">Value</span><span class="sxs-lookup"><span data-stu-id="b5e93-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e93-134">Versión</span><span class="sxs-lookup"><span data-stu-id="b5e93-134">Version</span></span><br/> | <span data-ttu-id="b5e93-135">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b5e93-135">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="b5e93-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5e93-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b5e93-137"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5e93-137"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5e93-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5e93-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5e93-139"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5e93-139"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
