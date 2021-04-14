---
title: IMsTscAxEvents OnRequestContainerMinimize, método
description: Se llama cuando el usuario presiona el botón minimizar en la barra de conexión en el modo de pantalla completa. La activación de este evento es una solicitud que la aplicación contenedora se minimiza por sí misma.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Método OnRequestContainerMinimize Servicios de Escritorio remoto
- Método OnRequestContainerMinimize Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRequestContainerMinimize
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85387e3b156eed29dc7068eac84280be521a934e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422423"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a><span data-ttu-id="5258e-107">IMsTscAxEvents:: OnRequestContainerMinimize (método)</span><span class="sxs-lookup"><span data-stu-id="5258e-107">IMsTscAxEvents::OnRequestContainerMinimize method</span></span>

<span data-ttu-id="5258e-108">Se llama cuando el usuario presiona el botón **minimizar** en la barra de conexión en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="5258e-108">Called when the user presses the **Minimize** button on the connection bar in full-screen mode.</span></span> <span data-ttu-id="5258e-109">La activación de este evento es una solicitud que la aplicación contenedora se minimiza por sí misma.</span><span class="sxs-lookup"><span data-stu-id="5258e-109">The firing of this event is a request that the container application minimize itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="5258e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5258e-110">Syntax</span></span>


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a><span data-ttu-id="5258e-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5258e-111">Parameters</span></span>

<span data-ttu-id="5258e-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5258e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5258e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5258e-113">Return value</span></span>

<span data-ttu-id="5258e-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5258e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5258e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5258e-115">Remarks</span></span>

<span data-ttu-id="5258e-116">Solo se llamará a este método si está habilitado el modo de pantalla completa controlado por contenedores; consulte [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5258e-116">This method will only be called if the container-handled full-screen mode is enabled - see [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5258e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5258e-117">Requirements</span></span>



| <span data-ttu-id="5258e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5258e-118">Requirement</span></span> | <span data-ttu-id="5258e-119">Value</span><span class="sxs-lookup"><span data-stu-id="5258e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5258e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5258e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5258e-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5258e-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5258e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5258e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5258e-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5258e-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5258e-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5258e-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="5258e-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5258e-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5258e-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5258e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5258e-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5258e-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5258e-128">IID</span><span class="sxs-lookup"><span data-stu-id="5258e-128">IID</span></span><br/>                      | <span data-ttu-id="5258e-129">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="5258e-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="5258e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5258e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5258e-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="5258e-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





