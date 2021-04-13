---
title: IMsTscAxEvents OnRequestGoFullScreen, método
description: Se llama cuando el cliente solicita cambiar al modo de pantalla completa y \_ se llama al método IMsTscAdvancedSettings Put ContainerHandledFullScreen para establecer la propiedad ContainerHandledFullScreen en un valor distinto de cero.
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- Método OnRequestGoFullScreen Servicios de Escritorio remoto
- Método OnRequestGoFullScreen Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRequestGoFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c865cd27b447743f781b8563956e7fb2d7f5d703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422422"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a><span data-ttu-id="1102e-106">IMsTscAxEvents:: OnRequestGoFullScreen (método)</span><span class="sxs-lookup"><span data-stu-id="1102e-106">IMsTscAxEvents::OnRequestGoFullScreen method</span></span>

<span data-ttu-id="1102e-107">Se llama cuando el cliente solicita cambiar al modo de pantalla completa y se llama al método [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) para establecer la propiedad **ContainerHandledFullScreen** en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="1102e-107">Called when the client requests to switch to full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called to set the **ContainerHandledFullScreen** property to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1102e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1102e-108">Syntax</span></span>


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="1102e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1102e-109">Parameters</span></span>

<span data-ttu-id="1102e-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1102e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1102e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1102e-111">Return value</span></span>

<span data-ttu-id="1102e-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1102e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1102e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1102e-113">Remarks</span></span>

<span data-ttu-id="1102e-114">En el modo de pantalla completa controlado por contenedores, el contenedor debe entrar en el modo de pantalla completa estándar en respuesta a este evento.</span><span class="sxs-lookup"><span data-stu-id="1102e-114">In container-handled full-screen mode, the container should enter standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="1102e-115">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1102e-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1102e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1102e-116">Requirements</span></span>



| <span data-ttu-id="1102e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1102e-117">Requirement</span></span> | <span data-ttu-id="1102e-118">Value</span><span class="sxs-lookup"><span data-stu-id="1102e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1102e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1102e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1102e-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1102e-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1102e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1102e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1102e-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1102e-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1102e-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1102e-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="1102e-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1102e-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1102e-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1102e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1102e-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1102e-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1102e-127">IID</span><span class="sxs-lookup"><span data-stu-id="1102e-127">IID</span></span><br/>                      | <span data-ttu-id="1102e-128">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="1102e-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1102e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1102e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1102e-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="1102e-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





