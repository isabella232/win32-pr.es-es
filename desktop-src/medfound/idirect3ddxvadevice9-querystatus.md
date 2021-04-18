---
description: Consulta el estado de lectura y escritura de una superficie de descodificación de aceleración de vídeo de DirectX (DXVA).
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'IDirect3DDXVADevice9:: QueryStatus (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715441"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a><span data-ttu-id="0bb00-103">IDirect3DDXVADevice9:: QueryStatus (método)</span><span class="sxs-lookup"><span data-stu-id="0bb00-103">IDirect3DDXVADevice9::QueryStatus method</span></span>

<span data-ttu-id="0bb00-104">Consulta el estado de lectura y escritura de una superficie de descodificación de aceleración de vídeo de DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="0bb00-104">Queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb00-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bb00-105">Syntax</span></span>


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="0bb00-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bb00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb00-107">*pSurface*</span><span class="sxs-lookup"><span data-stu-id="0bb00-107">*pSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="0bb00-108">Puntero a la interfaz **IDirect3DSurface9** de la superficie que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="0bb00-108">Pointer to the **IDirect3DSurface9** interface of the surface to query.</span></span>

</dd> <dt>

<span data-ttu-id="0bb00-109">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="0bb00-109">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="0bb00-110">Especifica el tipo de consulta que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="0bb00-110">Specifies the type of query to perform.</span></span>



| <span data-ttu-id="0bb00-111">Value</span><span class="sxs-lookup"><span data-stu-id="0bb00-111">Value</span></span>                                                                                                                             | <span data-ttu-id="0bb00-112">Significado</span><span class="sxs-lookup"><span data-stu-id="0bb00-112">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <span data-ttu-id="0bb00-113"><dt>**0x00**</dt></span><span class="sxs-lookup"><span data-stu-id="0bb00-113"><dt>**0x00**</dt></span></span> </dl> | <span data-ttu-id="0bb00-114">Compruebe si la superficie es segura para su uso en la escritura.</span><span class="sxs-lookup"><span data-stu-id="0bb00-114">Test whether the surface is safe to use for writing.</span></span><br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <span data-ttu-id="0bb00-115"><dt>**0x01**</dt></span><span class="sxs-lookup"><span data-stu-id="0bb00-115"><dt>**0x01**</dt></span></span> </dl> | <span data-ttu-id="0bb00-116">Compruebe si la superficie se usa con seguridad para la lectura.</span><span class="sxs-lookup"><span data-stu-id="0bb00-116">Test whether the surface is safe to use for reading.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bb00-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0bb00-117">Return value</span></span>

<span data-ttu-id="0bb00-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0bb00-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0bb00-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0bb00-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb00-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bb00-120">Requirements</span></span>



| <span data-ttu-id="0bb00-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb00-121">Requirement</span></span> | <span data-ttu-id="0bb00-122">Value</span><span class="sxs-lookup"><span data-stu-id="0bb00-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0bb00-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bb00-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb00-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0bb00-124">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0bb00-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bb00-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb00-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0bb00-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0bb00-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bb00-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bb00-128"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bb00-128"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bb00-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bb00-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb00-130">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="0bb00-130">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




