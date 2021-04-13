---
description: Calcula el riesgo de ejecutar código desconocido cuando se llama a un controlador en un archivo determinado. Este riesgo se basa en una comprensión del controlador y el contenido del código del archivo.
title: EstimateFileRiskLevel función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 96798e0bc64b39ae7f18d58b97fafafc9dc2508b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985903"
---
# <a name="estimatefilerisklevel-function"></a><span data-ttu-id="13ab7-104">EstimateFileRiskLevel función)</span><span class="sxs-lookup"><span data-stu-id="13ab7-104">EstimateFileRiskLevel function</span></span>

<span data-ttu-id="13ab7-105">\[Esta función está disponible en Windows XP con Service Pack 2 (SP2) a través de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13ab7-105">\[This function is available on Windows XP with Service Pack 2 (SP2) through Windows Vista.</span></span> <span data-ttu-id="13ab7-106">Podría modificarse o no estar disponible en versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="13ab7-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="13ab7-107">En su lugar, las aplicaciones cliente deben usar [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) para presentar un entorno de usuario que proporcione descarga e intercambio seguro de archivos a través de mensajes de correo electrónico y datos adjuntos.\]</span><span class="sxs-lookup"><span data-stu-id="13ab7-107">Client applications instead should use [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) to present a user environment that provides safe download and exchange of files through email and messaging attachments.\]</span></span>

<span data-ttu-id="13ab7-108">Calcula el riesgo de ejecutar código desconocido cuando se llama a un controlador en un archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="13ab7-108">Estimates the risk of executing unknown code when a handler is called on a given file.</span></span> <span data-ttu-id="13ab7-109">Este riesgo se basa en una comprensión del controlador y el contenido del código del archivo.</span><span class="sxs-lookup"><span data-stu-id="13ab7-109">This risk is based on an understanding of the handler and the code content of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ab7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13ab7-110">Syntax</span></span>


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a><span data-ttu-id="13ab7-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13ab7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ab7-112">*pszFilePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13ab7-112">*pszFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ab7-113">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="13ab7-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="13ab7-114">Puntero a una cadena terminada en null que contiene la ruta de acceso del archivo que se va a comprobar en el controlador.</span><span class="sxs-lookup"><span data-stu-id="13ab7-114">A pointer to a null-terminated string that contains the path of the file that is being checked against the handler.</span></span>

</dd> <dt>

<span data-ttu-id="13ab7-115">*pszExt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13ab7-115">*pszExt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ab7-116">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="13ab7-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="13ab7-117">Un puntero a una cadena terminada en null que contiene la extensión del archivo que se está comprobando, con o sin el punto inicial.</span><span class="sxs-lookup"><span data-stu-id="13ab7-117">A pointer to a null-terminated string that contains the extension of the file that is being checked, either with or without its leading period.</span></span> <span data-ttu-id="13ab7-118">Por ejemplo, ". txt" o "txt".</span><span class="sxs-lookup"><span data-stu-id="13ab7-118">For instance, ".txt" or "txt".</span></span>

</dd> <dt>

<span data-ttu-id="13ab7-119">*pszHandler* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13ab7-119">*pszHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ab7-120">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="13ab7-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="13ab7-121">Un puntero a una cadena terminada en null que contiene la ruta de acceso del controlador del archivo.</span><span class="sxs-lookup"><span data-stu-id="13ab7-121">A pointer to a null-terminated string that contains the path of the handler for the file.</span></span>

</dd> <dt>

<span data-ttu-id="13ab7-122">*pfrlEstimate* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="13ab7-122">*pfrlEstimate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13ab7-123">Tipo: \**\_ \_ nivel \* de riesgo de archivo* _</span><span class="sxs-lookup"><span data-stu-id="13ab7-123">Type: \**FILE\_RISK\_LEVEL\** _</span></span>

<span data-ttu-id="13ab7-124">Cuando esta función se devuelve correctamente, contiene un puntero a uno de los valores siguientes que indican el riesgo estimado.</span><span class="sxs-lookup"><span data-stu-id="13ab7-124">When this function returns successfully, contains a pointer to one of the following values that state the estimated risk.</span></span>

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span data-ttu-id="13ab7-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>_ *FRL \_ sin \_ opinión*\* (0)</span><span class="sxs-lookup"><span data-stu-id="13ab7-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>_ *FRL\_NO\_OPINION*\* (0)</span></span>


</dt> <dd>

<span data-ttu-id="13ab7-126">El formato del archivo no está identificado o el controlador no está identificado.</span><span class="sxs-lookup"><span data-stu-id="13ab7-126">The format of the file is not identified or the handler is not identified.</span></span> <span data-ttu-id="13ab7-127">No hay información disponible para una respuesta significativa.</span><span class="sxs-lookup"><span data-stu-id="13ab7-127">Insufficient information available for a meaningful answer.</span></span>

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span data-ttu-id="13ab7-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ BAJO** (1)</span><span class="sxs-lookup"><span data-stu-id="13ab7-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL\_LOW** (1)</span></span>


</dt> <dd>

<span data-ttu-id="13ab7-129">El formato del archivo se entiende por completo, se conoce el controlador y hay mucha confianza de que no se ejecutará ningún código extraño.</span><span class="sxs-lookup"><span data-stu-id="13ab7-129">The format of the file is completely understood, the handler is known, and there is high confidence that no extraneous code will be executed.</span></span>

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span data-ttu-id="13ab7-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERADO** (2)</span><span class="sxs-lookup"><span data-stu-id="13ab7-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL\_MODERATE** (2)</span></span>


</dt> <dd>

<span data-ttu-id="13ab7-131">Se identifica el formato del archivo, pero no se entiende lo suficientemente como como riesgo alto o bajo.</span><span class="sxs-lookup"><span data-stu-id="13ab7-131">The format of the file is identified, but it is not sufficiently understood to label as either a high or low risk.</span></span>

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span data-ttu-id="13ab7-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ ALTO** (3)</span><span class="sxs-lookup"><span data-stu-id="13ab7-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL\_HIGH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="13ab7-133">Se entiende el formato de archivo y se han identificado los factores de riesgo elevados.</span><span class="sxs-lookup"><span data-stu-id="13ab7-133">The file format is understood and elevated risk factors have been identified.</span></span>

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span data-ttu-id="13ab7-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOQUE** (4)</span><span class="sxs-lookup"><span data-stu-id="13ab7-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL\_BLOCK** (4)</span></span>


</dt> <dd>

<span data-ttu-id="13ab7-135">El formato de archivo está bloqueado específicamente para este controlador.</span><span class="sxs-lookup"><span data-stu-id="13ab7-135">The file format is specifically blocked for this handler.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ab7-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13ab7-136">Return value</span></span>

<span data-ttu-id="13ab7-137">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="13ab7-137">Type: **HRESULT**</span></span>

<span data-ttu-id="13ab7-138">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="13ab7-138">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13ab7-139">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="13ab7-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="13ab7-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13ab7-140">Remarks</span></span>

<span data-ttu-id="13ab7-141">Esta función no se declara en un encabezado público o se incluye en un archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="13ab7-141">This function is not declared in a public header or included in a library file.</span></span> <span data-ttu-id="13ab7-142">Para usarlo, debe cargarlo directamente desde Winshfhc.dll por el ordinal 101.</span><span class="sxs-lookup"><span data-stu-id="13ab7-142">To use it you must load it directly from Winshfhc.dll by ordinal 101.</span></span>

## <a name="requirements"></a><span data-ttu-id="13ab7-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13ab7-143">Requirements</span></span>



| <span data-ttu-id="13ab7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="13ab7-144">Requirement</span></span> | <span data-ttu-id="13ab7-145">Value</span><span class="sxs-lookup"><span data-stu-id="13ab7-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13ab7-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13ab7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="13ab7-147">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="13ab7-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13ab7-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13ab7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="13ab7-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="13ab7-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13ab7-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13ab7-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13ab7-151"><dt>Winshfhc.dll (versión 5,1 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="13ab7-151"><dt>Winshfhc.dll (version 5.1 or later)</dt></span></span> </dl> |



 

 




