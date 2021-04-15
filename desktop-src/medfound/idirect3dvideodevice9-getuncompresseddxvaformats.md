---
description: Obtiene una lista de formatos de píxeles sin comprimir que se pueden representar con un perfil de aceleración de vídeo de DirectX (DXVA) especificado.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'IDirect3DVideoDevice9:: GetUncompressedDXVAFormats (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360614"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a><span data-ttu-id="f2271-103">IDirect3DVideoDevice9:: GetUncompressedDXVAFormats (método)</span><span class="sxs-lookup"><span data-stu-id="f2271-103">IDirect3DVideoDevice9::GetUncompressedDXVAFormats method</span></span>

<span data-ttu-id="f2271-104">Obtiene una lista de formatos de píxeles sin comprimir que se pueden representar con un perfil de aceleración de vídeo de DirectX (DXVA) especificado.</span><span class="sxs-lookup"><span data-stu-id="f2271-104">Gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2271-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2271-105">Syntax</span></span>


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a><span data-ttu-id="f2271-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2271-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2271-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="f2271-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="f2271-108">Puntero a un GUID que especifica el perfil de DXVA.</span><span class="sxs-lookup"><span data-stu-id="f2271-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="f2271-109">Para obtener una lista de los perfiles compatibles, llame a [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="f2271-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2271-110">*pNumFormats*</span><span class="sxs-lookup"><span data-stu-id="f2271-110">*pNumFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="f2271-111">En la entrada, especifica el número de elementos de la matriz *pFormats* .</span><span class="sxs-lookup"><span data-stu-id="f2271-111">On input, specifies the number of elements in the *pFormats* array.</span></span> <span data-ttu-id="f2271-112">Si *pFormats* es **null**, el valor de `*pNumFormats` debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f2271-112">If *pFormats* is **NULL**, the value of `*pNumFormats` must be zero.</span></span>

<span data-ttu-id="f2271-113">En la salida, si *pFormats* es **null**, *pNumFormats* recibe el número de formatos de píxel admitidos.</span><span class="sxs-lookup"><span data-stu-id="f2271-113">On output, if *pFormats* is **NULL**, *pNumFormats* receives the number of supported pixel formats.</span></span> <span data-ttu-id="f2271-114">De lo contrario, *pNumFormats* recibe el número real de formatos de píxel copiados en la matriz *pFormats* .</span><span class="sxs-lookup"><span data-stu-id="f2271-114">Otherwise, *pNumFormats* receives the actual number of pixel formats copied to the *pFormats* array.</span></span>

</dd> <dt>

<span data-ttu-id="f2271-115">*pFormats*</span><span class="sxs-lookup"><span data-stu-id="f2271-115">*pFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="f2271-116">Dirección de una matriz de valores **D3DFORMAT** o **null**.</span><span class="sxs-lookup"><span data-stu-id="f2271-116">Address of an array of **D3DFORMAT** values, or **NULL**.</span></span> <span data-ttu-id="f2271-117">Si el valor no es **null**, la matriz recibe una lista de formatos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="f2271-117">If the value is non-**NULL**, the array receives a list of pixel formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2271-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2271-118">Return value</span></span>

<span data-ttu-id="f2271-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f2271-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f2271-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2271-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2271-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2271-121">Remarks</span></span>

<span data-ttu-id="f2271-122">Llame a este método dos veces.</span><span class="sxs-lookup"><span data-stu-id="f2271-122">Call this method twice.</span></span> <span data-ttu-id="f2271-123">En la primera llamada, establezca *pFormats* en **null**.</span><span class="sxs-lookup"><span data-stu-id="f2271-123">On the first call, set *pFormats* to **NULL**.</span></span> <span data-ttu-id="f2271-124">El parámetro *pNumFormats* recibe el número de formatos.</span><span class="sxs-lookup"><span data-stu-id="f2271-124">The *pNumFormats* parameter receives the number of formats.</span></span> <span data-ttu-id="f2271-125">Asigne una matriz **D3DFORMAT** con el tamaño necesario y vuelva a llamar al método.</span><span class="sxs-lookup"><span data-stu-id="f2271-125">Allocate a **D3DFORMAT** array with the required size, and call the method again.</span></span> <span data-ttu-id="f2271-126">Esta vez, establezca *pFormats* en la dirección de la matriz.</span><span class="sxs-lookup"><span data-stu-id="f2271-126">This time, set *pFormats* to the address of the array.</span></span> <span data-ttu-id="f2271-127">El método rellena la matriz con la lista de formatos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="f2271-127">The method fills the array with the list of pixel formats.</span></span>

<span data-ttu-id="f2271-128">El controlador debe devolver los formatos en orden decreciente de preferencia, con el formato más preferido indicado en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="f2271-128">The driver should return the formats in decreasing order of preference, with the most preferred format listed first.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2271-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2271-129">Requirements</span></span>



| <span data-ttu-id="f2271-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2271-130">Requirement</span></span> | <span data-ttu-id="f2271-131">Value</span><span class="sxs-lookup"><span data-stu-id="f2271-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f2271-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2271-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f2271-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f2271-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2271-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2271-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f2271-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2271-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f2271-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2271-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2271-137"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2271-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2271-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2271-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2271-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="f2271-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




