---
description: El método FindMediaFile busca un archivo y, si se realiza correctamente, recupera la ruta de acceso al archivo.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'IMediaLocator:: FindMediaFile (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679068"
---
# <a name="imedialocatorfindmediafile-method"></a><span data-ttu-id="d29c4-103">IMediaLocator:: FindMediaFile (método)</span><span class="sxs-lookup"><span data-stu-id="d29c4-103">IMediaLocator::FindMediaFile method</span></span>

> [!Note]  
> <span data-ttu-id="d29c4-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d29c4-104">\[Deprecated.</span></span> <span data-ttu-id="d29c4-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d29c4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d29c4-106">El `FindMediaFile` método busca un archivo y, si se realiza correctamente, recupera la ruta de acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="d29c4-106">The `FindMediaFile` method searches for a file and, if successful, retrieves the path to the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d29c4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d29c4-107">Syntax</span></span>


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a><span data-ttu-id="d29c4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d29c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d29c4-109">*Entrada*</span><span class="sxs-lookup"><span data-stu-id="d29c4-109">*Input*</span></span> 
</dt> <dd>

<span data-ttu-id="d29c4-110">Nombre de archivo, incluida la ruta de acceso, donde se conocía por última vez el archivo.</span><span class="sxs-lookup"><span data-stu-id="d29c4-110">File name, including path, where the file was last known to reside.</span></span> <span data-ttu-id="d29c4-111">Para los objetos de origen de la escala de tiempo, use el nombre del medio actual.</span><span class="sxs-lookup"><span data-stu-id="d29c4-111">For source objects in the timeline, use the current media name.</span></span>

</dd> <dt>

<span data-ttu-id="d29c4-112">*FilterString*</span><span class="sxs-lookup"><span data-stu-id="d29c4-112">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="d29c4-113">**BSTR** que contiene pares de cadenas de filtro, con el formato que requiere el miembro **lpstrFilter** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="d29c4-113">A **BSTR** containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="d29c4-114">El localizador de medios usa este filtro si muestra un cuadro de diálogo Abrir archivo.</span><span class="sxs-lookup"><span data-stu-id="d29c4-114">The media locator uses this filter if it displays a File Open dialog box.</span></span> <span data-ttu-id="d29c4-115">El valor puede ser **null** si el parámetro *Flags* no incluye la \_ \_ marca emergente SFN VALIDATEF.</span><span class="sxs-lookup"><span data-stu-id="d29c4-115">The value can be **NULL** if the *Flags* parameter does not include the SFN\_VALIDATEF\_POPUP flag.</span></span>

</dd> <dt>

<span data-ttu-id="d29c4-116">*pOutput*</span><span class="sxs-lookup"><span data-stu-id="d29c4-116">*pOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="d29c4-117">Puntero a una variable que recibe la ruta de acceso real al archivo, si difiere del valor contenido en la *entrada* y si el método localiza correctamente el archivo.</span><span class="sxs-lookup"><span data-stu-id="d29c4-117">Pointer to a variable that receives the actual path to the file, if it differs from the value contained in *Input* and if the method successfully locates the file.</span></span>

</dd> <dt>

<span data-ttu-id="d29c4-118">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="d29c4-118">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="d29c4-119">Combinación bit a bit de cero o más marcadores.</span><span class="sxs-lookup"><span data-stu-id="d29c4-119">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="d29c4-120">Para obtener una lista de posibles marcas, vea [**marcas de validación de nombre de archivo**](file-name-validation-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d29c4-120">For a list of possible flags, see [**File Name Validation Flags**](file-name-validation-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d29c4-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d29c4-121">Return value</span></span>

<span data-ttu-id="d29c4-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d29c4-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d29c4-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d29c4-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d29c4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d29c4-124">Remarks</span></span>

<span data-ttu-id="d29c4-125">La cadena de filtro para el cuadro de diálogo Abrir archivo, que se especifica mediante el parámetro *FilterString* , contiene caracteres nulos internos.</span><span class="sxs-lookup"><span data-stu-id="d29c4-125">The filter string for the File Open dialog, which is specified by the *FilterString* parameter, contains internal Null characters.</span></span> <span data-ttu-id="d29c4-126">Por ejemplo, \\ el vídeo 0 \* . avi \\ 0 \\ 0 es una cadena de filtro válida.</span><span class="sxs-lookup"><span data-stu-id="d29c4-126">For example, Video\\0\*.avi\\0\\0 is a valid filter string.</span></span> <span data-ttu-id="d29c4-127">No se puede usar la función **SysAllocStr** para asignar el BSTR, porque esa función espera una cadena terminada en NULL y truncará la cadena en el primer carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="d29c4-127">You cannot use the **SysAllocStr** function to allocate the BSTR, because that function expects a Null-terminated string and will truncate the string at the first Null character.</span></span> <span data-ttu-id="d29c4-128">Por lo tanto, use una función como **SysAllocStringLen**, que incluye un parámetro explícito para la longitud:</span><span class="sxs-lookup"><span data-stu-id="d29c4-128">Therefore, use a function such as **SysAllocStringLen**, which includes an explicit parameter for the length:</span></span>


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



<span data-ttu-id="d29c4-129">Si el usuario cancela el cuadro de diálogo Abrir archivo, el método devuelve E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="d29c4-129">If the user cancels the File Open dialog, the method returns E\_FAIL.</span></span>

<span data-ttu-id="d29c4-130">El método asigna memoria para el **BSTR** en *pOutput*.</span><span class="sxs-lookup"><span data-stu-id="d29c4-130">The method allocates memory for the **BSTR** in *pOutput*.</span></span> <span data-ttu-id="d29c4-131">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="d29c4-131">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="d29c4-132">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d29c4-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d29c4-133">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d29c4-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d29c4-134">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d29c4-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d29c4-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d29c4-135">Requirements</span></span>



| <span data-ttu-id="d29c4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d29c4-136">Requirement</span></span> | <span data-ttu-id="d29c4-137">Value</span><span class="sxs-lookup"><span data-stu-id="d29c4-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d29c4-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d29c4-138">Header</span></span><br/>  | <dl> <span data-ttu-id="d29c4-139"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d29c4-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d29c4-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d29c4-140">Library</span></span><br/> | <dl> <span data-ttu-id="d29c4-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d29c4-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d29c4-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d29c4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d29c4-143">**Interfaz IMediaLocator**</span><span class="sxs-lookup"><span data-stu-id="d29c4-143">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="d29c4-144">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="d29c4-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
