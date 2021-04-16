---
title: Propiedad NetworkConnectionType de IMsRdpClientAdvancedSettings7
description: Obtiene o establece el tipo de conexión de red utilizado entre el cliente y el servidor. La información del tipo de conexión de red que se pasa al servidor ayuda al servidor a optimizar varios parámetros según el tipo de conexión de red.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad NetworkConnectionType
- Propiedad NetworkConnectionType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad NetworkConnectionType
- Propiedad NetworkConnectionType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad NetworkConnectionType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686031"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a><span data-ttu-id="ed809-109">IMsRdpClientAdvancedSettings7:: NetworkConnectionType (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ed809-109">IMsRdpClientAdvancedSettings7::NetworkConnectionType property</span></span>

<span data-ttu-id="ed809-110">Obtiene o establece el tipo de conexión de red utilizado entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ed809-110">Gets or sets the type of network connection used between the client and server.</span></span> <span data-ttu-id="ed809-111">La información del tipo de conexión de red que se pasa al servidor ayuda al servidor a optimizar varios parámetros según el tipo de conexión de red.</span><span class="sxs-lookup"><span data-stu-id="ed809-111">The network connection type information passed on to the server helps the server tune several parameters based on the network connection type.</span></span>

<span data-ttu-id="ed809-112">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ed809-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed809-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed809-113">Syntax</span></span>


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a><span data-ttu-id="ed809-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ed809-114">Property value</span></span>

<span data-ttu-id="ed809-115">El tipo de conexión de red.</span><span class="sxs-lookup"><span data-stu-id="ed809-115">The network connection type.</span></span>

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span data-ttu-id="ed809-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Conexión \_ de \_Módem de tipo** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="ed809-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**CONNECTION\_TYPE\_MODEM** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="ed809-117">Módem (56 kbps)</span><span class="sxs-lookup"><span data-stu-id="ed809-117">Modem (56 Kbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span data-ttu-id="ed809-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Conexión \_ de Escriba \_ Broadband \_ Low** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="ed809-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**CONNECTION\_TYPE\_BROADBAND\_LOW** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="ed809-119">Banda ancha de baja velocidad (256 kbps a 2 Mbps)</span><span class="sxs-lookup"><span data-stu-id="ed809-119">Low-speed broadband (256 Kbps to 2 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span data-ttu-id="ed809-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Conexión \_ de Escriba \_ Satellite** (3 (0X3))</span><span class="sxs-lookup"><span data-stu-id="ed809-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**CONNECTION\_TYPE\_SATELLITE** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="ed809-121">Satélite (de 2 Mbps a 16 Mbps con latencia alta)</span><span class="sxs-lookup"><span data-stu-id="ed809-121">Satellite (2 Mbps to 16 Mbps, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span data-ttu-id="ed809-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Conexión \_ de Escriba \_ banda ancha \_ alta** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="ed809-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**CONNECTION\_TYPE\_BROADBAND\_HIGH** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="ed809-123">Banda ancha de alta velocidad (de 2 Mbps a 10 Mbps)</span><span class="sxs-lookup"><span data-stu-id="ed809-123">High-speed broadband (2 Mbps to 10 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span data-ttu-id="ed809-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Conexión \_ de TIPO \_ WAN** (5 (0X5))</span><span class="sxs-lookup"><span data-stu-id="ed809-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**CONNECTION\_TYPE\_WAN** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="ed809-125">Red de área extensa (WAN) (10 Mbps o superior, con latencia alta)</span><span class="sxs-lookup"><span data-stu-id="ed809-125">Wide area network (WAN) (10 Mbps or higher, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span data-ttu-id="ed809-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Conexión \_ de Escriba \_ LAN** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="ed809-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**CONNECTION\_TYPE\_LAN** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="ed809-127">Red de área local (LAN) (10 Mbps o superior)</span><span class="sxs-lookup"><span data-stu-id="ed809-127">Local area network (LAN) (10 Mbps or higher)</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed809-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed809-128">Requirements</span></span>



| <span data-ttu-id="ed809-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed809-129">Requirement</span></span> | <span data-ttu-id="ed809-130">Value</span><span class="sxs-lookup"><span data-stu-id="ed809-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed809-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed809-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ed809-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed809-132">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="ed809-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed809-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ed809-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ed809-134">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="ed809-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ed809-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="ed809-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed809-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ed809-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed809-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed809-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed809-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ed809-139">IID</span><span class="sxs-lookup"><span data-stu-id="ed809-139">IID</span></span><br/>                      | <span data-ttu-id="ed809-140">IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="ed809-140">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed809-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed809-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed809-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ed809-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ed809-143">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ed809-143">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





