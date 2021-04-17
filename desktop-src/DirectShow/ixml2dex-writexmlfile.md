---
description: El método WriteXMLFile traduce una escala de tiempo a XML y escribe los datos XML en un archivo.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'IXml2Dex:: WriteXMLFile (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690909"
---
# <a name="ixml2dexwritexmlfile-method"></a><span data-ttu-id="81853-103">IXml2Dex:: WriteXMLFile (método)</span><span class="sxs-lookup"><span data-stu-id="81853-103">IXml2Dex::WriteXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="81853-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="81853-104">\[Deprecated.</span></span> <span data-ttu-id="81853-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="81853-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="81853-106">El `WriteXMLFile` método traduce una escala de tiempo a XML y escribe los datos XML en un archivo.</span><span class="sxs-lookup"><span data-stu-id="81853-106">The `WriteXMLFile` method translates a timeline to XML and writes the XML data to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="81853-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81853-107">Syntax</span></span>


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="81853-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81853-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81853-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="81853-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="81853-110">Puntero a la interfaz **IUnknown** del objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="81853-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="81853-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="81853-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="81853-112">Cadena que especifica el nombre del archivo que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="81853-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81853-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81853-113">Return value</span></span>

<span data-ttu-id="81853-114">Devuelve un valor **HRESULT** que depende de la implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="81853-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="81853-115">**HRESULT** puede incluir una de las siguientes constantes estándar u otros valores que no se muestran en la lista.</span><span class="sxs-lookup"><span data-stu-id="81853-115">The **HRESULT** can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="81853-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="81853-116">Return code</span></span>                                                                                   | <span data-ttu-id="81853-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="81853-117">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="81853-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="81853-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="81853-119">El argumento no es válido.</span><span class="sxs-lookup"><span data-stu-id="81853-119">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="81853-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="81853-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="81853-121">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="81853-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="81853-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="81853-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="81853-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="81853-123">Success.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="81853-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81853-124">Remarks</span></span>

<span data-ttu-id="81853-125">Este método genera un archivo XML que representa todos los componentes de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="81853-125">This method generates an XML file that represents all the components in the timeline.</span></span>

> [!Note]  
> <span data-ttu-id="81853-126">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="81853-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="81853-127">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="81853-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="81853-128">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="81853-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81853-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81853-129">Requirements</span></span>



| <span data-ttu-id="81853-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="81853-130">Requirement</span></span> | <span data-ttu-id="81853-131">Value</span><span class="sxs-lookup"><span data-stu-id="81853-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81853-132">Versión</span><span class="sxs-lookup"><span data-stu-id="81853-132">Version</span></span><br/> | <span data-ttu-id="81853-133">Internet Explorer 4,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="81853-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="81853-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81853-134">Header</span></span><br/>  | <dl> <span data-ttu-id="81853-135"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="81853-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="81853-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81853-136">Library</span></span><br/> | <dl> <span data-ttu-id="81853-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81853-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81853-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="81853-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81853-139">**Interfaz IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="81853-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="81853-140">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="81853-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




