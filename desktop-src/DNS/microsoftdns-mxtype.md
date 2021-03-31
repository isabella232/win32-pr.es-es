---
title: MicrosoftDNS_MXType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un RR de intercambio de correo (MR).
ms.assetid: 7c147628-5bda-48dd-beb4-e630d1886da8
keywords:
- DNS de la clase MicrosoftDNS_MXType
- MicrosoftDNS_MXType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
- MicrosoftDNS_MXType.Modify
- MicrosoftDNS_MXType.Preference
- MicrosoftDNS_MXType.MailExchange
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652743178b71b2f9fed296ecfa4427f85b5cf1c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996394"
---
# <a name="microsoftdns_mxtype-class"></a><span data-ttu-id="652ed-105">MicrosoftDNS ( \_ clase MXType)</span><span class="sxs-lookup"><span data-stu-id="652ed-105">MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="652ed-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un RR de intercambio de correo (MR).</span><span class="sxs-lookup"><span data-stu-id="652ed-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Exchanger (MR) RR.</span></span>

<span data-ttu-id="652ed-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="652ed-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="652ed-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="652ed-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MXType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string MailExchange;
};
```

## <a name="members"></a><span data-ttu-id="652ed-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="652ed-109">Members</span></span>

<span data-ttu-id="652ed-110">La clase **MicrosoftDNS \_ MXType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="652ed-110">The **MicrosoftDNS\_MXType** class has these types of members:</span></span>

-   [<span data-ttu-id="652ed-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="652ed-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="652ed-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="652ed-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="652ed-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="652ed-113">Methods</span></span>

<span data-ttu-id="652ed-114">La clase **MicrosoftDNS \_ MXType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="652ed-114">The **MicrosoftDNS\_MXType** class has these methods.</span></span>



| <span data-ttu-id="652ed-115">Método</span><span class="sxs-lookup"><span data-stu-id="652ed-115">Method</span></span>                             | <span data-ttu-id="652ed-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="652ed-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="652ed-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="652ed-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="652ed-118">Crea una instancia de un tipo MX de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida, la preferencia de registro y el nombre de host que desea que sea un intercambio de correo.</span><span class="sxs-lookup"><span data-stu-id="652ed-118">Instantiates an MX Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, record preference, and host name willing to be a mail exchange.</span></span> <span data-ttu-id="652ed-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="652ed-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="652ed-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="652ed-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="652ed-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="652ed-121">**Modify**</span></span>                         | <span data-ttu-id="652ed-122">Actualiza el TTL, la preferencia y el intercambio de correo a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="652ed-122">Updates the TTL, Preference, and Mail Exchange to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="652ed-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="652ed-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="652ed-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="652ed-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="652ed-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="652ed-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="652ed-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="652ed-126">Properties</span></span>

<span data-ttu-id="652ed-127">La clase **MicrosoftDNS \_ MXType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="652ed-127">The **MicrosoftDNS\_MXType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="652ed-128">**MailExchange**</span><span class="sxs-lookup"><span data-stu-id="652ed-128">**MailExchange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="652ed-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="652ed-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="652ed-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="652ed-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="652ed-131">FQDN que especifica un host que desea actuar como intercambio de correo electrónico para el nombre del propietario.</span><span class="sxs-lookup"><span data-stu-id="652ed-131">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="652ed-132">**Justifica**</span><span class="sxs-lookup"><span data-stu-id="652ed-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="652ed-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="652ed-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="652ed-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="652ed-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="652ed-135">Preferencia asignada a este RR entre otros en el mismo propietario.</span><span class="sxs-lookup"><span data-stu-id="652ed-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="652ed-136">Se prefieren los valores inferiores.</span><span class="sxs-lookup"><span data-stu-id="652ed-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="652ed-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="652ed-137">Requirements</span></span>



| <span data-ttu-id="652ed-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="652ed-138">Requirement</span></span> | <span data-ttu-id="652ed-139">Value</span><span class="sxs-lookup"><span data-stu-id="652ed-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="652ed-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="652ed-140">Minimum supported client</span></span><br/> | <span data-ttu-id="652ed-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="652ed-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="652ed-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="652ed-142">Minimum supported server</span></span><br/> | <span data-ttu-id="652ed-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="652ed-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="652ed-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="652ed-144">Namespace</span></span><br/>                | <span data-ttu-id="652ed-145">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="652ed-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="652ed-146">MOF</span><span class="sxs-lookup"><span data-stu-id="652ed-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="652ed-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="652ed-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="652ed-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="652ed-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="652ed-149">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MXType**</span><span class="sxs-lookup"><span data-stu-id="652ed-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="652ed-150">**Método Modify de la \_ clase MicrosoftDNS MXType**</span><span class="sxs-lookup"><span data-stu-id="652ed-150">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="652ed-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="652ed-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





