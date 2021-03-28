---
description: Esta clase es la clase de tipo de evento para eventos de red. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: SystemConfig_Network (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23b469c31645c6a5b04319f91b758ee19beb935c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984451"
---
# <a name="systemconfig_network-class"></a><span data-ttu-id="9f061-104">\_Clase de red SystemConfig</span><span class="sxs-lookup"><span data-stu-id="9f061-104">SystemConfig\_Network class</span></span>

<span data-ttu-id="9f061-105">Esta clase es la clase de tipo de evento para eventos de red.</span><span class="sxs-lookup"><span data-stu-id="9f061-105">This class is the event type class for network events.</span></span>

<span data-ttu-id="9f061-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="9f061-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f061-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f061-107">Syntax</span></span>

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a><span data-ttu-id="9f061-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9f061-108">Members</span></span>

<span data-ttu-id="9f061-109">La clase de **\_ red SystemConfig** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9f061-109">The **SystemConfig\_Network** class has these types of members:</span></span>

-   [<span data-ttu-id="9f061-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f061-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f061-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f061-111">Properties</span></span>

<span data-ttu-id="9f061-112">La clase de **\_ red SystemConfig** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f061-112">The **SystemConfig\_Network** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f061-113">**MaxHashTableSize**</span><span class="sxs-lookup"><span data-stu-id="9f061-113">**MaxHashTableSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f061-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f061-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f061-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f061-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f061-116">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="9f061-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="9f061-117">Tamaño de la tabla hash en la que se almacenan los bloques de control TCP (TCBs).</span><span class="sxs-lookup"><span data-stu-id="9f061-117">The size of the hash table in which TCP control blocks (TCBs) are stored.</span></span> <span data-ttu-id="9f061-118">TCP almacena los bloques de control en una tabla hash para que pueda encontrarlos muy rápidamente.</span><span class="sxs-lookup"><span data-stu-id="9f061-118">TCP stores control blocks in a hash table so it can find them very quickly.</span></span>

</dd> <dt>

<span data-ttu-id="9f061-119">**MaxUserPort**</span><span class="sxs-lookup"><span data-stu-id="9f061-119">**MaxUserPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f061-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f061-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f061-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f061-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f061-122">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="9f061-122">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="9f061-123">El número de Puerto máximo TCP puede asignar cuando una aplicación solicita un puerto de usuario disponible del sistema.</span><span class="sxs-lookup"><span data-stu-id="9f061-123">The highest port number TCP can assign when an application requests an available user port from the system.</span></span> <span data-ttu-id="9f061-124">Normalmente, los puertos efímeros (los usados brevemente) se asignan a los números de puerto de 1024 a 5000.</span><span class="sxs-lookup"><span data-stu-id="9f061-124">Typically, ephemeral ports (those used briefly) are allocated to port numbers 1024 through 5000.</span></span>

<span data-ttu-id="9f061-125">El valor del número de puerto de usuario más alto que TCP puede asignar se controla mediante una configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="9f061-125">The value for the highest user port number TCP can assign is controlled by a registry setting.</span></span> <span data-ttu-id="9f061-126">Para obtener más información, consulte [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="9f061-126">For more information, see [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span></span>

</dd> <dt>

<span data-ttu-id="9f061-127">**TcbTablePartitions**</span><span class="sxs-lookup"><span data-stu-id="9f061-127">**TcbTablePartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f061-128">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f061-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f061-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f061-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f061-130">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="9f061-130">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="9f061-131">El número de particiones en la tabla de bloque de control de transporte.</span><span class="sxs-lookup"><span data-stu-id="9f061-131">The number of partitions in the Transport Control Block table.</span></span> <span data-ttu-id="9f061-132">La creación de particiones en la tabla de bloques de control de transporte minimiza la contención del acceso a las tablas.</span><span class="sxs-lookup"><span data-stu-id="9f061-132">Partitioning the Transport Control Block table minimizes contention for table access.</span></span> <span data-ttu-id="9f061-133">Esto es especialmente útil en sistemas multiprocesador.</span><span class="sxs-lookup"><span data-stu-id="9f061-133">This is especially useful on multiprocessor systems.</span></span>

</dd> <dt>

<span data-ttu-id="9f061-134">**TcpTimedWaitDelay**</span><span class="sxs-lookup"><span data-stu-id="9f061-134">**TcpTimedWaitDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f061-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f061-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f061-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f061-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f061-137">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="9f061-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="9f061-138">El tiempo que debe transcurrir antes de que TCP pueda liberar una conexión cerrada y volver a usar sus recursos.</span><span class="sxs-lookup"><span data-stu-id="9f061-138">The time that must elapse before TCP can release a closed connection and reuse its resources.</span></span> <span data-ttu-id="9f061-139">Este intervalo entre el cierre y la versión se conoce como \_ Estado de espera de tiempo o estado de 2MSL.</span><span class="sxs-lookup"><span data-stu-id="9f061-139">This interval between closure and release is known as the TIME\_WAIT state or 2MSL state.</span></span> <span data-ttu-id="9f061-140">Durante este tiempo, la conexión se puede volver a abrir mucho menos en el cliente y el servidor que en el establecimiento de una nueva conexión.</span><span class="sxs-lookup"><span data-stu-id="9f061-140">During this time, the connection can be reopened at much less cost to the client and server than establishing a new connection.</span></span>

<span data-ttu-id="9f061-141">RFC 793 publicado por IETF requiere que TCP mantenga una conexión cerrada para un intervalo de al menos igual al doble de la duración máxima del segmento (2MSL) de la red.</span><span class="sxs-lookup"><span data-stu-id="9f061-141">RFC 793 published by the IETF requires that TCP maintains a closed connection for an interval at least equal to twice the maximum segment lifetime (2MSL) of the network.</span></span> <span data-ttu-id="9f061-142">Cuando se libera una conexión, su par de sockets y el bloque de control TCP (TCB) se pueden usar para admitir otra conexión.</span><span class="sxs-lookup"><span data-stu-id="9f061-142">When a connection is released, its socket pair and TCP control block (TCB) can be used to support another connection.</span></span> <span data-ttu-id="9f061-143">De forma predeterminada, el MSL se define como 120 segundos y el valor de esta entrada es igual a dos MSLs, o 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="9f061-143">By default, the MSL is defined to be 120 seconds, and the value of this entry is equal to two MSLs, or 4 minutes.</span></span> <span data-ttu-id="9f061-144">Para obtener más información, consulte [RFC 793](https://tools.ietf.org/html/rfc973).</span><span class="sxs-lookup"><span data-stu-id="9f061-144">For more information, see [RFC 793](https://tools.ietf.org/html/rfc973).</span></span>

<span data-ttu-id="9f061-145">Reducir el valor de esta entrada mediante una configuración de registro permite a TCP liberar conexiones cerradas más rápido, lo que proporciona más recursos para las nuevas conexiones.</span><span class="sxs-lookup"><span data-stu-id="9f061-145">Reducing the value of this entry using a registry setting allows TCP to release closed connections faster, providing more resources for new connections.</span></span> <span data-ttu-id="9f061-146">Sin embargo, si el valor es demasiado bajo, es posible que TCP libere recursos de conexión antes de que se complete la conexión, lo que requiere que el servidor use recursos adicionales para restablecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="9f061-146">However, if the value is too low, TCP might release connection resources before the connection is complete, requiring the server to use additional resources to reestablish the connection.</span></span>

<span data-ttu-id="9f061-147">Normalmente, TCP no libera las conexiones cerradas hasta que expire el valor de esta entrada.</span><span class="sxs-lookup"><span data-stu-id="9f061-147">Normally, TCP does not release closed connections until the value of this entry expires.</span></span> <span data-ttu-id="9f061-148">Sin embargo, TCP puede liberar conexiones antes de que este valor expire si se está quedando sin bloques de control TCP (TCBs).</span><span class="sxs-lookup"><span data-stu-id="9f061-148">However, TCP can release connections before this value expires if it is running out of TCP control blocks (TCBs).</span></span> <span data-ttu-id="9f061-149">El número de TCBs que crea el sistema se controla mediante una configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="9f061-149">The number of TCBs the system creates is controlled by a registry setting.</span></span> <span data-ttu-id="9f061-150">Para obtener más información, vea [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="9f061-150">For more information, see [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f061-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f061-151">Requirements</span></span>



| <span data-ttu-id="9f061-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f061-152">Requirement</span></span> | <span data-ttu-id="9f061-153">Value</span><span class="sxs-lookup"><span data-stu-id="9f061-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9f061-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f061-154">Minimum supported client</span></span><br/> | <span data-ttu-id="9f061-155">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9f061-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9f061-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f061-156">Minimum supported server</span></span><br/> | <span data-ttu-id="9f061-157">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f061-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f061-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f061-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f061-159">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="9f061-159">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 
