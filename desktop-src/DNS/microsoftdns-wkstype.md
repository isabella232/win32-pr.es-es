---
title: MicrosoftDNS_WKSType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de Well-Known Services (WKS).
ms.assetid: 7bbfd518-d473-4127-949b-9133a43ac7a7
keywords:
- DNS de la clase MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WKSType.Modify
- MicrosoftDNS_WKSType.InternetAddress
- MicrosoftDNS_WKSType.IPProtocol
- MicrosoftDNS_WKSType.Services
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7fde08721bb8bb62b93f72b792060b06c15dad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996631"
---
# <a name="microsoftdns_wkstype-class"></a><span data-ttu-id="81fdd-105">MicrosoftDNS ( \_ clase WKSType)</span><span class="sxs-lookup"><span data-stu-id="81fdd-105">MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="81fdd-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de Well-Known Services (WKS).</span><span class="sxs-lookup"><span data-stu-id="81fdd-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Well-Known Services (WKS) record.</span></span>

<span data-ttu-id="81fdd-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="81fdd-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="81fdd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81fdd-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WKSType : MicrosoftDNS_ResourceRecord
{
  string InternetAddress;
  string IPProtocol;
  string Services;
};
```

## <a name="members"></a><span data-ttu-id="81fdd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="81fdd-109">Members</span></span>

<span data-ttu-id="81fdd-110">La clase **MicrosoftDNS \_ WKSType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="81fdd-110">The **MicrosoftDNS\_WKSType** class has these types of members:</span></span>

-   [<span data-ttu-id="81fdd-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="81fdd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="81fdd-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81fdd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="81fdd-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="81fdd-113">Methods</span></span>

<span data-ttu-id="81fdd-114">La clase **MicrosoftDNS \_ WKSType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="81fdd-114">The **MicrosoftDNS\_WKSType** class has these methods.</span></span>



| <span data-ttu-id="81fdd-115">Método</span><span class="sxs-lookup"><span data-stu-id="81fdd-115">Method</span></span>                             | <span data-ttu-id="81fdd-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="81fdd-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81fdd-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="81fdd-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="81fdd-118">Crea una instancia de un tipo WKS de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y la dirección de Internet del propietario, el protocolo IP y la máscara de bits del puerto.</span><span class="sxs-lookup"><span data-stu-id="81fdd-118">Instantiates a WKS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the owner's Internet Address, IP protocol and port bit mask.</span></span> <span data-ttu-id="81fdd-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="81fdd-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="81fdd-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="81fdd-120">Qualifiers: Implemented, static</span></span><br/>  |
| <span data-ttu-id="81fdd-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="81fdd-121">**Modify**</span></span>                         | <span data-ttu-id="81fdd-122">Este método actualiza el TTL, la dirección de Internet, el protocolo IP y los servicios a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="81fdd-122">This method updates the TTL, Internet Address, IP Protocol, and Services to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="81fdd-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="81fdd-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="81fdd-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="81fdd-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="81fdd-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="81fdd-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="81fdd-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81fdd-126">Properties</span></span>

<span data-ttu-id="81fdd-127">La clase **MicrosoftDNS \_ WKSType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="81fdd-127">The **MicrosoftDNS\_WKSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81fdd-128">**InternetAddress**</span><span class="sxs-lookup"><span data-stu-id="81fdd-128">**InternetAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81fdd-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81fdd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81fdd-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81fdd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81fdd-131">Dirección IP de Internet del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="81fdd-131">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="81fdd-132">**IPProtocol**</span><span class="sxs-lookup"><span data-stu-id="81fdd-132">**IPProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81fdd-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81fdd-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81fdd-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81fdd-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81fdd-135">Cadena que representa el protocolo IP para este registro.</span><span class="sxs-lookup"><span data-stu-id="81fdd-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="81fdd-136">Los valores válidos son UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="81fdd-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="81fdd-137">**Servicios**</span><span class="sxs-lookup"><span data-stu-id="81fdd-137">**Services**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81fdd-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81fdd-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81fdd-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81fdd-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81fdd-140">Cadena que contiene todos los servicios utilizados por el registro de servicio conocido (WKS).</span><span class="sxs-lookup"><span data-stu-id="81fdd-140">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81fdd-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81fdd-141">Requirements</span></span>



| <span data-ttu-id="81fdd-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="81fdd-142">Requirement</span></span> | <span data-ttu-id="81fdd-143">Value</span><span class="sxs-lookup"><span data-stu-id="81fdd-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81fdd-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81fdd-144">Minimum supported client</span></span><br/> | <span data-ttu-id="81fdd-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="81fdd-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="81fdd-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81fdd-146">Minimum supported server</span></span><br/> | <span data-ttu-id="81fdd-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81fdd-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="81fdd-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="81fdd-148">Namespace</span></span><br/>                | <span data-ttu-id="81fdd-149">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="81fdd-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="81fdd-150">MOF</span><span class="sxs-lookup"><span data-stu-id="81fdd-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81fdd-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81fdd-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81fdd-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="81fdd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81fdd-153">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WKSType**</span><span class="sxs-lookup"><span data-stu-id="81fdd-153">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="81fdd-154">**Método Modify de la \_ clase MicrosoftDNS WKSType**</span><span class="sxs-lookup"><span data-stu-id="81fdd-154">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="81fdd-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="81fdd-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





