---
description: El \_ método get KeyType recupera el tipo de clave.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'Método IDxtKey:: get_KeyType (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679421"
---
# <a name="idxtkeyget_keytype-method"></a><span data-ttu-id="1cafa-103">IDxtKey:: get \_ KeyType (método)</span><span class="sxs-lookup"><span data-stu-id="1cafa-103">IDxtKey::get\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="1cafa-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="1cafa-104">\[Deprecated.</span></span> <span data-ttu-id="1cafa-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1cafa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1cafa-106">El `get_KeyType` método recupera el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="1cafa-106">The `get_KeyType` method retrieves the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cafa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cafa-107">Syntax</span></span>


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1cafa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cafa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cafa-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1cafa-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1cafa-110">Recibe uno de los siguientes valores de enumeración.</span><span class="sxs-lookup"><span data-stu-id="1cafa-110">Receives one of the following enumeration values.</span></span>



| <span data-ttu-id="1cafa-111">Value</span><span class="sxs-lookup"><span data-stu-id="1cafa-111">Value</span></span>             | <span data-ttu-id="1cafa-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cafa-112">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="1cafa-113">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="1cafa-113">DXTKEY\_RGB</span></span>       | <span data-ttu-id="1cafa-114">Clave cromada.</span><span class="sxs-lookup"><span data-stu-id="1cafa-114">Chroma key.</span></span> <span data-ttu-id="1cafa-115">(Clave en valor RGB).</span><span class="sxs-lookup"><span data-stu-id="1cafa-115">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="1cafa-116">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="1cafa-116">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="1cafa-117">Clave Nonred.</span><span class="sxs-lookup"><span data-stu-id="1cafa-117">Nonred key.</span></span> <span data-ttu-id="1cafa-118">(Hace que las áreas azules y verdes sean transparentes).</span><span class="sxs-lookup"><span data-stu-id="1cafa-118">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="1cafa-119">\_luminancia DXTKEY</span><span class="sxs-lookup"><span data-stu-id="1cafa-119">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="1cafa-120">Clave de luminancia.</span><span class="sxs-lookup"><span data-stu-id="1cafa-120">Luminance key.</span></span>                                        |
| <span data-ttu-id="1cafa-121">\_alfa DXTKEY</span><span class="sxs-lookup"><span data-stu-id="1cafa-121">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="1cafa-122">Clave por valor alfa.</span><span class="sxs-lookup"><span data-stu-id="1cafa-122">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="1cafa-123">\_matiz DXTKEY</span><span class="sxs-lookup"><span data-stu-id="1cafa-123">DXTKEY\_HUE</span></span>       | <span data-ttu-id="1cafa-124">Clave por matiz.</span><span class="sxs-lookup"><span data-stu-id="1cafa-124">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cafa-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cafa-125">Return value</span></span>

<span data-ttu-id="1cafa-126">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1cafa-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1cafa-127">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1cafa-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cafa-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cafa-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1cafa-129">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="1cafa-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1cafa-130">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1cafa-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1cafa-131">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1cafa-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1cafa-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cafa-132">Requirements</span></span>



| <span data-ttu-id="1cafa-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cafa-133">Requirement</span></span> | <span data-ttu-id="1cafa-134">Value</span><span class="sxs-lookup"><span data-stu-id="1cafa-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cafa-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cafa-135">Header</span></span><br/>  | <dl> <span data-ttu-id="1cafa-136"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cafa-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1cafa-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1cafa-137">Library</span></span><br/> | <dl> <span data-ttu-id="1cafa-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cafa-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cafa-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cafa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cafa-140">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="1cafa-140">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




