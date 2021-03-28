---
description: Lee una línea de Setup. inf y extrae el campo especificado de la cadena.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Función ParseField (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277413"
---
# <a name="parsefield-function"></a><span data-ttu-id="275a9-103">ParseField función)</span><span class="sxs-lookup"><span data-stu-id="275a9-103">ParseField function</span></span>

<span data-ttu-id="275a9-104">\[Actualmente se espera que la función **ParseField** esté disponible para su uso en la siguiente versión del sistema operativo Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="275a9-104">\[The **ParseField** function is currently expected to be available for use in the next version of the Microsoft Windows operating system.</span></span> <span data-ttu-id="275a9-105">Podría modificarse o no estar disponible en versiones posteriores.\]</span><span class="sxs-lookup"><span data-stu-id="275a9-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="275a9-106">Lee una línea de Setup. inf y extrae el campo especificado de la cadena.</span><span class="sxs-lookup"><span data-stu-id="275a9-106">Reads a line from Setup.inf and extracts the specified field from the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="275a9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="275a9-107">Syntax</span></span>


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="275a9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="275a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="275a9-109">*szData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="275a9-109">*szData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="275a9-110">Tipo: \**LPCTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="275a9-110">Type: \**LPCTSTR\** _</span></span>

<span data-ttu-id="275a9-111">Un puntero a la línea de Setup. inf.</span><span class="sxs-lookup"><span data-stu-id="275a9-111">A pointer to the line from Setup.inf.</span></span>

</dd> <dt>

<span data-ttu-id="275a9-112">_n \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="275a9-112">_n\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="275a9-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="275a9-113">Type: **int**</span></span>

<span data-ttu-id="275a9-114">**Entero** que indica el campo que se va a extraer.</span><span class="sxs-lookup"><span data-stu-id="275a9-114">**INT** that indicates which field to extract.</span></span>

<dt>



 <span data-ttu-id="275a9-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="275a9-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="275a9-116">Indica el campo delante de un signo igual (=).</span><span class="sxs-lookup"><span data-stu-id="275a9-116">Indicates the field before an equals sign (=).</span></span>

</dd> <dt>



 <span data-ttu-id="275a9-117">(1)</span><span class="sxs-lookup"><span data-stu-id="275a9-117">(1)</span></span>


</dt> <dd>

<span data-ttu-id="275a9-118">Indica el primer campo.</span><span class="sxs-lookup"><span data-stu-id="275a9-118">Indicates the first field.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="275a9-119">*szBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="275a9-119">*szBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="275a9-120">Tipo: \**LPTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="275a9-120">Type: \**LPTSTR\** _</span></span>

<span data-ttu-id="275a9-121">Puntero al búfer que recibe el campo extraído.</span><span class="sxs-lookup"><span data-stu-id="275a9-121">A pointer to the buffer that receives the extracted field.</span></span>

</dd> <dt>

<span data-ttu-id="275a9-122">_iBufLen \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="275a9-122">_iBufLen\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="275a9-123">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="275a9-123">Type: **int**</span></span>

<span data-ttu-id="275a9-124">**Int** que recibe el tamaño del búfer que recibe el campo extraído.</span><span class="sxs-lookup"><span data-stu-id="275a9-124">**INT** that receives the size of the buffer that receives the extracted field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="275a9-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="275a9-125">Return value</span></span>

<span data-ttu-id="275a9-126">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="275a9-126">Type: **bool**</span></span>

<span data-ttu-id="275a9-127">Devuelve **true** si la función es correcta y **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="275a9-127">Returns **TRUE** if the function is successful and **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="275a9-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="275a9-128">Remarks</span></span>

<span data-ttu-id="275a9-129">Los campos de la cadena deben estar separados por comas.</span><span class="sxs-lookup"><span data-stu-id="275a9-129">The fields in the string must be separated by commas.</span></span>

<span data-ttu-id="275a9-130">Se quitan los espacios iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="275a9-130">Leading and trailing spaces are removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="275a9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="275a9-131">Requirements</span></span>



| <span data-ttu-id="275a9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="275a9-132">Requirement</span></span> | <span data-ttu-id="275a9-133">Value</span><span class="sxs-lookup"><span data-stu-id="275a9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="275a9-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="275a9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="275a9-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="275a9-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="275a9-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="275a9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="275a9-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="275a9-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="275a9-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="275a9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="275a9-139"><dt>Util. h</dt></span><span class="sxs-lookup"><span data-stu-id="275a9-139"><dt>Util.h</dt></span></span> </dl>                             |
| <span data-ttu-id="275a9-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="275a9-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="275a9-141"><dt>Shell32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="275a9-141"><dt>Shell32.lib</dt></span></span> </dl>                        |
| <span data-ttu-id="275a9-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="275a9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="275a9-143"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="275a9-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




