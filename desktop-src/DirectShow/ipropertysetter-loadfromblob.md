---
description: El método LoadFromBlob carga los datos de propiedad desde un formato de persistencia.
ms.assetid: b314a844-2190-469a-a030-4494e2140ce6
title: 'IPropertySetter:: LoadFromBlob (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadFromBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a1e58aa5802e8fcb05c2464fc1f121ee1e86f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679118"
---
# <a name="ipropertysetterloadfromblob-method"></a><span data-ttu-id="63bc5-103">IPropertySetter:: LoadFromBlob (método)</span><span class="sxs-lookup"><span data-stu-id="63bc5-103">IPropertySetter::LoadFromBlob method</span></span>

> [!Note]  
> <span data-ttu-id="63bc5-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="63bc5-104">\[Deprecated.</span></span> <span data-ttu-id="63bc5-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="63bc5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="63bc5-106">El `LoadFromBlob` método carga los datos de propiedad desde un formato de persistencia.</span><span class="sxs-lookup"><span data-stu-id="63bc5-106">The `LoadFromBlob` method loads property data from a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="63bc5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63bc5-107">Syntax</span></span>


```C++
HRESULT LoadFromBlob(
  [in] LONG cSize,
  [in] BYTE *pb
);
```



## <a name="parameters"></a><span data-ttu-id="63bc5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63bc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63bc5-109">*cSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63bc5-109">*cSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63bc5-110">Tamaño de los datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="63bc5-110">Size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="63bc5-111">*PB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63bc5-111">*pb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63bc5-112">Puntero a una matriz de bytes que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="63bc5-112">Pointer to an array of bytes that contains the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63bc5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63bc5-113">Return value</span></span>

<span data-ttu-id="63bc5-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="63bc5-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63bc5-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63bc5-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="63bc5-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63bc5-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="63bc5-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="63bc5-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="63bc5-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="63bc5-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="63bc5-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="63bc5-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63bc5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63bc5-120">Requirements</span></span>



| <span data-ttu-id="63bc5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="63bc5-121">Requirement</span></span> | <span data-ttu-id="63bc5-122">Value</span><span class="sxs-lookup"><span data-stu-id="63bc5-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63bc5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63bc5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="63bc5-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="63bc5-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="63bc5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63bc5-125">Library</span></span><br/> | <dl> <span data-ttu-id="63bc5-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63bc5-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63bc5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="63bc5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63bc5-128">**Interfaz IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="63bc5-128">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="63bc5-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="63bc5-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




