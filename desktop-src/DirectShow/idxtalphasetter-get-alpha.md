---
description: El \_ método get Alpha recupera el valor alfa de toda la imagen.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'Método IDxtAlphaSetter:: get_Alpha (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690380"
---
# <a name="idxtalphasetterget_alpha-method"></a><span data-ttu-id="b478f-103">IDxtAlphaSetter:: get \_ Alpha (método)</span><span class="sxs-lookup"><span data-stu-id="b478f-103">IDxtAlphaSetter::get\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="b478f-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b478f-104">\[Deprecated.</span></span> <span data-ttu-id="b478f-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b478f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b478f-106">El `get_Alpha` método recupera el valor alfa de toda la imagen.</span><span class="sxs-lookup"><span data-stu-id="b478f-106">The `get_Alpha` method retrieves the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="b478f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b478f-107">Syntax</span></span>


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="b478f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b478f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b478f-109">*pAlpha* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b478f-109">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b478f-110">Recibe el valor alfa.</span><span class="sxs-lookup"><span data-stu-id="b478f-110">Receives the alpha value.</span></span> <span data-ttu-id="b478f-111">Este valor alfa se aplicará a toda la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="b478f-111">This alpha value will be applied to the entire target image.</span></span> <span data-ttu-id="b478f-112">Un valor negativo indica que no se ha establecido ningún valor alfa.</span><span class="sxs-lookup"><span data-stu-id="b478f-112">A negative value indicates that no alpha value is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b478f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b478f-113">Return value</span></span>

<span data-ttu-id="b478f-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b478f-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b478f-115">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="b478f-115">Possible values include the following.</span></span>



| <span data-ttu-id="b478f-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b478f-116">Return code</span></span>                                                                               | <span data-ttu-id="b478f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b478f-117">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="b478f-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b478f-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b478f-119">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="b478f-119">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="b478f-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b478f-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b478f-121">Correcto</span><span class="sxs-lookup"><span data-stu-id="b478f-121">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="b478f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b478f-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b478f-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b478f-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b478f-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b478f-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b478f-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b478f-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b478f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b478f-126">Requirements</span></span>



| <span data-ttu-id="b478f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b478f-127">Requirement</span></span> | <span data-ttu-id="b478f-128">Value</span><span class="sxs-lookup"><span data-stu-id="b478f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b478f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b478f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b478f-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b478f-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b478f-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b478f-131">Library</span></span><br/> | <dl> <span data-ttu-id="b478f-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b478f-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b478f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b478f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b478f-134">**Interfaz IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="b478f-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




