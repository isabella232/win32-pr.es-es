---
title: MSAD_ReplCursor (clase)
description: Proporciona información de estado de replicación de entrada sobre todas las réplicas de un contexto de nomenclatura determinado (NC).
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor clase Active Directory
- Active Directory de MSAD_ReplCursor de clase, se describe
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490738"
---
# <a name="msad_replcursor-class"></a><span data-ttu-id="0ba16-105">MSAD \_ ReplCursor (clase)</span><span class="sxs-lookup"><span data-stu-id="0ba16-105">MSAD\_ReplCursor class</span></span>

<span data-ttu-id="0ba16-106">Proporciona información de estado de replicación de entrada sobre todas las réplicas de un contexto de nomenclatura determinado (NC).</span><span class="sxs-lookup"><span data-stu-id="0ba16-106">Provides inbound replication state information about all replicas of a given naming context (NC).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba16-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ba16-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a><span data-ttu-id="0ba16-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ba16-108">Members</span></span>

<span data-ttu-id="0ba16-109">La clase **MSAD \_ ReplCursor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0ba16-109">The **MSAD\_ReplCursor** class has these types of members:</span></span>

-   [<span data-ttu-id="0ba16-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0ba16-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ba16-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0ba16-111">Properties</span></span>

<span data-ttu-id="0ba16-112">La clase **MSAD \_ ReplCursor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0ba16-112">The **MSAD\_ReplCursor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ba16-113">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="0ba16-113">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba16-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0ba16-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="0ba16-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0ba16-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ba16-116">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ba16-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ba16-117">Obtiene la ruta de acceso X. 500 para el contexto de nomenclatura (NC) que contiene este cursor.</span><span class="sxs-lookup"><span data-stu-id="0ba16-117">Gets the X.500 path for the naming context (NC) that holds this cursor.</span></span>

</dd> <dt>

<span data-ttu-id="0ba16-118">**SourceDsaDN**</span><span class="sxs-lookup"><span data-stu-id="0ba16-118">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba16-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0ba16-119">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="0ba16-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0ba16-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba16-121">Obtiene la ruta de acceso X. 500 para el agente de sistema de directorio (DSA) que representa el controlador de dominio de origen (DC).</span><span class="sxs-lookup"><span data-stu-id="0ba16-121">Gets the X.500 path for the directory system agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="0ba16-122">**SourceDsaInvocationID**</span><span class="sxs-lookup"><span data-stu-id="0ba16-122">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba16-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0ba16-123">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="0ba16-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0ba16-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ba16-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ba16-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ba16-126">Obtiene el identificador de invocación del servidor de origen al que corresponde el **USNAttributeFilter** .</span><span class="sxs-lookup"><span data-stu-id="0ba16-126">Gets the invocation identifier of the originating server to which the **USNAttributeFilter** corresponds.</span></span>

</dd> <dt>

<span data-ttu-id="0ba16-127">**TimeOfLastSuccessfulSync**</span><span class="sxs-lookup"><span data-stu-id="0ba16-127">**TimeOfLastSuccessfulSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba16-128">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0ba16-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0ba16-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0ba16-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba16-130">Obtiene la marca de tiempo de la última sincronización de replicación correcta con el DSA de origen.</span><span class="sxs-lookup"><span data-stu-id="0ba16-130">Gets the timestamp of the last successful replication sync with the source DSA.</span></span> <span data-ttu-id="0ba16-131">Indica la hora a la que este DC vio por última vez los cambios realizados en el DSA de origen para este NC.</span><span class="sxs-lookup"><span data-stu-id="0ba16-131">Indicates the time when this DC last saw changes made on the source DSA for this NC.</span></span>

</dd> <dt>

<span data-ttu-id="0ba16-132">**USNAttributeFilter**</span><span class="sxs-lookup"><span data-stu-id="0ba16-132">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba16-133">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0ba16-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0ba16-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0ba16-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba16-135">Obtiene el número máximo de secuencias de actualización al que el servidor de destino puede indicar que ha registrado todos los cambios originados por el servidor determinado en números de secuencia de actualización menores o iguales que este número de secuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="0ba16-135">Gets the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number.</span></span> <span data-ttu-id="0ba16-136">Esta propiedad se utiliza para filtrar los cambios que el servidor de destino ya ha aplicado en los servidores de origen de replicación.</span><span class="sxs-lookup"><span data-stu-id="0ba16-136">This property is used to filter changes that the destination server has already applied at replication source servers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ba16-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ba16-137">Requirements</span></span>



| <span data-ttu-id="0ba16-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ba16-138">Requirement</span></span> | <span data-ttu-id="0ba16-139">Value</span><span class="sxs-lookup"><span data-stu-id="0ba16-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba16-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ba16-140">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba16-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0ba16-141">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0ba16-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ba16-142">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba16-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ba16-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ba16-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0ba16-144">Namespace</span></span><br/>                | <span data-ttu-id="0ba16-145">\\MicrosoftActiveDirectory raíz</span><span class="sxs-lookup"><span data-stu-id="0ba16-145">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="0ba16-146">MOF</span><span class="sxs-lookup"><span data-stu-id="0ba16-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ba16-147"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ba16-147"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ba16-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0ba16-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ba16-149"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ba16-149"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba16-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ba16-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba16-151">**\_cursor de replicación de DS \_**</span><span class="sxs-lookup"><span data-stu-id="0ba16-151">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

