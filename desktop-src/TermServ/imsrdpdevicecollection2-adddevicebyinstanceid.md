---
title: IMsRdpDeviceCollection2 AddDeviceByInstanceId, método
description: Agrega un dispositivo que no está en la lista a la recopilación de dispositivos.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- Método AddDeviceByInstanceId Servicios de Escritorio remoto
- Método AddDeviceByInstanceId Servicios de Escritorio remoto, interfaz IMsRdpDeviceCollection2
- Interfaz IMsRdpDeviceCollection2 Servicios de Escritorio remoto, método AddDeviceByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078888"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a><span data-ttu-id="2ee3d-106">IMsRdpDeviceCollection2:: AddDeviceByInstanceId (método)</span><span class="sxs-lookup"><span data-stu-id="2ee3d-106">IMsRdpDeviceCollection2::AddDeviceByInstanceId method</span></span>

<span data-ttu-id="2ee3d-107">Agrega un dispositivo que no está en la lista a la recopilación de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2ee3d-107">Adds an unlisted device to the device collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ee3d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ee3d-108">Syntax</span></span>


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a><span data-ttu-id="2ee3d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ee3d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ee3d-110">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2ee3d-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ee3d-111">Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="2ee3d-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="2ee3d-112">Valor de la enumeración [**RedirectDeviceType**](redirectdevicetype.md) que especifica el tipo de dispositivo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="2ee3d-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device being added.</span></span>

</dd> <dt>

<span data-ttu-id="2ee3d-113">*InstanceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ee3d-113">*InstanceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ee3d-114">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2ee3d-114">Type: **BSTR**</span></span>

<span data-ttu-id="2ee3d-115">Identificador de instancia del dispositivo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="2ee3d-115">The instance identifier of the device to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ee3d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ee3d-116">Return value</span></span>

<span data-ttu-id="2ee3d-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2ee3d-117">Type: **HRESULT**</span></span>

<span data-ttu-id="2ee3d-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2ee3d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2ee3d-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ee3d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee3d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ee3d-120">Requirements</span></span>



| <span data-ttu-id="2ee3d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ee3d-121">Requirement</span></span> | <span data-ttu-id="2ee3d-122">Value</span><span class="sxs-lookup"><span data-stu-id="2ee3d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee3d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ee3d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee3d-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2ee3d-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="2ee3d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ee3d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee3d-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ee3d-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="2ee3d-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2ee3d-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ee3d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ee3d-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2ee3d-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ee3d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ee3d-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ee3d-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ee3d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ee3d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee3d-132">**RedirectDeviceType**</span><span class="sxs-lookup"><span data-stu-id="2ee3d-132">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="2ee3d-133">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="2ee3d-133">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





