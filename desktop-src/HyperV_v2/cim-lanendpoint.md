---
description: Un punto de conexión de comunicación que se puede conectar a una LAN para enviar y recibir tramas de datos. Los puntos de conexión de LAN incluyen Ethernet, token ring e interfaces FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: CIM_LANEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670038"
---
# <a name="cim_lanendpoint-class"></a><span data-ttu-id="ad97c-104">\_Clase LANEndpoint de CIM</span><span class="sxs-lookup"><span data-stu-id="ad97c-104">CIM\_LANEndpoint class</span></span>

<span data-ttu-id="ad97c-105">Un punto de conexión de comunicación que se puede conectar a una LAN para enviar y recibir tramas de datos.</span><span class="sxs-lookup"><span data-stu-id="ad97c-105">A communication endpoint that can connect to a LAN to send and receive data frames.</span></span> <span data-ttu-id="ad97c-106">Los puntos de conexión de LAN incluyen Ethernet, token ring e interfaces FDDI.</span><span class="sxs-lookup"><span data-stu-id="ad97c-106">LAN endpoints include ethernet, token Ring, and FDDI interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad97c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad97c-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a><span data-ttu-id="ad97c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ad97c-108">Members</span></span>

<span data-ttu-id="ad97c-109">La clase **CIM \_ LANEndpoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ad97c-109">The **CIM\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="ad97c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ad97c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad97c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ad97c-111">Properties</span></span>

<span data-ttu-id="ad97c-112">La clase **CIM \_ LANEndpoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ad97c-112">The **CIM\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad97c-113">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="ad97c-113">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad97c-114">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ad97c-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad97c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad97c-116">Una matriz que contiene otras direcciones de unidifusión que se pueden usar para comunicarse con el punto de conexión de LAN.</span><span class="sxs-lookup"><span data-stu-id="ad97c-116">An array that contains other unicast addresses that may be used to communicate with the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="ad97c-117">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="ad97c-117">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad97c-118">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ad97c-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad97c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad97c-120">Una matriz que contiene las direcciones de multidifusión a las que el punto de conexión LAN realiza escuchas.</span><span class="sxs-lookup"><span data-stu-id="ad97c-120">An array that contains the multicast addresses to which the LAN endpoint listens.</span></span>

</dd> <dt>

<span data-ttu-id="ad97c-121">**LANID**</span><span class="sxs-lookup"><span data-stu-id="ad97c-121">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad97c-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ad97c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad97c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-124">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment. LANID, CIM \_ LANSegment. LANID")</span><span class="sxs-lookup"><span data-stu-id="ad97c-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.LANID, CIM\_LANSegment.LANID")</span></span>
</dt> </dl>

<span data-ttu-id="ad97c-125">Etiqueta o identificador del segmento de LAN al que está conectado el extremo.</span><span class="sxs-lookup"><span data-stu-id="ad97c-125">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="ad97c-126">Si el extremo no está conectado actualmente o si no se conoce esta información, **LANID** es NULL.</span><span class="sxs-lookup"><span data-stu-id="ad97c-126">If the endpoint is not currently connected or if this information is unknown, then **LANID** is NULL.</span></span>

</dd> <dt>

<span data-ttu-id="ad97c-127">**LANType**</span><span class="sxs-lookup"><span data-stu-id="ad97c-127">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad97c-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ad97c-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad97c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-130">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("el [**\_ ProtocolEndpoint de CIM**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANCONNECTIVITYSEGMENT. ConnectivityType, CIM \_ LANSegment. LANType ")</span><span class="sxs-lookup"><span data-stu-id="ad97c-130">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.ConnectivityType, CIM\_LANSegment.LANType")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="ad97c-131">Descripción en desuso: el tipo de tecnología que se usa en la LAN.</span><span class="sxs-lookup"><span data-stu-id="ad97c-131">Deprecated description: The kind of technology used on the LAN.</span></span>

 

<span data-ttu-id="ad97c-132">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="ad97c-132">This property is deprecated.</span></span> <span data-ttu-id="ad97c-133">En su lugar, se recomienda usar la propiedad **protocolType** .</span><span class="sxs-lookup"><span data-stu-id="ad97c-133">Instead we recommend that you use the **ProtocolType** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ad97c-134">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ad97c-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ad97c-135">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="ad97c-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="ad97c-136">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="ad97c-136">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="ad97c-137">**TokenRing** (3)</span><span class="sxs-lookup"><span data-stu-id="ad97c-137">**TokenRing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="ad97c-138">**FDDI** (4)</span><span class="sxs-lookup"><span data-stu-id="ad97c-138">**FDDI** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad97c-139">**Mac**</span><span class="sxs-lookup"><span data-stu-id="ad97c-139">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad97c-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ad97c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad97c-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-142">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span><span class="sxs-lookup"><span data-stu-id="ad97c-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span></span>
</dt> </dl>

<span data-ttu-id="ad97c-143">Dirección de unidifusión principal usada por el extremo de LAN.</span><span class="sxs-lookup"><span data-stu-id="ad97c-143">The principal unicast address used by the LAN endpoint.</span></span>

<span data-ttu-id="ad97c-144">La dirección MAC se debe formatear con las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="ad97c-144">The MAC address must be formatted with the following characteristics:</span></span>

-   <span data-ttu-id="ad97c-145">La dirección consta de doce dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="ad97c-145">The address consists of twelve hexadecimal digits.</span></span>
-   <span data-ttu-id="ad97c-146">Cada par de dígitos representa uno de los seis octetos de la dirección MAC.</span><span class="sxs-lookup"><span data-stu-id="ad97c-146">Each pair of digits represents one of the six octets of the MAC address.</span></span>
-   <span data-ttu-id="ad97c-147">Cada par de dígitos debe estar en orden de bits canónico según RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="ad97c-147">Each pair of digits must be in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="ad97c-148">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="ad97c-148">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad97c-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad97c-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad97c-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-151">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="ad97c-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="ad97c-152">Tamaño máximo, en bytes, de los campos de datos enviados o recibidos por el punto de conexión de LAN.</span><span class="sxs-lookup"><span data-stu-id="ad97c-152">The maximum size, in bytes, of data fields sent or received by the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="ad97c-153">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="ad97c-153">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad97c-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ad97c-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad97c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad97c-156">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("el [**\_ ProtocolEndpoint de CIM**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANConnectivitySegment. OtherTypeDescription ","**CIM \_ LANEndpoint**.**LANType**")</span><span class="sxs-lookup"><span data-stu-id="ad97c-156">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.OtherTypeDescription", "**CIM\_LANEndpoint**.**LANType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="ad97c-157">Descripción en desuso: el tipo de tecnología que se usa en la LAN cuando la propiedad **LANType** se establece en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="ad97c-157">Deprecated description: The type of technology used on the LAN when the **LANType** property is set to "1" (Other).</span></span>

 

<span data-ttu-id="ad97c-158">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="ad97c-158">This property is deprecated.</span></span> <span data-ttu-id="ad97c-159">En su lugar, se recomienda usar la propiedad **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="ad97c-159">Instead we recommend that you use the **OtherTypeDescription** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad97c-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad97c-160">Requirements</span></span>



| <span data-ttu-id="ad97c-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad97c-161">Requirement</span></span> | <span data-ttu-id="ad97c-162">Value</span><span class="sxs-lookup"><span data-stu-id="ad97c-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad97c-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad97c-163">Minimum supported client</span></span><br/> | <span data-ttu-id="ad97c-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ad97c-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ad97c-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad97c-165">Minimum supported server</span></span><br/> | <span data-ttu-id="ad97c-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad97c-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ad97c-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ad97c-167">Namespace</span></span><br/>                | <span data-ttu-id="ad97c-168">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ad97c-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ad97c-169">MOF</span><span class="sxs-lookup"><span data-stu-id="ad97c-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad97c-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad97c-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad97c-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ad97c-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad97c-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ad97c-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ad97c-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad97c-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad97c-174">**ProtocolEndpoint de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ad97c-174">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

