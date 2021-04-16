---
description: El método WriteGrfFile escribe un gráfico de filtro en un archivo en formato. GRF.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'IXml2Dex:: WriteGrfFile (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690461"
---
# <a name="ixml2dexwritegrffile-method"></a><span data-ttu-id="9e9a0-103">IXml2Dex:: WriteGrfFile (método)</span><span class="sxs-lookup"><span data-stu-id="9e9a0-103">IXml2Dex::WriteGrfFile method</span></span>

> [!Note]  
> <span data-ttu-id="9e9a0-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-104">\[Deprecated.</span></span> <span data-ttu-id="9e9a0-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9e9a0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9e9a0-106">El `WriteGrfFile` método escribe un gráfico de filtro en un archivo en formato. GRF.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-106">The `WriteGrfFile` method writes a filter graph to a file in .grf format.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e9a0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e9a0-107">Syntax</span></span>


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="9e9a0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e9a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e9a0-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="9e9a0-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="9e9a0-110">Puntero a la interfaz **IUnknown** del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-110">Pointer to the filter graph's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="9e9a0-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="9e9a0-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="9e9a0-112">Cadena que especifica el nombre del archivo que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e9a0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e9a0-113">Return value</span></span>

<span data-ttu-id="9e9a0-114">Devuelve un valor **HRESULT** que depende de la implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="9e9a0-115">HRESULT puede incluir una de las siguientes constantes estándar u otros valores que no se muestran en la lista.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-115">HRESULT can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="9e9a0-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9e9a0-116">Return code</span></span>                                                                                  | <span data-ttu-id="9e9a0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e9a0-117">Description</span></span>                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="9e9a0-118"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="9e9a0-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="9e9a0-119">Error.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-119">Failure.</span></span><br/>             |
| <dl> <span data-ttu-id="9e9a0-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9e9a0-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9e9a0-121">El argumento no es válido.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-121">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="9e9a0-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9e9a0-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9e9a0-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-123">Success.</span></span><br/>             |



 

<span data-ttu-id="9e9a0-124">Este método también puede devolver códigos de error generados por llamadas internas a los métodos **IStorage:: CreateStream (** y **IPersist:: Save** .</span><span class="sxs-lookup"><span data-stu-id="9e9a0-124">This method can also return error codes generated by internal calls to the **IStorage::CreateStream** and **IPersist::Save** methods.</span></span> <span data-ttu-id="9e9a0-125">Para obtener más información, vea el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-125">For more information, see the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e9a0-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e9a0-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9e9a0-127">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9e9a0-128">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e9a0-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9e9a0-129">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e9a0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e9a0-130">Requirements</span></span>



| <span data-ttu-id="9e9a0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e9a0-131">Requirement</span></span> | <span data-ttu-id="9e9a0-132">Value</span><span class="sxs-lookup"><span data-stu-id="9e9a0-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9a0-133">Versión</span><span class="sxs-lookup"><span data-stu-id="9e9a0-133">Version</span></span><br/> | <span data-ttu-id="9e9a0-134">Internet Explorer 4,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="9e9a0-134">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="9e9a0-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e9a0-135">Header</span></span><br/>  | <dl> <span data-ttu-id="9e9a0-136"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e9a0-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9e9a0-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e9a0-137">Library</span></span><br/> | <dl> <span data-ttu-id="9e9a0-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e9a0-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e9a0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e9a0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9a0-140">**Interfaz IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="9e9a0-140">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="9e9a0-141">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="9e9a0-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




