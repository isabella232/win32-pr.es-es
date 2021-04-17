---
description: El método PrintXML convierte los datos de propiedad en una cadena XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: IPropertySetter::P método rintXML (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680494"
---
# <a name="ipropertysetterprintxml-method"></a><span data-ttu-id="e07f9-103">IPropertySetter::P método rintXML</span><span class="sxs-lookup"><span data-stu-id="e07f9-103">IPropertySetter::PrintXML method</span></span>

> [!Note]  
> <span data-ttu-id="e07f9-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e07f9-104">\[Deprecated.</span></span> <span data-ttu-id="e07f9-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e07f9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e07f9-106">El `PrintXML` método convierte los datos de propiedad en una cadena XML.</span><span class="sxs-lookup"><span data-stu-id="e07f9-106">The `PrintXML` method converts property data into an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e07f9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e07f9-107">Syntax</span></span>


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a><span data-ttu-id="e07f9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e07f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e07f9-109">*pszXML* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e07f9-109">*pszXML* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e07f9-110">Puntero a un búfer que recibe la cadena XML.</span><span class="sxs-lookup"><span data-stu-id="e07f9-110">Pointer to a buffer that receives the XML string.</span></span>

</dd> <dt>

<span data-ttu-id="e07f9-111">*cbXML* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e07f9-111">*cbXML* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07f9-112">Tamaño del búfer al que apunta *pszXML*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e07f9-112">Size of the buffer pointed to by *pszXML*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e07f9-113">*pcbPrinted* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e07f9-113">*pcbPrinted* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e07f9-114">Puntero a una variable que recibe la longitud de la cadena XML.</span><span class="sxs-lookup"><span data-stu-id="e07f9-114">Pointer to a variable that receives the length of the XML string.</span></span> <span data-ttu-id="e07f9-115">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="e07f9-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e07f9-116">*aplicar sangría* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e07f9-116">*indent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07f9-117">Número de niveles de sangría para la etiqueta más externa.</span><span class="sxs-lookup"><span data-stu-id="e07f9-117">Number of indent levels for the outermost tag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e07f9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e07f9-118">Return value</span></span>

<span data-ttu-id="e07f9-119">Devuelve S \_ correcto si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="e07f9-119">Returns S\_OK if successful.</span></span> <span data-ttu-id="e07f9-120">De lo contrario, devuelve un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="e07f9-120">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span> <span data-ttu-id="e07f9-121">Si la cadena XML es más larga que el búfer, el método devuelve E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e07f9-121">If the XML string is longer than the buffer, the method returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e07f9-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e07f9-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e07f9-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e07f9-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e07f9-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e07f9-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e07f9-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e07f9-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e07f9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e07f9-126">Requirements</span></span>



| <span data-ttu-id="e07f9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e07f9-127">Requirement</span></span> | <span data-ttu-id="e07f9-128">Value</span><span class="sxs-lookup"><span data-stu-id="e07f9-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e07f9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e07f9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e07f9-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e07f9-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e07f9-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e07f9-131">Library</span></span><br/> | <dl> <span data-ttu-id="e07f9-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e07f9-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e07f9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e07f9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07f9-134">**Interfaz IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="e07f9-134">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="e07f9-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e07f9-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




