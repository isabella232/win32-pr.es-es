---
description: El método ValidateSourceNames valida los nombres de origen en la escala de tiempo mediante el localizador de medios. Opcionalmente, este método también actualiza cualquier objeto de origen para el que encuentra un archivo.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'IAMTimeline:: ValidateSourceNames (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690615"
---
# <a name="iamtimelinevalidatesourcenames-method"></a><span data-ttu-id="434a8-104">IAMTimeline:: ValidateSourceNames (método)</span><span class="sxs-lookup"><span data-stu-id="434a8-104">IAMTimeline::ValidateSourceNames method</span></span>

> [!Note]  
> <span data-ttu-id="434a8-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="434a8-105">\[Deprecated.</span></span> <span data-ttu-id="434a8-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="434a8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="434a8-107">El `ValidateSourceNames` método valida los nombres de origen en la escala de tiempo mediante el localizador de medios.</span><span class="sxs-lookup"><span data-stu-id="434a8-107">The `ValidateSourceNames` method validates source names in the timeline, using the media locator.</span></span> <span data-ttu-id="434a8-108">Opcionalmente, este método también actualiza cualquier objeto de origen para el que encuentra un archivo.</span><span class="sxs-lookup"><span data-stu-id="434a8-108">Optionally, this method also updates any source object for which it locates a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="434a8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="434a8-109">Syntax</span></span>


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a><span data-ttu-id="434a8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="434a8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434a8-111">*ValidateFlags*</span><span class="sxs-lookup"><span data-stu-id="434a8-111">*ValidateFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="434a8-112">Combinación bit a bit de las [**marcas de validación de nombre de archivo**](file-name-validation-flags.md) que especifican el comportamiento del localizador de medios.</span><span class="sxs-lookup"><span data-stu-id="434a8-112">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="434a8-113">\_ \_ Deben estar presentes las marcas de comprobación SFN VALIDATEF Replace y SFN \_ VALIDATEF \_ , o bien el método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="434a8-113">The SFN\_VALIDATEF\_REPLACE and SFN\_VALIDATEF\_CHECK flags must be present, or the method returns E\_INVALIDARG.</span></span>

</dd> <dt>

<span data-ttu-id="434a8-114">*pOverride*</span><span class="sxs-lookup"><span data-stu-id="434a8-114">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="434a8-115">Puntero opcional a la interfaz [**IMediaLocator**](imedialocator.md) de un localizador de medios que se va a usar en lugar del valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="434a8-115">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="434a8-116">Para usar el localizador de medios predeterminado, establezca el valor de este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="434a8-116">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="434a8-117">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="434a8-117">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="434a8-118">*NotifyEventHandle*</span><span class="sxs-lookup"><span data-stu-id="434a8-118">*NotifyEventHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="434a8-119">Identificador para un evento.</span><span class="sxs-lookup"><span data-stu-id="434a8-119">Handle to an event.</span></span> <span data-ttu-id="434a8-120">El método señala el evento una vez finalizada la validación.</span><span class="sxs-lookup"><span data-stu-id="434a8-120">The method signals the event after it has completed the validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="434a8-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="434a8-121">Return value</span></span>

<span data-ttu-id="434a8-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="434a8-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="434a8-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="434a8-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="434a8-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="434a8-124">Remarks</span></span>

<span data-ttu-id="434a8-125">Con el parámetro *pOverride* , puede proporcionar su propia implementación personalizada de la interfaz [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="434a8-125">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="434a8-126">Por ejemplo, el localizador de medios predeterminado no enviará una notificación a la aplicación sobre los archivos que encuentre (o no puede encontrar).</span><span class="sxs-lookup"><span data-stu-id="434a8-126">For example, the default media locator will not notify your application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="434a8-127">Para superar esta limitación, puede implementar un localizador de medios personalizado, convirtiéndolo en un contenedor para la versión predeterminada.</span><span class="sxs-lookup"><span data-stu-id="434a8-127">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="434a8-128">En la versión personalizada, pase [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) llamadas directamente a la versión predeterminada y examine el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="434a8-128">In your custom version, pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version, and examine the return value.</span></span>

> [!Note]  
> <span data-ttu-id="434a8-129">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="434a8-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="434a8-130">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="434a8-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="434a8-131">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="434a8-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="434a8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="434a8-132">Requirements</span></span>



| <span data-ttu-id="434a8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="434a8-133">Requirement</span></span> | <span data-ttu-id="434a8-134">Value</span><span class="sxs-lookup"><span data-stu-id="434a8-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="434a8-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="434a8-135">Header</span></span><br/>  | <dl> <span data-ttu-id="434a8-136"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="434a8-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="434a8-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="434a8-137">Library</span></span><br/> | <dl> <span data-ttu-id="434a8-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="434a8-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="434a8-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="434a8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434a8-140">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="434a8-140">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="434a8-141">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="434a8-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




