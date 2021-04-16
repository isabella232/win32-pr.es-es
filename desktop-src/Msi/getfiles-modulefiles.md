---
description: La propiedad ModuleFiles del objeto GetFiles devuelve todas las claves principales de la tabla de archivos para el módulo actualmente abierto.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: Propiedad GetFiles. ModuleFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671651"
---
# <a name="getfilesmodulefiles-property"></a><span data-ttu-id="e2c07-103">Propiedad GetFiles. ModuleFiles</span><span class="sxs-lookup"><span data-stu-id="e2c07-103">GetFiles.ModuleFiles property</span></span>

<span data-ttu-id="e2c07-104">La propiedad **ModuleFiles** del objeto [**GetFiles**](getfiles-object.md) devuelve todas las claves principales de la [tabla de archivos](file-table.md) para el módulo actualmente abierto.</span><span class="sxs-lookup"><span data-stu-id="e2c07-104">**ModuleFiles** property of the [**GetFiles**](getfiles-object.md) object returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span> <span data-ttu-id="e2c07-105">Las claves principales se devuelven como una colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="e2c07-105">The primary keys are returned as a collection of strings.</span></span> <span data-ttu-id="e2c07-106">El módulo debe abrirse mediante una llamada al método [**OpenModule**](merge-openmodule.md) del [objeto Merge](merge-object.md) antes de llamar a **ModuleFiles**.</span><span class="sxs-lookup"><span data-stu-id="e2c07-106">The module must be opened by a call to the [**OpenModule**](merge-openmodule.md) method of the [Merge object](merge-object.md) before calling **ModuleFiles**.</span></span>

<span data-ttu-id="e2c07-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e2c07-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c07-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2c07-108">Syntax</span></span>


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a><span data-ttu-id="e2c07-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e2c07-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e2c07-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2c07-110">Remarks</span></span>

<span data-ttu-id="e2c07-111">Tenga en cuenta que el orden de los archivos enumerados en la colección puede no estar en la misma secuencia que se muestra en la tabla de archivos.</span><span class="sxs-lookup"><span data-stu-id="e2c07-111">Note that order of the files listed in the collection may not be in the same sequence as listed in the File table.</span></span>

<span data-ttu-id="e2c07-112">Si el módulo no tiene ninguna tabla de archivos o no contiene ningún archivo en el idioma en particular, ModuleFiles devuelve una colección vacía de cadenas.</span><span class="sxs-lookup"><span data-stu-id="e2c07-112">If the module has no File table, or contains no files in the particular language, ModuleFiles returns an empty collection of strings.</span></span>

### <a name="c"></a><span data-ttu-id="e2c07-113">C++</span><span class="sxs-lookup"><span data-stu-id="e2c07-113">C++</span></span>

<span data-ttu-id="e2c07-114">Consulte [**Get \_ ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.</span><span class="sxs-lookup"><span data-stu-id="e2c07-114">See [**get\_ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2c07-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2c07-115">Requirements</span></span>



| <span data-ttu-id="e2c07-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2c07-116">Requirement</span></span> | <span data-ttu-id="e2c07-117">Value</span><span class="sxs-lookup"><span data-stu-id="e2c07-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c07-118">Versión</span><span class="sxs-lookup"><span data-stu-id="e2c07-118">Version</span></span><br/> | <span data-ttu-id="e2c07-119">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e2c07-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="e2c07-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2c07-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e2c07-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2c07-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2c07-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2c07-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2c07-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2c07-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
