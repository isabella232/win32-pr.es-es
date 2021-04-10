---
description: El método OnStart es un método opcional que puede ser implementado por el monitor. MCSVC llama a este método para solicitar que el monitor inicie la captura.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'IMonitor:: OnStart (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153849"
---
# <a name="imonitoronstart-method"></a><span data-ttu-id="f70db-104">IMonitor:: OnStart (método)</span><span class="sxs-lookup"><span data-stu-id="f70db-104">IMonitor::OnStart method</span></span>

<span data-ttu-id="f70db-105">El método **OnStart** es un método opcional que puede ser implementado por el monitor.</span><span class="sxs-lookup"><span data-stu-id="f70db-105">The **OnStart** method is an optional method that can be implemented by the monitor.</span></span> <span data-ttu-id="f70db-106">MCSVC llama a este método para solicitar que el monitor inicie la captura.</span><span class="sxs-lookup"><span data-stu-id="f70db-106">The MCSVC calls this method to request that the monitor start the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70db-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f70db-107">Syntax</span></span>


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a><span data-ttu-id="f70db-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f70db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f70db-109">*pUnkNPP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f70db-109">*pUnkNPP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f70db-110">Un puntero [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) a la interfaz [IRTC](irtc.md) .</span><span class="sxs-lookup"><span data-stu-id="f70db-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer to the [IRTC](irtc.md) interface.</span></span> <span data-ttu-id="f70db-111">El monitor puede utilizar esta interfaz para obtener estadísticas que se pueden usar para determinar si se debe iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="f70db-111">The monitor can use this interface to obtain statistics that can be used to determine if the capture should be started.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f70db-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f70db-112">Return value</span></span>

<span data-ttu-id="f70db-113">Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError).</span><span class="sxs-lookup"><span data-stu-id="f70db-113">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="f70db-114">Cuando \_ se devuelve, el MCSVC llama al método [IRTC:: Start](irtc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="f70db-114">When S\_OK is returned, the MCSVC calls the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="f70db-115">Si el método no se realiza correctamente, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="f70db-115">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="f70db-116">El MCSVC no iniciará la captura si se devuelve algún código de error.</span><span class="sxs-lookup"><span data-stu-id="f70db-116">The MCSVC will not start the capture if any error code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="f70db-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f70db-117">Remarks</span></span>

<span data-ttu-id="f70db-118">El MCSVC llama a este método antes de que se llame al método [IRTC:: Start](irtc-start.md) del NPP para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="f70db-118">The MCSVC calls this method before the NPP's [IRTC::Start](irtc-start.md) method is called to start the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70db-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f70db-119">Requirements</span></span>



| <span data-ttu-id="f70db-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f70db-120">Requirement</span></span> | <span data-ttu-id="f70db-121">Value</span><span class="sxs-lookup"><span data-stu-id="f70db-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f70db-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f70db-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f70db-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f70db-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f70db-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f70db-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f70db-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f70db-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f70db-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f70db-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f70db-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f70db-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f70db-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f70db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70db-129">IMonitor</span><span class="sxs-lookup"><span data-stu-id="f70db-129">IMonitor</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="f70db-130">Proveedores de paquetes de red</span><span class="sxs-lookup"><span data-stu-id="f70db-130">Network Packet Providers</span></span>](network-packet-providers.md)
</dt> </dl>

 

