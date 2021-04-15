---
description: Obtiene una lista de perfiles de aceleración de vídeo de DirectX (DXVA) admitidos por el controlador de pantalla.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'IDirect3DVideoDevice9:: GetDXVAGuids (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715884"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a><span data-ttu-id="b930c-103">IDirect3DVideoDevice9:: GetDXVAGuids (método)</span><span class="sxs-lookup"><span data-stu-id="b930c-103">IDirect3DVideoDevice9::GetDXVAGuids method</span></span>

<span data-ttu-id="b930c-104">Obtiene una lista de perfiles de aceleración de vídeo de DirectX (DXVA) admitidos por el controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="b930c-104">Gets a list of DirectX Video Acceleration (DXVA) profiles that are supported by the display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="b930c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b930c-105">Syntax</span></span>


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a><span data-ttu-id="b930c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b930c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b930c-107">*pNumGuids*</span><span class="sxs-lookup"><span data-stu-id="b930c-107">*pNumGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="b930c-108">En la entrada, especifica el número de elementos de la matriz *pGuids* .</span><span class="sxs-lookup"><span data-stu-id="b930c-108">On input, specifies the number of elements in the *pGuids* array.</span></span> <span data-ttu-id="b930c-109">Si *pGuids* es **null**, el valor de `*pNumGuids` debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b930c-109">If *pGuids* is **NULL**, the value of `*pNumGuids` must be zero.</span></span>

<span data-ttu-id="b930c-110">En la salida, si *pGuids* es **null**, *pNumGuids* recibe el número de perfiles de DXVA en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="b930c-110">On output, if *pGuids* is **NULL**, *pNumGuids* receives the number of restricted-mode DXVA profiles.</span></span> <span data-ttu-id="b930c-111">De lo contrario, *pNumGuids* recibe el número real de GUID que se copian en la matriz *pGuids* .</span><span class="sxs-lookup"><span data-stu-id="b930c-111">Otherwise, *pNumGuids* receives the actual number of GUIDs that are copied to the *pGuids* array.</span></span>

</dd> <dt>

<span data-ttu-id="b930c-112">*pGuids*</span><span class="sxs-lookup"><span data-stu-id="b930c-112">*pGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="b930c-113">Dirección de una matriz de GUID o **null**.</span><span class="sxs-lookup"><span data-stu-id="b930c-113">Address of an array of GUIDs or **NULL**.</span></span> <span data-ttu-id="b930c-114">Si el valor no es **null**, la matriz recibe una lista de GUID que especifican los perfiles de DXVA en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="b930c-114">If the value is non-**NULL**, the array receives a list of GUIDs that specify restricted-mode DXVA profiles.</span></span> <span data-ttu-id="b930c-115">Estos GUID se definen en DXVA. h y se documentan en la [especificación de dxva 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="b930c-115">These GUIDs are defined in dxva.h, and are documented in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b930c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b930c-116">Return value</span></span>

<span data-ttu-id="b930c-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b930c-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b930c-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b930c-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b930c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b930c-119">Remarks</span></span>

<span data-ttu-id="b930c-120">Llame a este método dos veces.</span><span class="sxs-lookup"><span data-stu-id="b930c-120">Call this method twice.</span></span> <span data-ttu-id="b930c-121">En la primera llamada, establezca *pGuids* en **null**.</span><span class="sxs-lookup"><span data-stu-id="b930c-121">On the first call, set *pGuids* to **NULL**.</span></span> <span data-ttu-id="b930c-122">El parámetro *pNumGuids* recibe el número de GUID de Perfil de DXVA.</span><span class="sxs-lookup"><span data-stu-id="b930c-122">The *pNumGuids* parameter receives the number of DXVA profile GUIDs.</span></span> <span data-ttu-id="b930c-123">Asigne una matriz de GUID con el tamaño necesario y vuelva a llamar al método.</span><span class="sxs-lookup"><span data-stu-id="b930c-123">Allocate an array of GUIDs with the required size and call the method again.</span></span> <span data-ttu-id="b930c-124">Esta vez, establezca *pGuids* en la dirección de la matriz.</span><span class="sxs-lookup"><span data-stu-id="b930c-124">This time, set *pGuids* to the address of the array.</span></span> <span data-ttu-id="b930c-125">El método rellena la matriz con la lista de GUID de Perfil de DXVA.</span><span class="sxs-lookup"><span data-stu-id="b930c-125">The method fills the array with the list of DXVA profile GUIDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b930c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b930c-126">Requirements</span></span>



| <span data-ttu-id="b930c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b930c-127">Requirement</span></span> | <span data-ttu-id="b930c-128">Value</span><span class="sxs-lookup"><span data-stu-id="b930c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b930c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b930c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b930c-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b930c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b930c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b930c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b930c-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b930c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b930c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b930c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b930c-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b930c-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b930c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b930c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b930c-136">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="b930c-136">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
