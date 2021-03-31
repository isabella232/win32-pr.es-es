---
title: MicrosoftDNS_AFSDBType (clase)
description: Subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de servidor de base de datos del sistema de archivos (AFSDB) Andrew.
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- DNS de la clase MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 836de50f4da9e613fb3e940b90971f38a634c804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079388"
---
# <a name="microsoftdns_afsdbtype-class"></a><span data-ttu-id="e17ed-105">MicrosoftDNS ( \_ clase AFSDBType)</span><span class="sxs-lookup"><span data-stu-id="e17ed-105">MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="e17ed-106">Subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de servidor de base de datos del sistema de archivos (AFSDB) Andrew.</span><span class="sxs-lookup"><span data-stu-id="e17ed-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an Andrew File System Database Server (AFSDB) record.</span></span>

<span data-ttu-id="e17ed-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="e17ed-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e17ed-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e17ed-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a><span data-ttu-id="e17ed-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e17ed-109">Members</span></span>

<span data-ttu-id="e17ed-110">La clase **MicrosoftDNS \_ AFSDBType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e17ed-110">The **MicrosoftDNS\_AFSDBType** class has these types of members:</span></span>

-   [<span data-ttu-id="e17ed-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e17ed-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e17ed-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e17ed-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e17ed-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="e17ed-113">Methods</span></span>

<span data-ttu-id="e17ed-114">La clase **MicrosoftDNS \_ AFSDBType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e17ed-114">The **MicrosoftDNS\_AFSDBType** class has these methods.</span></span>



| <span data-ttu-id="e17ed-115">Método</span><span class="sxs-lookup"><span data-stu-id="e17ed-115">Method</span></span>                             | <span data-ttu-id="e17ed-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e17ed-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e17ed-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e17ed-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="e17ed-118">Crea una instancia de un registro de recursos AFSDB basado en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario o la celda, la clase (valor predeterminado = IN), el valor de período de vida y el subtipo y nombre del servidor AFS del host.</span><span class="sxs-lookup"><span data-stu-id="e17ed-118">Instantiates an AFSDB Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Cell Name, class (default = IN), time-to-live value, and host AFS server subtype and name.</span></span> <span data-ttu-id="e17ed-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="e17ed-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="e17ed-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="e17ed-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="e17ed-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="e17ed-121">**Modify**</span></span>                         | <span data-ttu-id="e17ed-122">Este método actualiza el TTL, el subtipo y el nombre del servidor a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="e17ed-122">This method updates the TTL, Subtype and Server Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="e17ed-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="e17ed-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="e17ed-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="e17ed-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="e17ed-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="e17ed-125">Qualifiers: Implemented</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="e17ed-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e17ed-126">Properties</span></span>

<span data-ttu-id="e17ed-127">La clase **MicrosoftDNS \_ AFSDBType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e17ed-127">The **MicrosoftDNS\_AFSDBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e17ed-128">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="e17ed-128">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17ed-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e17ed-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17ed-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e17ed-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e17ed-131">FQDN que especifica un host que tiene un servidor para la celda AFS especificada en el nombre del propietario.</span><span class="sxs-lookup"><span data-stu-id="e17ed-131">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="e17ed-132">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="e17ed-132">**Subtype**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17ed-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e17ed-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e17ed-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e17ed-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e17ed-135">Subtipo del servidor AFS del host.</span><span class="sxs-lookup"><span data-stu-id="e17ed-135">Subtype of the host AFS server.</span></span> <span data-ttu-id="e17ed-136">Para el subtipo 1 (valor = 1), el host tiene un servidor de ubicación del volumen AFS versión 3,0 para la celda AFS con nombre.</span><span class="sxs-lookup"><span data-stu-id="e17ed-136">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="e17ed-137">En el caso del subtipo 2 (valor = 2), el host tiene un servidor de nombres autenticado que contiene el nodo del directorio raíz de la celda para la celda de DCE/NCA con nombre.</span><span class="sxs-lookup"><span data-stu-id="e17ed-137">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e17ed-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e17ed-138">Requirements</span></span>



| <span data-ttu-id="e17ed-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e17ed-139">Requirement</span></span> | <span data-ttu-id="e17ed-140">Value</span><span class="sxs-lookup"><span data-stu-id="e17ed-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e17ed-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e17ed-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e17ed-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e17ed-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e17ed-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e17ed-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e17ed-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e17ed-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e17ed-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e17ed-145">Namespace</span></span><br/>                | <span data-ttu-id="e17ed-146">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="e17ed-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e17ed-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e17ed-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e17ed-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e17ed-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e17ed-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="e17ed-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e17ed-150">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="e17ed-150">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e17ed-151">**Método Modify de la \_ clase MicrosoftDNS AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="e17ed-151">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="e17ed-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="e17ed-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





