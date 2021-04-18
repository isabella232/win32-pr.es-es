---
description: El método SetSourceNameValidation especifica cómo valida el motor de representación los nombres de archivo.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'IRenderEngine:: SetSourceNameValidation (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680709"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a><span data-ttu-id="16003-103">IRenderEngine:: SetSourceNameValidation (método)</span><span class="sxs-lookup"><span data-stu-id="16003-103">IRenderEngine::SetSourceNameValidation method</span></span>

> [!Note]  
> <span data-ttu-id="16003-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="16003-104">\[Deprecated.</span></span> <span data-ttu-id="16003-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="16003-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="16003-106">El `SetSourceNameValidation` método especifica cómo valida el motor de representación los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="16003-106">The `SetSourceNameValidation` method specifies how the render engine validates file names.</span></span>

## <a name="syntax"></a><span data-ttu-id="16003-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16003-107">Syntax</span></span>


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a><span data-ttu-id="16003-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16003-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16003-109">*FilterString*</span><span class="sxs-lookup"><span data-stu-id="16003-109">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="16003-110">Valor **BSTR** que contiene pares de cadenas de filtro, con el formato que requiere el miembro **lpstrFilter** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="16003-110">**BSTR** value containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="16003-111">El localizador de medios usa este filtro si presenta un cuadro de diálogo Abrir archivo al usuario final.</span><span class="sxs-lookup"><span data-stu-id="16003-111">The media locator uses this filter if it presents an Open File dialog box to the end user.</span></span>

</dd> <dt>

<span data-ttu-id="16003-112">*pOverride*</span><span class="sxs-lookup"><span data-stu-id="16003-112">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="16003-113">Puntero opcional a la interfaz [**IMediaLocator**](imedialocator.md) de un localizador de medios que se va a usar en lugar del valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="16003-113">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="16003-114">Para usar el localizador de medios predeterminado, establezca el valor de este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="16003-114">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="16003-115">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="16003-115">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="16003-116">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="16003-116">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="16003-117">Combinación bit a bit de las [**marcas de validación de nombre de archivo**](file-name-validation-flags.md) que especifican el comportamiento del localizador de medios.</span><span class="sxs-lookup"><span data-stu-id="16003-117">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="16003-118">La marca de comprobación de SFN \_ VALIDATEF \_ debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="16003-118">The SFN\_VALIDATEF\_CHECK flag must be present.</span></span> <span data-ttu-id="16003-119">La \_ \_ marca HLINKMUTED VALIDATEF SFN no tiene ningún efecto en este método.</span><span class="sxs-lookup"><span data-stu-id="16003-119">The SFN\_VALIDATEF\_hlinkMUTED flag has no effect with this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16003-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16003-120">Return value</span></span>

<span data-ttu-id="16003-121">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="16003-121">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="16003-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="16003-122">Return code</span></span>                                                                                            | <span data-ttu-id="16003-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="16003-123">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="16003-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="16003-124"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="16003-125">Correcto.</span><span class="sxs-lookup"><span data-stu-id="16003-125">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="16003-126"><dt>**E \_ debe \_ inicializar el \_ representador**</dt></span><span class="sxs-lookup"><span data-stu-id="16003-126"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="16003-127">No se pudo inicializar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="16003-127">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16003-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16003-128">Remarks</span></span>

<span data-ttu-id="16003-129">Con el parámetro *pOverride* , puede proporcionar su propia implementación personalizada de la interfaz [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="16003-129">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="16003-130">Por ejemplo, el localizador de medios predeterminado no notifica a una aplicación los archivos que encuentra (o no puede encontrar).</span><span class="sxs-lookup"><span data-stu-id="16003-130">For example, the default media locator does not notify an application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="16003-131">Para superar esta limitación, puede implementar un localizador de medios personalizado, convirtiéndolo en un contenedor para la versión predeterminada.</span><span class="sxs-lookup"><span data-stu-id="16003-131">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="16003-132">Después, pase las llamadas a [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) directamente a la versión predeterminada y examine el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="16003-132">Then pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version and examine the return value.</span></span>

<span data-ttu-id="16003-133">Actualmente, este método no valida los orígenes cargados dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="16003-133">Currently, this method does not validate dynamically loaded sources.</span></span> <span data-ttu-id="16003-134">Vea [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="16003-134">See [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="16003-135">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="16003-135">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="16003-136">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="16003-136">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="16003-137">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="16003-137">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16003-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16003-138">Requirements</span></span>



| <span data-ttu-id="16003-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="16003-139">Requirement</span></span> | <span data-ttu-id="16003-140">Value</span><span class="sxs-lookup"><span data-stu-id="16003-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16003-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16003-141">Header</span></span><br/>  | <dl> <span data-ttu-id="16003-142"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="16003-142"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="16003-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16003-143">Library</span></span><br/> | <dl> <span data-ttu-id="16003-144"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16003-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16003-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="16003-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16003-146">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="16003-146">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="16003-147">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="16003-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
