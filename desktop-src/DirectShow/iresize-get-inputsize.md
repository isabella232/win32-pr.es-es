---
description: El \_ método get Inlocate devuelve el tamaño de entrada actual del filtro de tamaño.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'Método IResize:: get_InputSize (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681023"
---
# <a name="iresizeget_inputsize-method"></a><span data-ttu-id="413a3-103">IResize:: get \_ Inlocate (método)</span><span class="sxs-lookup"><span data-stu-id="413a3-103">IResize::get\_InputSize method</span></span>

> [!Note]  
> <span data-ttu-id="413a3-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="413a3-104">\[Deprecated.</span></span> <span data-ttu-id="413a3-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="413a3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="413a3-106">El `get_InputSize` método devuelve el tamaño de entrada actual del filtro de tamaño.</span><span class="sxs-lookup"><span data-stu-id="413a3-106">The `get_InputSize` method returns the resizer filter's current input size.</span></span>

## <a name="syntax"></a><span data-ttu-id="413a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="413a3-107">Syntax</span></span>


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a><span data-ttu-id="413a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="413a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="413a3-109">*piHeight* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="413a3-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="413a3-110">Recibe el alto del vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="413a3-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="413a3-111">*piWidth* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="413a3-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="413a3-112">Recibe el ancho del vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="413a3-112">Receives the video width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="413a3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="413a3-113">Return value</span></span>

<span data-ttu-id="413a3-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="413a3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="413a3-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="413a3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="413a3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="413a3-116">Remarks</span></span>

<span data-ttu-id="413a3-117">Si el PIN de entrada del filtro no está conectado, devuelva un código de error.</span><span class="sxs-lookup"><span data-stu-id="413a3-117">If the filter's input pin is not connected, return an error code.</span></span> <span data-ttu-id="413a3-118">De lo contrario, devuelva el ancho y el alto del vídeo, según lo especificado por el tipo de medio del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="413a3-118">Otherwise, return the width and height of the video, as specified by the input pin's media type.</span></span>

> [!Note]  
> <span data-ttu-id="413a3-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="413a3-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="413a3-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="413a3-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="413a3-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="413a3-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="413a3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="413a3-122">Requirements</span></span>



| <span data-ttu-id="413a3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="413a3-123">Requirement</span></span> | <span data-ttu-id="413a3-124">Value</span><span class="sxs-lookup"><span data-stu-id="413a3-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="413a3-125">Versión</span><span class="sxs-lookup"><span data-stu-id="413a3-125">Version</span></span><br/> | <span data-ttu-id="413a3-126">DirectX 9,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="413a3-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="413a3-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="413a3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="413a3-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="413a3-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="413a3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="413a3-129">Library</span></span><br/> | <dl> <span data-ttu-id="413a3-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="413a3-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="413a3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="413a3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="413a3-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="413a3-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="413a3-133">**Interfaz IResize**</span><span class="sxs-lookup"><span data-stu-id="413a3-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




