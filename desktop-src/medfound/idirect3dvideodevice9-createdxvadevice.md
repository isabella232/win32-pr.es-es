---
description: Crea un dispositivo descodificador de aceleración de vídeo de DirectX (DXVA).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'IDirect3DVideoDevice9:: CreateDXVADevice (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 50ce7cee350479f4286921b6cdf69b319033c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155188"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a><span data-ttu-id="b7f69-103">IDirect3DVideoDevice9:: CreateDXVADevice (método)</span><span class="sxs-lookup"><span data-stu-id="b7f69-103">IDirect3DVideoDevice9::CreateDXVADevice method</span></span>

<span data-ttu-id="b7f69-104">Crea un dispositivo descodificador de aceleración de vídeo de DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="b7f69-104">Creates a DirectX Video Acceleration (DXVA) decoder device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f69-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7f69-105">Syntax</span></span>


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a><span data-ttu-id="b7f69-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7f69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7f69-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="b7f69-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="b7f69-108">Puntero a un GUID que especifica el dispositivo que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="b7f69-108">Pointer to a GUID that specifies the device to create.</span></span>

</dd> <dt>

<span data-ttu-id="b7f69-109">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="b7f69-109">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="b7f69-110">Puntero a una estructura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica el formato de la imagen sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="b7f69-110">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the format of the uncompressed image.</span></span>

</dd> <dt>

<span data-ttu-id="b7f69-111">*pData*</span><span class="sxs-lookup"><span data-stu-id="b7f69-111">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="b7f69-112">Puntero a una estructura de **\_ ConnectMode de DXVA** que especifica el modo DXVA y el perfil restringido.</span><span class="sxs-lookup"><span data-stu-id="b7f69-112">Pointer to a **DXVA\_ConnectMode** structure that specifies the DXVA mode and restricted profile.</span></span>

</dd> <dt>

<span data-ttu-id="b7f69-113">*DataSize*</span><span class="sxs-lookup"><span data-stu-id="b7f69-113">*DataSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b7f69-114">Tamaño de la estructura de **\_ ConnectMode de DXVA** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="b7f69-114">Size of the **DXVA\_ConnectMode** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b7f69-115">*ppDXVADevice*</span><span class="sxs-lookup"><span data-stu-id="b7f69-115">*ppDXVADevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b7f69-116">Recibe un puntero a la interfaz [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) .</span><span class="sxs-lookup"><span data-stu-id="b7f69-116">Receives a pointer to the [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) interface.</span></span> <span data-ttu-id="b7f69-117">El llamador debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="b7f69-117">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7f69-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7f69-118">Return value</span></span>

<span data-ttu-id="b7f69-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b7f69-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7f69-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7f69-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f69-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7f69-121">Requirements</span></span>



| <span data-ttu-id="b7f69-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f69-122">Requirement</span></span> | <span data-ttu-id="b7f69-123">Value</span><span class="sxs-lookup"><span data-stu-id="b7f69-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b7f69-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7f69-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f69-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b7f69-125">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7f69-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7f69-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f69-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7f69-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b7f69-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7f69-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7f69-129"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7f69-129"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f69-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7f69-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f69-131">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="b7f69-131">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




