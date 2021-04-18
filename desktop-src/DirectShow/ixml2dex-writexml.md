---
description: El método WriteXML convierte una escala de tiempo en una cadena XML.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'IXml2Dex:: WriteXML (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ab8a4421244f2c2ee21c5243923f5d0827317e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679065"
---
# <a name="ixml2dexwritexml-method"></a><span data-ttu-id="5faae-103">IXml2Dex:: WriteXML (método)</span><span class="sxs-lookup"><span data-stu-id="5faae-103">IXml2Dex::WriteXML method</span></span>

> [!Note]  
> <span data-ttu-id="5faae-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="5faae-104">\[Deprecated.</span></span> <span data-ttu-id="5faae-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5faae-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5faae-106">El `WriteXML` método convierte una escala de tiempo en una cadena XML.</span><span class="sxs-lookup"><span data-stu-id="5faae-106">The `WriteXML` method translates a timeline to an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5faae-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5faae-107">Syntax</span></span>


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a><span data-ttu-id="5faae-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5faae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5faae-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="5faae-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="5faae-110">Puntero a la interfaz **IUnknown** del objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="5faae-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="5faae-111">*pbstrXML*</span><span class="sxs-lookup"><span data-stu-id="5faae-111">*pbstrXML*</span></span> 
</dt> <dd>

<span data-ttu-id="5faae-112">Puntero a una variable de tipo BSTR que recibe la cadena XML que describe la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5faae-112">Pointer to a variable of type BSTR that receives the XML string describing the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5faae-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5faae-113">Return value</span></span>

<span data-ttu-id="5faae-114">Devuelve S \_ correcto si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="5faae-114">Returns S\_OK if successful.</span></span> <span data-ttu-id="5faae-115">Si no hay memoria suficiente para la conversión, devuelve E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5faae-115">If there is insufficient memory for the conversion, returns E\_OUTOFMEMORY.</span></span> <span data-ttu-id="5faae-116">De lo contrario, devuelve otro código de error.</span><span class="sxs-lookup"><span data-stu-id="5faae-116">Otherwise, returns another error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5faae-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5faae-117">Remarks</span></span>

<span data-ttu-id="5faae-118">El método asigna memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="5faae-118">The method allocates memory for the string.</span></span> <span data-ttu-id="5faae-119">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="5faae-119">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="5faae-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="5faae-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5faae-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5faae-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5faae-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5faae-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5faae-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5faae-123">Requirements</span></span>



| <span data-ttu-id="5faae-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5faae-124">Requirement</span></span> | <span data-ttu-id="5faae-125">Value</span><span class="sxs-lookup"><span data-stu-id="5faae-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5faae-126">Versión</span><span class="sxs-lookup"><span data-stu-id="5faae-126">Version</span></span><br/> | <span data-ttu-id="5faae-127">Internet Explorer 4,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5faae-127">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="5faae-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5faae-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5faae-129"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="5faae-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5faae-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5faae-130">Library</span></span><br/> | <dl> <span data-ttu-id="5faae-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5faae-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5faae-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="5faae-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5faae-133">**Interfaz IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="5faae-133">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="5faae-134">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="5faae-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




