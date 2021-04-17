---
description: El método MergeEx del objeto Merge es equivalente a la función Merge, salvo que toma un argumento adicional.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Método Merge. MergeEx (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679283"
---
# <a name="mergemergeex-method"></a><span data-ttu-id="5b6f9-103">Merge. MergeEx (método)</span><span class="sxs-lookup"><span data-stu-id="5b6f9-103">Merge.MergeEx method</span></span>

<span data-ttu-id="5b6f9-104">El método **MergeEx** del objeto [**Merge**](merge-object.md) es equivalente a la función [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , salvo que toma un argumento adicional.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-104">The **MergeEx** method of the [**Merge**](merge-object.md) object is equivalent to the [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function, except that it takes an extra argument.</span></span> <span data-ttu-id="5b6f9-105">El argumento *pConfiguration* es una interfaz implementada por el cliente.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-105">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="5b6f9-106">El argumento puede ser null.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-106">The argument may be null.</span></span> <span data-ttu-id="5b6f9-107">La presencia de este argumento indica que el cliente es capaz de admitir la funcionalidad de configuración, pero no obliga al cliente a proporcionar datos de configuración para ningún elemento configurable específico.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-107">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

<span data-ttu-id="5b6f9-108">El método [**Merge**](merge-merge.md) ejecuta una combinación de la base de datos actual y el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-108">The [**Merge**](merge-merge.md) method executes a merge of the current database and current module.</span></span> <span data-ttu-id="5b6f9-109">La combinación adjunta los componentes del módulo a la característica identificada por la *característica*.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-109">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="5b6f9-110">La raíz del árbol de directorios del módulo se redirige a la ubicación especificada por *RedirectDir*.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-110">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b6f9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b6f9-111">Syntax</span></span>


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
)
```



## <a name="parameters"></a><span data-ttu-id="5b6f9-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b6f9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b6f9-113">*Característica*</span><span class="sxs-lookup"><span data-stu-id="5b6f9-113">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="5b6f9-114">El nombre de una característica en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-114">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="5b6f9-115">*RedirectDir*</span><span class="sxs-lookup"><span data-stu-id="5b6f9-115">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="5b6f9-116">La clave de una entrada en la [tabla de directorios](directory-table.md) de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-116">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="5b6f9-117">Este parámetro puede ser null o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-117">This parameter may be null or an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="5b6f9-118">*pConfiguration*</span><span class="sxs-lookup"><span data-stu-id="5b6f9-118">*pConfiguration*</span></span> 
</dt> <dd>

<span data-ttu-id="5b6f9-119">El argumento *pConfiguration* es una interfaz implementada por el cliente.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-119">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="5b6f9-120">El argumento puede ser null.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-120">The argument may be null.</span></span> <span data-ttu-id="5b6f9-121">La presencia de este argumento indica que el cliente es capaz de admitir la funcionalidad de configuración, pero no obliga al cliente a proporcionar datos de configuración para ningún elemento configurable específico.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-121">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b6f9-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b6f9-122">Return value</span></span>

<span data-ttu-id="5b6f9-123">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b6f9-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b6f9-124">Remarks</span></span>

<span data-ttu-id="5b6f9-125">Una vez completada la combinación, los componentes del módulo se adjuntan a la característica identificada por la *característica*.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-125">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="5b6f9-126">Esta característica no se crea y debe ser una característica existente.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-126">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="5b6f9-127">El módulo se puede adjuntar a características adicionales mediante el método [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="5b6f9-127">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span>

<span data-ttu-id="5b6f9-128">Los cambios realizados en la base de datos se guardan si y solo si se llama al método [**CerrarBaseDeDatos**](merge-closedatabase.md) con *BCommit* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-128">Changes made to the database are saved if and only if the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="5b6f9-129">Si se producen conflictos de combinación, incluidas las exclusiones, se colocan en el enumerador de errores para su posterior recuperación, pero no se produce un error en la combinación.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-129">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="5b6f9-130">Los errores se pueden recuperar a través de la propiedad [**errores**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="5b6f9-130">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="5b6f9-131">Los errores y los mensajes informativos se publican en el archivo de registro actual.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-131">Errors and informational messages are posted to the current log file.</span></span>

<span data-ttu-id="5b6f9-132">Cuando se produce un error en la combinación debido a una configuración incorrecta del módulo, la función [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) devuelve E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-132">When the merge fails because of an incorrect module configuration the [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function returns E\_FAIL.</span></span> <span data-ttu-id="5b6f9-133">Esto incluye estos errores de msmErrorType: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem** y **msmErrorDataRequestFailed**.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-133">This includes these msmErrorType errors: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem**, and **msmErrorDataRequestFailed**.</span></span> <span data-ttu-id="5b6f9-134">Estos errores hacen que la combinación se detenga inmediatamente cuando se produce el error.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-134">These errors cause the merge to stop immediately when the error is encountered.</span></span> <span data-ttu-id="5b6f9-135">El objeto de error se sigue agregando al enumerador cuando **MergeEx** devuelve E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-135">The error object is still added to the enumerator when **MergeEx** returns E\_FAIL.</span></span> <span data-ttu-id="5b6f9-136">Para obtener más información sobre los errores de msmErrorType, consulte [**Get \_ Type function (objeto de error)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span><span class="sxs-lookup"><span data-stu-id="5b6f9-136">For more information about msmErrorType errors, see [**get\_Type Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span></span> <span data-ttu-id="5b6f9-137">Todos los demás errores hacen que **MergeEx** devuelva S \_ false y provoque que la combinación continúe.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-137">All other errors cause **MergeEx** to return S\_FALSE and cause the merge to continue.</span></span>

### <a name="c"></a><span data-ttu-id="5b6f9-138">C++</span><span class="sxs-lookup"><span data-stu-id="5b6f9-138">C++</span></span>

<span data-ttu-id="5b6f9-139">Consulte función [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) .</span><span class="sxs-lookup"><span data-stu-id="5b6f9-139">See [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b6f9-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b6f9-140">Requirements</span></span>



| <span data-ttu-id="5b6f9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b6f9-141">Requirement</span></span> | <span data-ttu-id="5b6f9-142">Value</span><span class="sxs-lookup"><span data-stu-id="5b6f9-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f9-143">Versión</span><span class="sxs-lookup"><span data-stu-id="5b6f9-143">Version</span></span><br/> | <span data-ttu-id="5b6f9-144">Mergemod.dll 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5b6f9-144">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5b6f9-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b6f9-145">Header</span></span><br/>  | <dl> <span data-ttu-id="5b6f9-146"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b6f9-146"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b6f9-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b6f9-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b6f9-148"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b6f9-148"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
