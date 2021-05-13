---
description: Calcula el riesgo de ejecutar código desconocido cuando se llama a un controlador en un archivo determinado. Este riesgo se basa en una comprensión del controlador y del contenido de código del archivo.
title: Función EstimateFileRiskLevel
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
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841436"
---
# <a name="estimatefilerisklevel-function"></a><span data-ttu-id="be53c-104">Función EstimateFileRiskLevel</span><span class="sxs-lookup"><span data-stu-id="be53c-104">EstimateFileRiskLevel function</span></span>

<span data-ttu-id="be53c-105">\[Esta función está disponible en Windows XP con Service Pack 2 (SP2) a través de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be53c-105">\[This function is available on Windows XP with Service Pack 2 (SP2) through Windows Vista.</span></span> <span data-ttu-id="be53c-106">Podría modificarse o no estar disponible en versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="be53c-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="be53c-107">En su lugar, las aplicaciones cliente deben usar [**IAttachmentExecute para**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) presentar un entorno de usuario que proporciona descarga e intercambio seguro de archivos a través de correo electrónico y datos adjuntos de mensajería.\]</span><span class="sxs-lookup"><span data-stu-id="be53c-107">Client applications instead should use [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) to present a user environment that provides safe download and exchange of files through email and messaging attachments.\]</span></span>

<span data-ttu-id="be53c-108">Calcula el riesgo de ejecutar código desconocido cuando se llama a un controlador en un archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="be53c-108">Estimates the risk of executing unknown code when a handler is called on a given file.</span></span> <span data-ttu-id="be53c-109">Este riesgo se basa en una comprensión del controlador y del contenido de código del archivo.</span><span class="sxs-lookup"><span data-stu-id="be53c-109">This risk is based on an understanding of the handler and the code content of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="be53c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be53c-110">Syntax</span></span>


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a><span data-ttu-id="be53c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be53c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be53c-112">*pszFilePath* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="be53c-112">*pszFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be53c-113">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="be53c-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="be53c-114">Puntero a una cadena terminada en NULL que contiene la ruta de acceso del archivo que se comprueba con el controlador.</span><span class="sxs-lookup"><span data-stu-id="be53c-114">A pointer to a null-terminated string that contains the path of the file that is being checked against the handler.</span></span>

</dd> <dt>

<span data-ttu-id="be53c-115">*pszExt* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="be53c-115">*pszExt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be53c-116">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="be53c-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="be53c-117">Puntero a una cadena terminada en NULL que contiene la extensión del archivo que se está compruebando, ya sea con o sin su período inicial.</span><span class="sxs-lookup"><span data-stu-id="be53c-117">A pointer to a null-terminated string that contains the extension of the file that is being checked, either with or without its leading period.</span></span> <span data-ttu-id="be53c-118">Por ejemplo, ".txt" o "txt".</span><span class="sxs-lookup"><span data-stu-id="be53c-118">For instance, ".txt" or "txt".</span></span>

</dd> <dt>

<span data-ttu-id="be53c-119">*pszHandler* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="be53c-119">*pszHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be53c-120">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="be53c-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="be53c-121">Puntero a una cadena terminada en NULL que contiene la ruta de acceso del controlador para el archivo.</span><span class="sxs-lookup"><span data-stu-id="be53c-121">A pointer to a null-terminated string that contains the path of the handler for the file.</span></span>

</dd> <dt>

<span data-ttu-id="be53c-122">*pfrlEstimate* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="be53c-122">*pfrlEstimate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be53c-123">Tipo: **NIVEL DE RIESGO DE \_ \_ ARCHIVO \***</span><span class="sxs-lookup"><span data-stu-id="be53c-123">Type: **FILE\_RISK\_LEVEL\***</span></span>

<span data-ttu-id="be53c-124">Cuando esta función se devuelve correctamente, contiene un puntero a uno de los valores siguientes que indica el riesgo estimado.</span><span class="sxs-lookup"><span data-stu-id="be53c-124">When this function returns successfully, contains a pointer to one of the following values that state the estimated risk.</span></span>

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span data-ttu-id="be53c-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL \_ SIN \_ OPINIÓN** (0)</span><span class="sxs-lookup"><span data-stu-id="be53c-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL\_NO\_OPINION** (0)</span></span>


</dt> <dd>

<span data-ttu-id="be53c-126">No se identifica el formato del archivo o no se identifica el controlador.</span><span class="sxs-lookup"><span data-stu-id="be53c-126">The format of the file is not identified or the handler is not identified.</span></span> <span data-ttu-id="be53c-127">Información insuficiente disponible para una respuesta significativa.</span><span class="sxs-lookup"><span data-stu-id="be53c-127">Insufficient information available for a meaningful answer.</span></span>

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span data-ttu-id="be53c-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ LOW** (1)</span><span class="sxs-lookup"><span data-stu-id="be53c-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL\_LOW** (1)</span></span>


</dt> <dd>

<span data-ttu-id="be53c-129">El formato del archivo se entiende completamente, se conoce el controlador y hay una gran confianza en que no se ejecutará ningún código extraneous.</span><span class="sxs-lookup"><span data-stu-id="be53c-129">The format of the file is completely understood, the handler is known, and there is high confidence that no extraneous code will be executed.</span></span>

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span data-ttu-id="be53c-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERATE** (2)</span><span class="sxs-lookup"><span data-stu-id="be53c-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL\_MODERATE** (2)</span></span>


</dt> <dd>

<span data-ttu-id="be53c-131">Se identifica el formato del archivo, pero no se entiende lo suficiente para etiquetar como un riesgo alto o bajo.</span><span class="sxs-lookup"><span data-stu-id="be53c-131">The format of the file is identified, but it is not sufficiently understood to label as either a high or low risk.</span></span>

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span data-ttu-id="be53c-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ HIGH** (3)</span><span class="sxs-lookup"><span data-stu-id="be53c-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL\_HIGH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="be53c-133">Se entiende el formato de archivo y se han identificado factores de riesgo elevados.</span><span class="sxs-lookup"><span data-stu-id="be53c-133">The file format is understood and elevated risk factors have been identified.</span></span>

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span data-ttu-id="be53c-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOCK** (4)</span><span class="sxs-lookup"><span data-stu-id="be53c-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL\_BLOCK** (4)</span></span>


</dt> <dd>

<span data-ttu-id="be53c-135">El formato de archivo está bloqueado específicamente para este controlador.</span><span class="sxs-lookup"><span data-stu-id="be53c-135">The file format is specifically blocked for this handler.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be53c-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be53c-136">Return value</span></span>

<span data-ttu-id="be53c-137">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="be53c-137">Type: **HRESULT**</span></span>

<span data-ttu-id="be53c-138">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="be53c-138">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be53c-139">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="be53c-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be53c-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be53c-140">Remarks</span></span>

<span data-ttu-id="be53c-141">Esta función no se declara en un encabezado público ni se incluye en un archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="be53c-141">This function is not declared in a public header or included in a library file.</span></span> <span data-ttu-id="be53c-142">Para usarlo, debe cargarlo directamente desde Winshfhc.dll ordinal 101.</span><span class="sxs-lookup"><span data-stu-id="be53c-142">To use it you must load it directly from Winshfhc.dll by ordinal 101.</span></span>

## <a name="requirements"></a><span data-ttu-id="be53c-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be53c-143">Requirements</span></span>



| <span data-ttu-id="be53c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="be53c-144">Requirement</span></span> | <span data-ttu-id="be53c-145">Value</span><span class="sxs-lookup"><span data-stu-id="be53c-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be53c-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be53c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="be53c-147">Windows XP solo con aplicaciones de escritorio sp2 \[\]</span><span class="sxs-lookup"><span data-stu-id="be53c-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="be53c-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be53c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="be53c-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="be53c-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="be53c-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be53c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be53c-151"><dt>Winshfhc.dll (versión 5.1 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="be53c-151"><dt>Winshfhc.dll (version 5.1 or later)</dt></span></span> </dl> |



 

 




