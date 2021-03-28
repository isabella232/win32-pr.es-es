---
description: Crea una matriz de identificadores para los iconos extraídos de un archivo especificado.
title: SHExtractIconsW función)
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
ms.openlocfilehash: d82eb48d45210ebf12464708b09fe469d97432db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997769"
---
# <a name="shextracticonsw-function"></a><span data-ttu-id="89c6b-103">SHExtractIconsW función)</span><span class="sxs-lookup"><span data-stu-id="89c6b-103">SHExtractIconsW function</span></span>

<span data-ttu-id="89c6b-104">\[**SHExtractIconsW** está disponible a través de Windows XP Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="89c6b-104">\[**SHExtractIconsW** is available through Windows XP Service Pack 2 (SP2).</span></span> <span data-ttu-id="89c6b-105">Podría modificarse o no estar disponible en versiones posteriores.\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="89c6b-106">Crea una matriz de identificadores para los iconos extraídos de un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="89c6b-106">Creates an array of handles to icons extracted from a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c6b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89c6b-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="89c6b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89c6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89c6b-109">*pszFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-109">*pszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6b-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="89c6b-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="89c6b-111">Puntero al nombre de archivo del que se van a extraer los iconos.</span><span class="sxs-lookup"><span data-stu-id="89c6b-111">A pointer to the file name from which to extract the icons.</span></span>

</dd> <dt>

<span data-ttu-id="89c6b-112">*nIconIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-112">*nIconIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6b-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="89c6b-113">Type: **int**</span></span>

<span data-ttu-id="89c6b-114">Índice del primer icono que se va a extraer del recurso denominado en *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="89c6b-114">The index of the first icon to extract from the resource named in *pszFileName*.</span></span>

</dd> <dt>

<span data-ttu-id="89c6b-115">*cxIcon* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-115">*cxIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6b-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="89c6b-116">Type: **int**</span></span>

<span data-ttu-id="89c6b-117">Ancho deseado del icono.</span><span class="sxs-lookup"><span data-stu-id="89c6b-117">The desired width of the icon.</span></span> <span data-ttu-id="89c6b-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="89c6b-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="89c6b-119">*cyIcon* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-119">*cyIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6b-120">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="89c6b-120">Type: **int**</span></span>

<span data-ttu-id="89c6b-121">Alto deseado del icono.</span><span class="sxs-lookup"><span data-stu-id="89c6b-121">The desired height of the icon.</span></span> <span data-ttu-id="89c6b-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="89c6b-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="89c6b-123">*phIcon* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-123">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6b-124">Tipo: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="89c6b-124">Type: \**HICON\** _</span></span>

<span data-ttu-id="89c6b-125">Cuando esta función devuelve un, contiene un puntero a la matriz de identificadores de icono.</span><span class="sxs-lookup"><span data-stu-id="89c6b-125">When this function returns, contains a pointer to the array of icon handles.</span></span>

</dd> <dt>

<span data-ttu-id="89c6b-126">_pIconId \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-126">_pIconId\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6b-127">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="89c6b-127">Type: \**UINT\** _</span></span>

<span data-ttu-id="89c6b-128">Cuando esta función vuelve, contiene un puntero al identificador de recurso del icono extraído que mejor se adapta al dispositivo de pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="89c6b-128">When this function returns, contains a pointer to the resource identifier of the extracted icon that best fits the current display device.</span></span> <span data-ttu-id="89c6b-129">Si no hay ningún identificador disponible para este formato, contiene 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="89c6b-129">If there is no identifier available for this format, it contains 0xFFFFFFFF.</span></span> <span data-ttu-id="89c6b-130">Si no se puede obtener ningún identificador por cualquier otro motivo, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="89c6b-130">If no identifier can be obtained for any other reason, returns zero.</span></span>

</dd> <dt>

<span data-ttu-id="89c6b-131">_nIcons \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-131">_nIcons\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6b-132">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="89c6b-132">Type: **UINT**</span></span>

<span data-ttu-id="89c6b-133">Número de iconos que se van a extraer del recurso denominado en *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="89c6b-133">The number of icons to extract from the resource named in *pszFileName*.</span></span> <span data-ttu-id="89c6b-134">Este parámetro solo es válido cuando el recurso es un archivo. exe o. dll.</span><span class="sxs-lookup"><span data-stu-id="89c6b-134">This parameter is valid only when the resource is a .exe or .dll file.</span></span>

</dd> <dt>

<span data-ttu-id="89c6b-135">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-135">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6b-136">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="89c6b-136">Type: **UINT**</span></span>

<span data-ttu-id="89c6b-137">Marcas que controlan esta función.</span><span class="sxs-lookup"><span data-stu-id="89c6b-137">The flags that control this function.</span></span> <span data-ttu-id="89c6b-138">Para ver los valores posibles, vea el parámetro *fuLoad* de la función [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) .</span><span class="sxs-lookup"><span data-stu-id="89c6b-138">For possible values, see the *fuLoad* parameter of the [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89c6b-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89c6b-139">Return value</span></span>

<span data-ttu-id="89c6b-140">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="89c6b-140">Type: **UINT**</span></span>

<span data-ttu-id="89c6b-141">Un valor distinto de cero si es correcto; de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="89c6b-141">A nonzero value if successful; otherwise, zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="89c6b-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89c6b-142">Remarks</span></span>

<span data-ttu-id="89c6b-143">**SHExtractIconsW** extrae de los siguientes tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="89c6b-143">**SHExtractIconsW** extracts from the following file types.</span></span>

-   <span data-ttu-id="89c6b-144">Ejecutable (.exe)</span><span class="sxs-lookup"><span data-stu-id="89c6b-144">Executable (.exe)</span></span>
-   <span data-ttu-id="89c6b-145">DLL (. dll)</span><span class="sxs-lookup"><span data-stu-id="89c6b-145">DLL (.dll)</span></span>
-   <span data-ttu-id="89c6b-146">Icono (. ico)</span><span class="sxs-lookup"><span data-stu-id="89c6b-146">Icon (.ico)</span></span>
-   <span data-ttu-id="89c6b-147">Cursor (. cur)</span><span class="sxs-lookup"><span data-stu-id="89c6b-147">Cursor (.cur)</span></span>
-   <span data-ttu-id="89c6b-148">Cursor animado (. ANI)</span><span class="sxs-lookup"><span data-stu-id="89c6b-148">Animated cursor (.ani)</span></span>
-   <span data-ttu-id="89c6b-149">Mapa de bits (.bmp)</span><span class="sxs-lookup"><span data-stu-id="89c6b-149">Bitmap (.bmp)</span></span>

<span data-ttu-id="89c6b-150">Extracciones de Windows 3. también se admiten archivos ejecutables *de 16 bits* (. exe o. dll).</span><span class="sxs-lookup"><span data-stu-id="89c6b-150">Extractions from Windows 3.*x* 16-bit executable files (.exe or .dll) are also supported.</span></span>

<span data-ttu-id="89c6b-151">Los parámetros *cxIcon* y *cyIcon* especifican el tamaño de los iconos que se van a extraer.</span><span class="sxs-lookup"><span data-stu-id="89c6b-151">The *cxIcon* and *cyIcon* parameters specify the size of the icons to extract.</span></span> <span data-ttu-id="89c6b-152">Se pueden extraer dos tamaños a través de cada parámetro dividiendo el valor entre su LOWORD y HIWORD.</span><span class="sxs-lookup"><span data-stu-id="89c6b-152">Two sizes can be extracted through each parameter by splitting the value between its LOWORD and HIWORD.</span></span> <span data-ttu-id="89c6b-153">Coloque el primer tamaño deseado en el LOWORD del parámetro y el segundo tamaño en el HIWORD.</span><span class="sxs-lookup"><span data-stu-id="89c6b-153">Put the first desired size in the LOWORD of the parameter and the second size in the HIWORD.</span></span> <span data-ttu-id="89c6b-154">Por ejemplo, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) para *cxIcon* y *cyIcon* extraen los iconos de tamaño 24 y 48.</span><span class="sxs-lookup"><span data-stu-id="89c6b-154">For example, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) for both *cxIcon* and *cyIcon* extracts both 24 and 48 sized icons.</span></span>

<span data-ttu-id="89c6b-155">El proceso de llamada es responsable de destruir todos los iconos extraídos mediante esta función llamando a la función [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) .</span><span class="sxs-lookup"><span data-stu-id="89c6b-155">The calling process is responsible for destroying all icons extracted through this function by calling the [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) function.</span></span>

<span data-ttu-id="89c6b-156">**SHExtractIconsW** no se exporta por nombre o se declara en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="89c6b-156">**SHExtractIconsW** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="89c6b-157">Para usarlo, debe declarar un prototipo coincidente y utilizar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para solicitar un puntero de función de Shell32.dll que se pueda usar para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="89c6b-157">To use it, you must declare a matching prototype and use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to request a function pointer from Shell32.dll that can be used to call this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c6b-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89c6b-158">Requirements</span></span>



| <span data-ttu-id="89c6b-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="89c6b-159">Requirement</span></span> | <span data-ttu-id="89c6b-160">Value</span><span class="sxs-lookup"><span data-stu-id="89c6b-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c6b-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89c6b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="89c6b-162">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89c6b-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89c6b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="89c6b-164">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="89c6b-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89c6b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89c6b-166"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="89c6b-166"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="89c6b-167">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="89c6b-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="89c6b-168">**SHExtractIconsW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="89c6b-168">**SHExtractIconsW** (Unicode)</span></span><br/>                                                                      |



 

 
