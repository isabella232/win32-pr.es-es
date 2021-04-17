---
description: El \_ método put similitud especifica el intervalo de datos de color que se vuelve transparente. En los valores más altos, una mayor variedad de colores similares es transparente. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB o DXTKEY \_ NONRED.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: 'IDxtKey: método de ut_Similarity de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680495"
---
# <a name="idxtkeyput_similarity-method"></a><span data-ttu-id="4f863-105">IDxtKey: método de similitud de:p UT \_</span><span class="sxs-lookup"><span data-stu-id="4f863-105">IDxtKey::put\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="4f863-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4f863-106">\[Deprecated.</span></span> <span data-ttu-id="4f863-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4f863-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4f863-108">El `put_Similarity` método especifica el intervalo de datos de color que se vuelve transparente.</span><span class="sxs-lookup"><span data-stu-id="4f863-108">The `put_Similarity` method specifies the range of color data that becomes transparent.</span></span> <span data-ttu-id="4f863-109">En los valores más altos, una mayor variedad de colores similares es transparente.</span><span class="sxs-lookup"><span data-stu-id="4f863-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="4f863-110">Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB o DXTKEY \_ NONRED.</span><span class="sxs-lookup"><span data-stu-id="4f863-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f863-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f863-111">Syntax</span></span>


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="4f863-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f863-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f863-113">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f863-113">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f863-114">Especifica el valor de similitud.</span><span class="sxs-lookup"><span data-stu-id="4f863-114">Specifies the similarity value.</span></span> <span data-ttu-id="4f863-115">El intervalo válido es de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="4f863-115">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f863-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f863-116">Return value</span></span>

<span data-ttu-id="4f863-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4f863-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4f863-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f863-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f863-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f863-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f863-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4f863-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4f863-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f863-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4f863-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4f863-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f863-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f863-123">Requirements</span></span>



| <span data-ttu-id="4f863-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f863-124">Requirement</span></span> | <span data-ttu-id="4f863-125">Value</span><span class="sxs-lookup"><span data-stu-id="4f863-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f863-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f863-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4f863-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f863-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4f863-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f863-128">Library</span></span><br/> | <dl> <span data-ttu-id="4f863-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f863-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f863-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f863-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f863-131">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="4f863-131">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="4f863-132">**IDxtKey::p \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="4f863-132">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




