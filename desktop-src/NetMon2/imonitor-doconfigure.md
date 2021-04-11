---
description: El monitor debe implementar el método configure. MCSVC llama a este método para obtener información de configuración de la captura.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: IMonitor::D método oConfigure (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154145"
---
# <a name="imonitordoconfigure-method"></a><span data-ttu-id="7d82d-104">IMonitor::D método oConfigure</span><span class="sxs-lookup"><span data-stu-id="7d82d-104">IMonitor::DoConfigure method</span></span>

<span data-ttu-id="7d82d-105">El monitor debe implementar el método **Configure** .</span><span class="sxs-lookup"><span data-stu-id="7d82d-105">The **DoConfigure** method must be implemented by the monitor.</span></span> <span data-ttu-id="7d82d-106">MCSVC llama a este método para obtener información de configuración de la captura.</span><span class="sxs-lookup"><span data-stu-id="7d82d-106">The MCSVC calls this method to obtain configuration information for the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d82d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d82d-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a><span data-ttu-id="7d82d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d82d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d82d-109">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d82d-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d82d-110">Nombre de una instancia del monitor.</span><span class="sxs-lookup"><span data-stu-id="7d82d-110">Name of an instance of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7d82d-111">*pConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d82d-111">*pConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d82d-112">Cadena de configuración proporcionada por MCSVC.</span><span class="sxs-lookup"><span data-stu-id="7d82d-112">Configuration string provided by the MCSVC.</span></span> <span data-ttu-id="7d82d-113">El monitor debe analizar esta cadena para los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="7d82d-113">The monitor must parse this string for configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="7d82d-114">*ppScriptInstance* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7d82d-114">*ppScriptInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d82d-115">Dirección de la cadena HTML utilizada para configurar el monitor.</span><span class="sxs-lookup"><span data-stu-id="7d82d-115">Address of the HTML string used to configure the monitor.</span></span> <span data-ttu-id="7d82d-116">Si se usa un script predeterminado para la configuración, este valor debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="7d82d-116">If a default script is used for configuration, this value should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d82d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d82d-117">Return value</span></span>

<span data-ttu-id="7d82d-118">Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es el mismo que NoError) y MCSVC ejecutará el monitor.</span><span class="sxs-lookup"><span data-stu-id="7d82d-118">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC will run the monitor.</span></span>

<span data-ttu-id="7d82d-119">Si el método no se realiza correctamente, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="7d82d-119">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="7d82d-120">Un valor devuelto de NMERR \_ monitor \_ config \_ no es aceptable, pero cuando se devuelve este error, el monitor no puede iniciarse hasta que se realice correctamente una llamada **configurada** en el futuro.</span><span class="sxs-lookup"><span data-stu-id="7d82d-120">A return value of NMERR\_MONITOR\_CONFIG\_FAILED is acceptable, but when this error is returned, the monitor cannot start until a future **DoConfigure** call succeeds.</span></span> <span data-ttu-id="7d82d-121">Cualquier otro error impide que la instancia del monitor esté habilitada.</span><span class="sxs-lookup"><span data-stu-id="7d82d-121">Any other error prevents the instance of the monitor from being enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d82d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d82d-122">Remarks</span></span>

<span data-ttu-id="7d82d-123">El MCSVC llama a este método después de que se haya conectado a la red y antes de que se llame al método [IRTC:: configure](irtc-configure.md) .</span><span class="sxs-lookup"><span data-stu-id="7d82d-123">The MCSVC calls this method after it has connected to the network and before the [IRTC::Configure](irtc-configure.md) method is called.</span></span>

<span data-ttu-id="7d82d-124">El monitor puede almacenar la información proporcionada por esta llamada, actualizar el script HTML o la cadena de configuración y establecer el [filtro de captura](capture-filters.md) en el BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="7d82d-124">The monitor can store information provided by this call, update the HTML script or configuration string, and set the [capture filter](capture-filters.md) in the NPP BLOB.</span></span>

<span data-ttu-id="7d82d-125">MCSVC puede llamar a este método varias veces, pero no se puede llamar mientras el monitor está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="7d82d-125">The MCSVC may call this method several times, but it cannot be not called while the monitor is capturing data.</span></span> <span data-ttu-id="7d82d-126">Tenga en cuenta que cada vez que un [NPP](network-packet-providers.md) inicia una captura, se debe configurar la conexión a la red.</span><span class="sxs-lookup"><span data-stu-id="7d82d-126">Note that every time an [NPP](network-packet-providers.md) starts a capture, the connection to the network must be configured.</span></span> <span data-ttu-id="7d82d-127">Esta restricción incluye situaciones en las que se inicia NPP y detiene la misma captura.</span><span class="sxs-lookup"><span data-stu-id="7d82d-127">This restriction includes situations in which the NPP starts and stops the same capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d82d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d82d-128">Requirements</span></span>



| <span data-ttu-id="7d82d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d82d-129">Requirement</span></span> | <span data-ttu-id="7d82d-130">Value</span><span class="sxs-lookup"><span data-stu-id="7d82d-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7d82d-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d82d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7d82d-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7d82d-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7d82d-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d82d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7d82d-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7d82d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7d82d-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d82d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d82d-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d82d-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




