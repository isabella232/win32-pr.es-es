---
title: VER. scriptFile
description: El atributo scriptFile especifica los nombres de archivo de los archivos JScript que lo acompañan.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- VIEW. scriptFile Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649991"
---
# <a name="viewscriptfile"></a><span data-ttu-id="dba3d-104">VER. scriptFile</span><span class="sxs-lookup"><span data-stu-id="dba3d-104">VIEW.scriptFile</span></span>

<span data-ttu-id="dba3d-105">El atributo **scriptFile** especifica los nombres de archivo de los archivos JScript que lo acompañan.</span><span class="sxs-lookup"><span data-stu-id="dba3d-105">The **scriptFile** attribute specifies the file names of accompanying JScript files.</span></span>

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a><span data-ttu-id="dba3d-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="dba3d-106">Possible Values</span></span>

<span data-ttu-id="dba3d-107">Este atributo es una **cadena** de solo escritura sin ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dba3d-107">This attribute is a write-only **String** with no default value.</span></span> <span data-ttu-id="dba3d-108">Los nombres de archivo de varios archivos JScript están delimitados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="dba3d-108">The file names of multiple JScript files are delimited with semicolons.</span></span> <span data-ttu-id="dba3d-109">Los espacios iniciales y siguientes y los signos de punto y coma no deben estar presentes.</span><span class="sxs-lookup"><span data-stu-id="dba3d-109">Leading and following spaces and semicolons should not be present.</span></span>

## <a name="remarks"></a><span data-ttu-id="dba3d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dba3d-110">Remarks</span></span>

<span data-ttu-id="dba3d-111">Cualquier controlador de eventos de la vista puede utilizar el código de los archivos especificados.</span><span class="sxs-lookup"><span data-stu-id="dba3d-111">The code in the specified files can be used by any event handler in the View.</span></span> <span data-ttu-id="dba3d-112">El código que usan los controladores de eventos en varias vistas puede colocarse en un archivo con el mismo nombre que el archivo de definición de máscara, pero con una extensión. js en lugar de una extensión. WMS.</span><span class="sxs-lookup"><span data-stu-id="dba3d-112">Code that is used by event handlers in multiple Views can be placed in a file with the same name as the skin definition file but with a .js extension instead of a .wms extension.</span></span> <span data-ttu-id="dba3d-113">Este archivo se carga automáticamente y no es necesario especificarlo en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="dba3d-113">This file is loaded automatically and need not be specified in the skin definition file.</span></span>

## <a name="examples"></a><span data-ttu-id="dba3d-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dba3d-114">Examples</span></span>


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a><span data-ttu-id="dba3d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dba3d-115">Requirements</span></span>



| <span data-ttu-id="dba3d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dba3d-116">Requirement</span></span> | <span data-ttu-id="dba3d-117">Value</span><span class="sxs-lookup"><span data-stu-id="dba3d-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="dba3d-118">Versión</span><span class="sxs-lookup"><span data-stu-id="dba3d-118">Version</span></span><br/> | <span data-ttu-id="dba3d-119">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="dba3d-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dba3d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="dba3d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba3d-121">**Elemento de vista**</span><span class="sxs-lookup"><span data-stu-id="dba3d-121">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





