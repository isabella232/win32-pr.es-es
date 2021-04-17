---
description: El método SaveToBlob guarda los datos de la propiedad en un formato de persistencia.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'IPropertySetter:: SaveToBlob (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680492"
---
# <a name="ipropertysettersavetoblob-method"></a><span data-ttu-id="e8fbe-103">IPropertySetter:: SaveToBlob (método)</span><span class="sxs-lookup"><span data-stu-id="e8fbe-103">IPropertySetter::SaveToBlob method</span></span>

> [!Note]  
> <span data-ttu-id="e8fbe-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-104">\[Deprecated.</span></span> <span data-ttu-id="e8fbe-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e8fbe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e8fbe-106">El `SaveToBlob` método guarda los datos de la propiedad en un formato de persistencia.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-106">The `SaveToBlob` method saves the property data to a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8fbe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8fbe-107">Syntax</span></span>


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a><span data-ttu-id="e8fbe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8fbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8fbe-109">*pcSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e8fbe-109">*pcSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8fbe-110">Recibe el tamaño de los datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-110">Receives the size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e8fbe-111">*ppb* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e8fbe-111">*ppb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8fbe-112">Recibe un puntero a una matriz de bytes que recibe los datos.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-112">Receives a pointer to an array of bytes that receives the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8fbe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8fbe-113">Return value</span></span>

<span data-ttu-id="e8fbe-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e8fbe-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e8fbe-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8fbe-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8fbe-116">Remarks</span></span>

<span data-ttu-id="e8fbe-117">El método asigna memoria para la matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-117">The method allocates memory for the byte array.</span></span> <span data-ttu-id="e8fbe-118">El autor de la llamada debe liberarlo mediante la función **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="e8fbe-118">The caller must free it, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="e8fbe-119">Todos los valores y nombres de propiedad se truncan hasta 40 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-119">All property names and values are truncated to 40 characters in length.</span></span> <span data-ttu-id="e8fbe-120">Por esta razón, XML es el formato de persistencia preferido.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-120">For this reason, XML is the preferred persistence format.</span></span> <span data-ttu-id="e8fbe-121">Consulte la [**interfaz IXml2Dex**](ixml2dex.md).</span><span class="sxs-lookup"><span data-stu-id="e8fbe-121">See [**IXml2Dex Interface**](ixml2dex.md).</span></span>

> [!Note]  
> <span data-ttu-id="e8fbe-122">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e8fbe-123">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8fbe-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e8fbe-124">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8fbe-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8fbe-125">Requirements</span></span>



| <span data-ttu-id="e8fbe-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8fbe-126">Requirement</span></span> | <span data-ttu-id="e8fbe-127">Value</span><span class="sxs-lookup"><span data-stu-id="e8fbe-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fbe-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8fbe-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e8fbe-129"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8fbe-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e8fbe-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8fbe-130">Library</span></span><br/> | <dl> <span data-ttu-id="e8fbe-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8fbe-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8fbe-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8fbe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8fbe-133">**Interfaz IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="e8fbe-133">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="e8fbe-134">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e8fbe-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




