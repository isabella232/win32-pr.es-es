---
title: IMsRdpClient9 SyncSessionDisplaySettings, método
description: Sincroniza la configuración de presentación de la sesión.
ms.assetid: cc2c497f-665a-458d-895b-21dd21977890
ms.tgt_platform: multiple
keywords:
- Método SyncSessionDisplaySettings Servicios de Escritorio remoto
- Método SyncSessionDisplaySettings Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método SyncSessionDisplaySettings
- Método SyncSessionDisplaySettings Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método SyncSessionDisplaySettings
topic_type:
- apiref
api_name:
- IMsRdpClient9.SyncSessionDisplaySettings
- IMsRdpClient10.SyncSessionDisplaySettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4429f966c00fb608416d541bec229defeca3e5b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995948"
---
# <a name="imsrdpclient9syncsessiondisplaysettings-method"></a><span data-ttu-id="eb086-108">IMsRdpClient9:: SyncSessionDisplaySettings (método)</span><span class="sxs-lookup"><span data-stu-id="eb086-108">IMsRdpClient9::SyncSessionDisplaySettings method</span></span>

<span data-ttu-id="eb086-109">Sincroniza la configuración de presentación de la sesión.</span><span class="sxs-lookup"><span data-stu-id="eb086-109">Synchronizes session display settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb086-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb086-110">Syntax</span></span>


```C++
HRESULT SyncSessionDisplaySettings();
```



## <a name="parameters"></a><span data-ttu-id="eb086-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb086-111">Parameters</span></span>

<span data-ttu-id="eb086-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="eb086-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb086-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb086-113">Return value</span></span>

<span data-ttu-id="eb086-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="eb086-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb086-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb086-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb086-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb086-116">Requirements</span></span>



| <span data-ttu-id="eb086-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb086-117">Requirement</span></span> | <span data-ttu-id="eb086-118">Value</span><span class="sxs-lookup"><span data-stu-id="eb086-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb086-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb086-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eb086-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="eb086-120">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="eb086-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb086-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eb086-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="eb086-122">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="eb086-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="eb086-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb086-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb086-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="eb086-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb086-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb086-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb086-126"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="eb086-127">IID</span><span class="sxs-lookup"><span data-stu-id="eb086-127">IID</span></span><br/>                      | <span data-ttu-id="eb086-128">CLSID \_ MsRdpClient9 se define como 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="eb086-128">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="eb086-129">CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="eb086-129">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="eb086-130">IID \_ IMsRdpClient9 se define como 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="eb086-130">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb086-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb086-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb086-132">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="eb086-132">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="eb086-133">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="eb086-133">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





