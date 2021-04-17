---
title: MicrosoftDNS_MGType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de grupo de correo (mg).
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- DNS de la clase MicrosoftDNS_MGType
- MicrosoftDNS_MGType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4772f8841977fbeae1f0bf609a65a9511bc704a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535356"
---
# <a name="microsoftdns_mgtype-class"></a><span data-ttu-id="bc542-105">MicrosoftDNS ( \_ clase MGType)</span><span class="sxs-lookup"><span data-stu-id="bc542-105">MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="bc542-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de grupo de correo (mg).</span><span class="sxs-lookup"><span data-stu-id="bc542-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Group (MG) record.</span></span>

<span data-ttu-id="bc542-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="bc542-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc542-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc542-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a><span data-ttu-id="bc542-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="bc542-109">Members</span></span>

<span data-ttu-id="bc542-110">La clase **MicrosoftDNS \_ MGType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bc542-110">The **MicrosoftDNS\_MGType** class has these types of members:</span></span>

-   [<span data-ttu-id="bc542-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="bc542-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc542-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc542-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc542-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="bc542-113">Methods</span></span>

<span data-ttu-id="bc542-114">La clase **MicrosoftDNS \_ MGType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bc542-114">The **MicrosoftDNS\_MGType** class has these methods.</span></span>



| <span data-ttu-id="bc542-115">Método</span><span class="sxs-lookup"><span data-stu-id="bc542-115">Method</span></span>                             | <span data-ttu-id="bc542-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc542-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc542-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="bc542-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="bc542-118">Este método crea una instancia de un tipo MG de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario del grupo de correo, la clase (valor predeterminado = IN), el valor de período de vida y el nombre del buzón.</span><span class="sxs-lookup"><span data-stu-id="bc542-118">This method instantiates an MG Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail group, class (default = IN), time-to-live value and the mailbox name.</span></span> <span data-ttu-id="bc542-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="bc542-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="bc542-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="bc542-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="bc542-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="bc542-121">**Modify**</span></span>                         | <span data-ttu-id="bc542-122">Este método actualiza el buzón TTL y MG a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="bc542-122">This method updates the TTL and MG Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="bc542-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="bc542-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="bc542-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="bc542-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="bc542-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="bc542-125">Qualifiers: Implemented</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="bc542-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc542-126">Properties</span></span>

<span data-ttu-id="bc542-127">La clase **MicrosoftDNS \_ MGType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bc542-127">The **MicrosoftDNS\_MGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc542-128">**MGMailbox**</span><span class="sxs-lookup"><span data-stu-id="bc542-128">**MGMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc542-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bc542-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc542-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc542-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc542-131">FQDN que especifica un buzón que es miembro del grupo de correo especificado por el nombre del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="bc542-131">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc542-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc542-132">Requirements</span></span>



| <span data-ttu-id="bc542-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc542-133">Requirement</span></span> | <span data-ttu-id="bc542-134">Value</span><span class="sxs-lookup"><span data-stu-id="bc542-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc542-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc542-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bc542-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bc542-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bc542-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc542-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bc542-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc542-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bc542-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bc542-139">Namespace</span></span><br/>                | <span data-ttu-id="bc542-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="bc542-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="bc542-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bc542-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc542-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc542-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc542-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc542-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc542-144">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MGType**</span><span class="sxs-lookup"><span data-stu-id="bc542-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="bc542-145">**Método Modify de la \_ clase MicrosoftDNS MGType**</span><span class="sxs-lookup"><span data-stu-id="bc542-145">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="bc542-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="bc542-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





