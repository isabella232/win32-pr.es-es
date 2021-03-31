---
title: MicrosoftDNS_SRVType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de servicio (SRV).
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- DNS de la clase MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea955cad281e9361b4fa1ca5b033a4ca0d39719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491158"
---
# <a name="microsoftdns_srvtype-class"></a><span data-ttu-id="fc87f-105">MicrosoftDNS ( \_ clase SRVType)</span><span class="sxs-lookup"><span data-stu-id="fc87f-105">MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="fc87f-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de servicio (SRV).</span><span class="sxs-lookup"><span data-stu-id="fc87f-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Service (SRV) record.</span></span>

<span data-ttu-id="fc87f-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="fc87f-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc87f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc87f-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a><span data-ttu-id="fc87f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc87f-109">Members</span></span>

<span data-ttu-id="fc87f-110">La clase **MicrosoftDNS \_ SRVType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fc87f-110">The **MicrosoftDNS\_SRVType** class has these types of members:</span></span>

-   [<span data-ttu-id="fc87f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc87f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc87f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc87f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc87f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc87f-113">Methods</span></span>

<span data-ttu-id="fc87f-114">La clase **MicrosoftDNS \_ SRVType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fc87f-114">The **MicrosoftDNS\_SRVType** class has these methods.</span></span>



| <span data-ttu-id="fc87f-115">Método</span><span class="sxs-lookup"><span data-stu-id="fc87f-115">Method</span></span>                             | <span data-ttu-id="fc87f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc87f-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc87f-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fc87f-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fc87f-118">Crea una instancia de un tipo SRV de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el propietario o el nombre del destino, la clase (valor predeterminado = en), el valor de período de vida y la prioridad, el peso, el puerto y el nombre de dominio del host de destino.</span><span class="sxs-lookup"><span data-stu-id="fc87f-118">Instantiates an SRV Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/target Name, class (default = IN), time-to-live value, and target host's priority, weight, port, and domain name.</span></span> <span data-ttu-id="fc87f-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="fc87f-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fc87f-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="fc87f-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fc87f-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="fc87f-121">**Modify**</span></span>                         | <span data-ttu-id="fc87f-122">Actualiza el TTL, la prioridad, el peso, el puerto y el nombre de dominio a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="fc87f-122">Updates the TTL, Priority, Weight, Port, and Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fc87f-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="fc87f-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fc87f-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="fc87f-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fc87f-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="fc87f-125">Qualifiers: Implemented</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="fc87f-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc87f-126">Properties</span></span>

<span data-ttu-id="fc87f-127">La clase **MicrosoftDNS \_ SRVType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc87f-127">The **MicrosoftDNS\_SRVType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc87f-128">**Puerto**</span><span class="sxs-lookup"><span data-stu-id="fc87f-128">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc87f-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc87f-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc87f-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc87f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc87f-131">Puerto usado en el host de destino de un servicio de protocolo.</span><span class="sxs-lookup"><span data-stu-id="fc87f-131">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="fc87f-132">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="fc87f-132">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc87f-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc87f-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc87f-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc87f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc87f-135">Prioridad del host de destino especificado en el nombre del propietario.</span><span class="sxs-lookup"><span data-stu-id="fc87f-135">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="fc87f-136">Los números más bajos implican prioridades más altas.</span><span class="sxs-lookup"><span data-stu-id="fc87f-136">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="fc87f-137">**SRVDomainName**</span><span class="sxs-lookup"><span data-stu-id="fc87f-137">**SRVDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc87f-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc87f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc87f-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc87f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc87f-140">FQDN del host de destino.</span><span class="sxs-lookup"><span data-stu-id="fc87f-140">FQDN of the target host.</span></span> <span data-ttu-id="fc87f-141">Un destino de \\ . \\ significa que el servicio no está disponible en este dominio.</span><span class="sxs-lookup"><span data-stu-id="fc87f-141">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="fc87f-142">**Peso**</span><span class="sxs-lookup"><span data-stu-id="fc87f-142">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc87f-143">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc87f-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc87f-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc87f-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc87f-145">Peso del host de destino.</span><span class="sxs-lookup"><span data-stu-id="fc87f-145">Weight of the target host.</span></span> <span data-ttu-id="fc87f-146">Esto resulta útil al seleccionar entre los hosts que tienen la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="fc87f-146">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="fc87f-147">Las posibilidades de usar este host deben ser proporcionales a su peso.</span><span class="sxs-lookup"><span data-stu-id="fc87f-147">The chances of using this host should be proportional to its weight.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc87f-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc87f-148">Requirements</span></span>



| <span data-ttu-id="fc87f-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc87f-149">Requirement</span></span> | <span data-ttu-id="fc87f-150">Value</span><span class="sxs-lookup"><span data-stu-id="fc87f-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc87f-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc87f-151">Minimum supported client</span></span><br/> | <span data-ttu-id="fc87f-152">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fc87f-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fc87f-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc87f-153">Minimum supported server</span></span><br/> | <span data-ttu-id="fc87f-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fc87f-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fc87f-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc87f-155">Namespace</span></span><br/>                | <span data-ttu-id="fc87f-156">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="fc87f-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fc87f-157">MOF</span><span class="sxs-lookup"><span data-stu-id="fc87f-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc87f-158"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc87f-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc87f-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc87f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc87f-160">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS SRVType**</span><span class="sxs-lookup"><span data-stu-id="fc87f-160">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fc87f-161">**Método Modify de la \_ clase MicrosoftDNS SRVType**</span><span class="sxs-lookup"><span data-stu-id="fc87f-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="fc87f-162">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="fc87f-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





