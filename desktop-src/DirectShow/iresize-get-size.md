---
description: El \_ método get size devuelve el tamaño de salida actual y el modo de ajuste.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'Método IResize:: get_Size (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681021"
---
# <a name="iresizeget_size-method"></a><span data-ttu-id="90155-103">IResize:: get \_ size (método)</span><span class="sxs-lookup"><span data-stu-id="90155-103">IResize::get\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="90155-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="90155-104">\[Deprecated.</span></span> <span data-ttu-id="90155-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="90155-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="90155-106">El `get_Size` método devuelve el tamaño de salida actual y el modo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="90155-106">The `get_Size` method returns the current output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="90155-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90155-107">Syntax</span></span>


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
);
```



## <a name="parameters"></a><span data-ttu-id="90155-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90155-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90155-109">*piHeight* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90155-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90155-110">Recibe el alto del vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="90155-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="90155-111">*piWidth* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90155-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90155-112">Recibe el ancho del vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="90155-112">Receives the video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="90155-113">*pFlag* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90155-113">*pFlag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90155-114">Recibe una marca que especifica el modo de Stretch.</span><span class="sxs-lookup"><span data-stu-id="90155-114">Receives a flag specifying the stretch mode.</span></span> <span data-ttu-id="90155-115">Vea [**cambiar el tamaño**](resize-flags.md) de las marcas para los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="90155-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90155-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90155-116">Return value</span></span>

<span data-ttu-id="90155-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="90155-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="90155-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="90155-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="90155-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90155-119">Remarks</span></span>

<span data-ttu-id="90155-120">Si no se ha establecido el tipo de salida, el filtro debe devolver los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="90155-120">If the output type has not been set, the filter should return default values.</span></span> <span data-ttu-id="90155-121">Estos valores se pueden elegir arbitrariamente en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="90155-121">These values can be arbitrarily chosen at design time.</span></span>

> [!Note]  
> <span data-ttu-id="90155-122">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="90155-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="90155-123">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="90155-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="90155-124">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="90155-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="90155-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90155-125">Requirements</span></span>



| <span data-ttu-id="90155-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="90155-126">Requirement</span></span> | <span data-ttu-id="90155-127">Value</span><span class="sxs-lookup"><span data-stu-id="90155-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90155-128">Versión</span><span class="sxs-lookup"><span data-stu-id="90155-128">Version</span></span><br/> | <span data-ttu-id="90155-129">DirectX 9,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="90155-129">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="90155-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90155-130">Header</span></span><br/>  | <dl> <span data-ttu-id="90155-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="90155-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="90155-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90155-132">Library</span></span><br/> | <dl> <span data-ttu-id="90155-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90155-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90155-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="90155-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90155-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="90155-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="90155-136">**Interfaz IResize**</span><span class="sxs-lookup"><span data-stu-id="90155-136">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




