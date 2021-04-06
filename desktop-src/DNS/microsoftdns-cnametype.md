---
title: MicrosoftDNS_CNAMEType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de nombre canónico (CNAME).
ms.assetid: 93a972e3-abb1-425f-beb7-32abe7d0b485
keywords:
- DNS de la clase MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
- MicrosoftDNS_CNAMEType.Modify
- MicrosoftDNS_CNAMEType.PrimaryName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dca8729c2c750e1cef774b5f0f3eadc3e2f6fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905254"
---
# <a name="microsoftdns_cnametype-class"></a><span data-ttu-id="24d47-105">MicrosoftDNS ( \_ clase CNAMEType)</span><span class="sxs-lookup"><span data-stu-id="24d47-105">MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="24d47-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de nombre canónico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="24d47-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Canonical Name (CNAME) record.</span></span>

<span data-ttu-id="24d47-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="24d47-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="24d47-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24d47-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_CNAMEType : MicrosoftDNS_ResourceRecord
{
  string PrimaryName;
};
```

## <a name="members"></a><span data-ttu-id="24d47-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="24d47-109">Members</span></span>

<span data-ttu-id="24d47-110">La clase **MicrosoftDNS \_ CNAMEType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="24d47-110">The **MicrosoftDNS\_CNAMEType** class has these types of members:</span></span>

-   [<span data-ttu-id="24d47-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="24d47-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="24d47-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24d47-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="24d47-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="24d47-113">Methods</span></span>

<span data-ttu-id="24d47-114">La clase **MicrosoftDNS \_ CNAMEType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="24d47-114">The **MicrosoftDNS\_CNAMEType** class has these methods.</span></span>



| <span data-ttu-id="24d47-115">Método</span><span class="sxs-lookup"><span data-stu-id="24d47-115">Method</span></span>                             | <span data-ttu-id="24d47-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="24d47-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24d47-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="24d47-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="24d47-118">Crea una instancia de un registro de recursos CNAME basado en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y el nombre principal del registro CNAME.</span><span class="sxs-lookup"><span data-stu-id="24d47-118">Instantiates a CNAME Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the primary name of the CNAME record.</span></span> <span data-ttu-id="24d47-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="24d47-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="24d47-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="24d47-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="24d47-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="24d47-121">**Modify**</span></span>                         | <span data-ttu-id="24d47-122">Actualiza el TTL y el nombre principal a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="24d47-122">Updates the TTL and Primary Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="24d47-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="24d47-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="24d47-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="24d47-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="24d47-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="24d47-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="24d47-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24d47-126">Properties</span></span>

<span data-ttu-id="24d47-127">La clase **MicrosoftDNS \_ CNAMEType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="24d47-127">The **MicrosoftDNS\_CNAMEType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24d47-128">**PrimaryName**</span><span class="sxs-lookup"><span data-stu-id="24d47-128">**PrimaryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24d47-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="24d47-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24d47-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="24d47-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24d47-131">Nombre canónico o principal del propietario del registro CNAME.</span><span class="sxs-lookup"><span data-stu-id="24d47-131">Canonical, or primary name for the owner of the CNAME record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24d47-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24d47-132">Requirements</span></span>



| <span data-ttu-id="24d47-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="24d47-133">Requirement</span></span> | <span data-ttu-id="24d47-134">Value</span><span class="sxs-lookup"><span data-stu-id="24d47-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24d47-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24d47-135">Minimum supported client</span></span><br/> | <span data-ttu-id="24d47-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="24d47-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="24d47-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24d47-137">Minimum supported server</span></span><br/> | <span data-ttu-id="24d47-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="24d47-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="24d47-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24d47-139">Namespace</span></span><br/>                | <span data-ttu-id="24d47-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="24d47-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="24d47-141">MOF</span><span class="sxs-lookup"><span data-stu-id="24d47-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24d47-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24d47-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24d47-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="24d47-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24d47-144">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="24d47-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="24d47-145">**Método Modify de la \_ clase MicrosoftDNS CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="24d47-145">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="24d47-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="24d47-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





