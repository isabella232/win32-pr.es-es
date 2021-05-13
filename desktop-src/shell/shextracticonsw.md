---
description: Crea una matriz de identificadores para los iconos extraídos de un archivo especificado.
title: Función SHExtractIconsW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: 699b6d5473d97548a22e220372b9f53633cb2346
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840916"
---
# <a name="shextracticonsw-function"></a><span data-ttu-id="f01d4-103">Función SHExtractIconsW</span><span class="sxs-lookup"><span data-stu-id="f01d4-103">SHExtractIconsW function</span></span>

<span data-ttu-id="f01d4-104">\[**SHExtractIconsW** está disponible a través de Windows XP Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="f01d4-104">\[**SHExtractIconsW** is available through Windows XP Service Pack 2 (SP2).</span></span> <span data-ttu-id="f01d4-105">Podría modificarse o no estar disponible en versiones posteriores.\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="f01d4-106">Crea una matriz de identificadores para los iconos extraídos de un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="f01d4-106">Creates an array of handles to icons extracted from a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f01d4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f01d4-107">Syntax</span></span>


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a><span data-ttu-id="f01d4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f01d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f01d4-109">*pszFileName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-109">*pszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01d4-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="f01d4-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="f01d4-111">Puntero al nombre de archivo del que se extraen los iconos.</span><span class="sxs-lookup"><span data-stu-id="f01d4-111">A pointer to the file name from which to extract the icons.</span></span>

</dd> <dt>

<span data-ttu-id="f01d4-112">*nIconIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-112">*nIconIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01d4-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f01d4-113">Type: **int**</span></span>

<span data-ttu-id="f01d4-114">Índice del primer icono que se extraerá del recurso denominado *en pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="f01d4-114">The index of the first icon to extract from the resource named in *pszFileName*.</span></span>

</dd> <dt>

<span data-ttu-id="f01d4-115">*cxIcon* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-115">*cxIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01d4-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f01d4-116">Type: **int**</span></span>

<span data-ttu-id="f01d4-117">Ancho deseado del icono.</span><span class="sxs-lookup"><span data-stu-id="f01d4-117">The desired width of the icon.</span></span> <span data-ttu-id="f01d4-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f01d4-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f01d4-119">*cyIcon* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-119">*cyIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01d4-120">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f01d4-120">Type: **int**</span></span>

<span data-ttu-id="f01d4-121">Alto deseado del icono.</span><span class="sxs-lookup"><span data-stu-id="f01d4-121">The desired height of the icon.</span></span> <span data-ttu-id="f01d4-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f01d4-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f01d4-123">*phIcon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-123">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f01d4-124">Tipo: **HICON \***</span><span class="sxs-lookup"><span data-stu-id="f01d4-124">Type: **HICON\***</span></span>

<span data-ttu-id="f01d4-125">Cuando esta función devuelve un resultado, contiene un puntero a la matriz de identificadores de icono.</span><span class="sxs-lookup"><span data-stu-id="f01d4-125">When this function returns, contains a pointer to the array of icon handles.</span></span>

</dd> <dt>

<span data-ttu-id="f01d4-126">*pIconId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-126">*pIconId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f01d4-127">Tipo: **UINT \***</span><span class="sxs-lookup"><span data-stu-id="f01d4-127">Type: **UINT\***</span></span>

<span data-ttu-id="f01d4-128">Cuando esta función vuelve, contiene un puntero al identificador de recursos del icono extraído que mejor se adapta al dispositivo de visualización actual.</span><span class="sxs-lookup"><span data-stu-id="f01d4-128">When this function returns, contains a pointer to the resource identifier of the extracted icon that best fits the current display device.</span></span> <span data-ttu-id="f01d4-129">Si no hay ningún identificador disponible para este formato, contiene 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="f01d4-129">If there is no identifier available for this format, it contains 0xFFFFFFFF.</span></span> <span data-ttu-id="f01d4-130">Si no se puede obtener ningún identificador por cualquier otro motivo, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="f01d4-130">If no identifier can be obtained for any other reason, returns zero.</span></span>

</dd> <dt>

<span data-ttu-id="f01d4-131">*nIcons* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-131">*nIcons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01d4-132">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="f01d4-132">Type: **UINT**</span></span>

<span data-ttu-id="f01d4-133">Número de iconos que se extraerán del recurso denominado *en pszFileName.*</span><span class="sxs-lookup"><span data-stu-id="f01d4-133">The number of icons to extract from the resource named in *pszFileName*.</span></span> <span data-ttu-id="f01d4-134">Este parámetro solo es válido cuando el recurso es un archivo .exe o .dll.</span><span class="sxs-lookup"><span data-stu-id="f01d4-134">This parameter is valid only when the resource is a .exe or .dll file.</span></span>

</dd> <dt>

<span data-ttu-id="f01d4-135">*flags* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-135">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01d4-136">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="f01d4-136">Type: **UINT**</span></span>

<span data-ttu-id="f01d4-137">Marcas que controlan esta función.</span><span class="sxs-lookup"><span data-stu-id="f01d4-137">The flags that control this function.</span></span> <span data-ttu-id="f01d4-138">Para ver los valores posibles, *vea el parámetro fuLoad* de la [**función LoadImage.**](/windows/win32/api/winuser/nf-winuser-loadimagea)</span><span class="sxs-lookup"><span data-stu-id="f01d4-138">For possible values, see the *fuLoad* parameter of the [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f01d4-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f01d4-139">Return value</span></span>

<span data-ttu-id="f01d4-140">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="f01d4-140">Type: **UINT**</span></span>

<span data-ttu-id="f01d4-141">Valor distinto de cero si se realiza correctamente; de lo contrario, cero.</span><span class="sxs-lookup"><span data-stu-id="f01d4-141">A nonzero value if successful; otherwise, zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f01d4-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f01d4-142">Remarks</span></span>

<span data-ttu-id="f01d4-143">**SHExtractIconsW** extrae de los siguientes tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f01d4-143">**SHExtractIconsW** extracts from the following file types.</span></span>

-   <span data-ttu-id="f01d4-144">Ejecutable (.exe)</span><span class="sxs-lookup"><span data-stu-id="f01d4-144">Executable (.exe)</span></span>
-   <span data-ttu-id="f01d4-145">DLL (.dll)</span><span class="sxs-lookup"><span data-stu-id="f01d4-145">DLL (.dll)</span></span>
-   <span data-ttu-id="f01d4-146">Icono (.ico)</span><span class="sxs-lookup"><span data-stu-id="f01d4-146">Icon (.ico)</span></span>
-   <span data-ttu-id="f01d4-147">Cursor (.cur)</span><span class="sxs-lookup"><span data-stu-id="f01d4-147">Cursor (.cur)</span></span>
-   <span data-ttu-id="f01d4-148">Cursor animado (.ani)</span><span class="sxs-lookup"><span data-stu-id="f01d4-148">Animated cursor (.ani)</span></span>
-   <span data-ttu-id="f01d4-149">Mapa de bits (.bmp)</span><span class="sxs-lookup"><span data-stu-id="f01d4-149">Bitmap (.bmp)</span></span>

<span data-ttu-id="f01d4-150">Extracciones de Windows 3. *También se* admiten archivos ejecutables de 16 bits (.exe o .dll).</span><span class="sxs-lookup"><span data-stu-id="f01d4-150">Extractions from Windows 3.*x* 16-bit executable files (.exe or .dll) are also supported.</span></span>

<span data-ttu-id="f01d4-151">Los *parámetros cxIcon* *y cyIcon* especifican el tamaño de los iconos que se extraerán.</span><span class="sxs-lookup"><span data-stu-id="f01d4-151">The *cxIcon* and *cyIcon* parameters specify the size of the icons to extract.</span></span> <span data-ttu-id="f01d4-152">Se pueden extraer dos tamaños a través de cada parámetro dividiendo el valor entre su LOWORD y HIWORD.</span><span class="sxs-lookup"><span data-stu-id="f01d4-152">Two sizes can be extracted through each parameter by splitting the value between its LOWORD and HIWORD.</span></span> <span data-ttu-id="f01d4-153">Coloque el primer tamaño deseado en el LOWORD del parámetro y el segundo tamaño en HIWORD.</span><span class="sxs-lookup"><span data-stu-id="f01d4-153">Put the first desired size in the LOWORD of the parameter and the second size in the HIWORD.</span></span> <span data-ttu-id="f01d4-154">Por ejemplo, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) para *cxIcon* y *cyIcon* extrae iconos de tamaño 24 y 48.</span><span class="sxs-lookup"><span data-stu-id="f01d4-154">For example, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) for both *cxIcon* and *cyIcon* extracts both 24 and 48 sized icons.</span></span>

<span data-ttu-id="f01d4-155">El proceso de llamada es responsable de destruir todos los iconos extraídos a través de esta función mediante una llamada a la [**función DestroyIcon.**](/windows/win32/api/winuser/nf-winuser-destroyicon)</span><span class="sxs-lookup"><span data-stu-id="f01d4-155">The calling process is responsible for destroying all icons extracted through this function by calling the [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) function.</span></span>

<span data-ttu-id="f01d4-156">**SHExtractIconsW** no se exporta por nombre ni se declara en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="f01d4-156">**SHExtractIconsW** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="f01d4-157">Para usarlo, debe declarar un prototipo que coincida y usar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para solicitar un puntero de función de Shell32.dll que se pueda usar para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="f01d4-157">To use it, you must declare a matching prototype and use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to request a function pointer from Shell32.dll that can be used to call this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f01d4-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f01d4-158">Requirements</span></span>



| <span data-ttu-id="f01d4-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="f01d4-159">Requirement</span></span> | <span data-ttu-id="f01d4-160">Value</span><span class="sxs-lookup"><span data-stu-id="f01d4-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f01d4-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f01d4-161">Minimum supported client</span></span><br/> | <span data-ttu-id="f01d4-162">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f01d4-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f01d4-163">Minimum supported server</span></span><br/> | <span data-ttu-id="f01d4-164">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f01d4-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f01d4-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f01d4-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f01d4-166"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f01d4-166"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="f01d4-167">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f01d4-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f01d4-168">**SHExtractIconsW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="f01d4-168">**SHExtractIconsW** (Unicode)</span></span><br/>                                                                      |



 

 
