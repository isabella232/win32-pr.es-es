---
description: El \_ método get similitud recupera el intervalo de datos de color que se vuelve transparente. En los valores más altos, una mayor variedad de colores similares es transparente. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB o DXTKEY \_ NONRED.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'Método IDxtKey:: get_Similarity (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e53898a1f9c5175fdf7a42ba6de68e3173f02afe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679417"
---
# <a name="idxtkeyget_similarity-method"></a><span data-ttu-id="d039a-105">IDxtKey:: get \_ similitud (método)</span><span class="sxs-lookup"><span data-stu-id="d039a-105">IDxtKey::get\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="d039a-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d039a-106">\[Deprecated.</span></span> <span data-ttu-id="d039a-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d039a-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d039a-108">El `get_Similarity` método recupera el intervalo de datos de color que se vuelve transparente.</span><span class="sxs-lookup"><span data-stu-id="d039a-108">The `get_Similarity` method retrieves the range of color data that becomes transparent.</span></span> <span data-ttu-id="d039a-109">En los valores más altos, una mayor variedad de colores similares es transparente.</span><span class="sxs-lookup"><span data-stu-id="d039a-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="d039a-110">Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB o DXTKEY \_ NONRED.</span><span class="sxs-lookup"><span data-stu-id="d039a-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="d039a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d039a-111">Syntax</span></span>


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d039a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d039a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d039a-113">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d039a-113">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d039a-114">Recibe el valor de similitud.</span><span class="sxs-lookup"><span data-stu-id="d039a-114">Receives the similarity value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d039a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d039a-115">Return value</span></span>

<span data-ttu-id="d039a-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d039a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d039a-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d039a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d039a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d039a-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d039a-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d039a-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d039a-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d039a-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d039a-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d039a-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d039a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d039a-122">Requirements</span></span>



| <span data-ttu-id="d039a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d039a-123">Requirement</span></span> | <span data-ttu-id="d039a-124">Value</span><span class="sxs-lookup"><span data-stu-id="d039a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d039a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d039a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d039a-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d039a-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d039a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d039a-127">Library</span></span><br/> | <dl> <span data-ttu-id="d039a-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d039a-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d039a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d039a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d039a-130">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="d039a-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="d039a-131">**IDxtKey:: get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="d039a-131">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




