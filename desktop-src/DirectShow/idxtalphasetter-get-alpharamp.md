---
description: El \_ método get AlphaRamp recupera la propiedad de rampa alfa. La rampa alfa es el porcentaje por el que se ajustan los valores alfa de la imagen original. Por ejemplo, si la rampa alfa es 0,5, los valores alfa de la imagen se reducen al 50%.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'Método IDxtAlphaSetter:: get_AlphaRamp (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 335c227b0ac35ccd730d8ce7014b9a5c7ebc3213
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690251"
---
# <a name="idxtalphasetterget_alpharamp-method"></a><span data-ttu-id="ea365-105">IDxtAlphaSetter:: get \_ AlphaRamp (método)</span><span class="sxs-lookup"><span data-stu-id="ea365-105">IDxtAlphaSetter::get\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="ea365-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="ea365-106">\[Deprecated.</span></span> <span data-ttu-id="ea365-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ea365-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ea365-108">El `get_AlphaRamp` método recupera la propiedad de rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="ea365-108">The `get_AlphaRamp` method retrieves the alpha ramp property.</span></span> <span data-ttu-id="ea365-109">La rampa alfa es el porcentaje por el que se ajustan los valores alfa de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="ea365-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="ea365-110">Por ejemplo, si la rampa alfa es 0,5, los valores alfa de la imagen se reducen al 50%.</span><span class="sxs-lookup"><span data-stu-id="ea365-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea365-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea365-111">Syntax</span></span>


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="ea365-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea365-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea365-113">*pAlpha* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ea365-113">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ea365-114">Recibe la rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="ea365-114">Receives the alpha ramp.</span></span> <span data-ttu-id="ea365-115">Un valor negativo indica que no se ha establecido ninguna rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="ea365-115">A negative value indicates that no alpha ramp is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea365-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea365-116">Return value</span></span>

<span data-ttu-id="ea365-117">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ea365-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ea365-118">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="ea365-118">Possible values include the following.</span></span>



| <span data-ttu-id="ea365-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ea365-119">Return code</span></span>                                                                               | <span data-ttu-id="ea365-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea365-120">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="ea365-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="ea365-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="ea365-122">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="ea365-122">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="ea365-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ea365-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="ea365-124">Correcto</span><span class="sxs-lookup"><span data-stu-id="ea365-124">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="ea365-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea365-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea365-126">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="ea365-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ea365-127">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ea365-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ea365-128">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ea365-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea365-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea365-129">Requirements</span></span>



| <span data-ttu-id="ea365-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea365-130">Requirement</span></span> | <span data-ttu-id="ea365-131">Value</span><span class="sxs-lookup"><span data-stu-id="ea365-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea365-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea365-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ea365-133"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea365-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ea365-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea365-134">Library</span></span><br/> | <dl> <span data-ttu-id="ea365-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea365-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea365-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea365-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea365-137">**Interfaz IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="ea365-137">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




