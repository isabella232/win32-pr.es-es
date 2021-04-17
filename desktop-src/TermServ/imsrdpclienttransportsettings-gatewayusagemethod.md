---
title: Propiedad GatewayUsageMethod de IMsRdpClientTransportSettings
description: Especifica cuándo se debe usar un servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayUsageMethod
- Propiedad GatewayUsageMethod Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676638"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a><span data-ttu-id="fed0f-106">IMsRdpClientTransportSettings:: GatewayUsageMethod (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fed0f-106">IMsRdpClientTransportSettings::GatewayUsageMethod property</span></span>

<span data-ttu-id="fed0f-107">Especifica cuándo se debe usar un servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="fed0f-107">Specifies when to use a Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="fed0f-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fed0f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fed0f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fed0f-109">Syntax</span></span>


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="fed0f-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fed0f-110">Property value</span></span>

<span data-ttu-id="fed0f-111">Variable **ULong** que especifica el método de uso del servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fed0f-111">A **ULONG** variable that specifies the RD Gateway server usage method.</span></span> <span data-ttu-id="fed0f-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fed0f-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span data-ttu-id="fed0f-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ \_Modo proxy \_ ninguno \_ directo** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="fed0f-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC\_PROXY\_MODE\_NONE\_DIRECT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="fed0f-114">No use un servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fed0f-114">Do not use an RD Gateway server.</span></span> <span data-ttu-id="fed0f-115">En la interfaz de usuario del cliente de Conexión a Escritorio remoto (RDC), la casilla **omitir el servidor de puerta de enlace de escritorio remoto para direcciones locales** está desactivada.</span><span class="sxs-lookup"><span data-stu-id="fed0f-115">In the Remote Desktop Connection (RDC) client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span data-ttu-id="fed0f-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ \_Modo proxy \_ directo** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="fed0f-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC\_PROXY\_MODE\_DIRECT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="fed0f-117">Use siempre un servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fed0f-117">Always use an RD Gateway server.</span></span> <span data-ttu-id="fed0f-118">En la interfaz de usuario del cliente RDC, se desactiva la casilla **omitir el servidor de puerta de enlace de escritorio remoto para direcciones locales** .</span><span class="sxs-lookup"><span data-stu-id="fed0f-118">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span data-ttu-id="fed0f-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ \_ \_ Detección del modo proxy** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="fed0f-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC\_PROXY\_MODE\_DETECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="fed0f-120">Use un servidor de puerta de enlace de escritorio remoto si no se puede establecer una conexión directa con el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fed0f-120">Use an RD Gateway server if a direct connection cannot be made to the RD Session Host server.</span></span> <span data-ttu-id="fed0f-121">En la interfaz de usuario del cliente RDC, se activa la casilla **omitir el servidor de puerta de enlace de escritorio remoto para direcciones locales** .</span><span class="sxs-lookup"><span data-stu-id="fed0f-121">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span data-ttu-id="fed0f-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ \_ \_ Valor predeterminado del modo proxy** (3 (0X3))</span><span class="sxs-lookup"><span data-stu-id="fed0f-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC\_PROXY\_MODE\_DEFAULT** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="fed0f-123">Utilice la configuración predeterminada del servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fed0f-123">Use the default RD Gateway server settings.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span data-ttu-id="fed0f-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ No \_ hay \_ ninguna \_ detección de modo proxy** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="fed0f-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC\_PROXY\_MODE\_NONE\_DETECT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="fed0f-125">No use un servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fed0f-125">Do not use an RD Gateway server.</span></span> <span data-ttu-id="fed0f-126">En la interfaz de usuario del cliente RDC, se activa la casilla **omitir el servidor de puerta de enlace de escritorio remoto para direcciones locales** .</span><span class="sxs-lookup"><span data-stu-id="fed0f-126">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="fed0f-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fed0f-127">Error codes</span></span>

<span data-ttu-id="fed0f-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="fed0f-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed0f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fed0f-129">Requirements</span></span>



| <span data-ttu-id="fed0f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fed0f-130">Requirement</span></span> | <span data-ttu-id="fed0f-131">Value</span><span class="sxs-lookup"><span data-stu-id="fed0f-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed0f-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fed0f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fed0f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fed0f-133">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="fed0f-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fed0f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fed0f-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fed0f-135">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="fed0f-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fed0f-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="fed0f-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fed0f-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fed0f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fed0f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fed0f-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fed0f-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fed0f-140">IID</span><span class="sxs-lookup"><span data-stu-id="fed0f-140">IID</span></span><br/>                      | <span data-ttu-id="fed0f-141">IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="fed0f-141">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fed0f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="fed0f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed0f-143">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="fed0f-143">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





