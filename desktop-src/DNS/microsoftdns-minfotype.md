---
title: MicrosoftDNS_MINFOType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de información de correo (MINFO).
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- DNS de la clase MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7d230db9da32ce47cd4cfaf99c4978c4e63385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151038"
---
# <a name="microsoftdns_minfotype-class"></a><span data-ttu-id="17bf6-105">MicrosoftDNS ( \_ clase MINFOType)</span><span class="sxs-lookup"><span data-stu-id="17bf6-105">MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="17bf6-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de información de correo (MINFO).</span><span class="sxs-lookup"><span data-stu-id="17bf6-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Information (MINFO) record.</span></span>

<span data-ttu-id="17bf6-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="17bf6-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="17bf6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17bf6-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a><span data-ttu-id="17bf6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="17bf6-109">Members</span></span>

<span data-ttu-id="17bf6-110">La clase **MicrosoftDNS \_ MINFOType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="17bf6-110">The **MicrosoftDNS\_MINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="17bf6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="17bf6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="17bf6-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17bf6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="17bf6-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="17bf6-113">Methods</span></span>

<span data-ttu-id="17bf6-114">La clase **MicrosoftDNS \_ MINFOType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="17bf6-114">The **MicrosoftDNS\_MINFOType** class has these methods.</span></span>



| <span data-ttu-id="17bf6-115">Método</span><span class="sxs-lookup"><span data-stu-id="17bf6-115">Method</span></span>                             | <span data-ttu-id="17bf6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="17bf6-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17bf6-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="17bf6-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="17bf6-118">Crea una instancia de un tipo MINFO de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario de la lista o el cuadro de correo, la clase (valor predeterminado = IN), el valor de período de vida y los buzones responsables y de errores.</span><span class="sxs-lookup"><span data-stu-id="17bf6-118">Instantiates an MINFO Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail list/box, class (default = IN), time-to-live value and the responsible and error mailboxes.</span></span> <span data-ttu-id="17bf6-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="17bf6-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="17bf6-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="17bf6-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="17bf6-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="17bf6-121">**Modify**</span></span>                         | <span data-ttu-id="17bf6-122">Este método actualiza el TTL, el buzón responsable y el buzón de error a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="17bf6-122">This method updates the TTL, Responsible Mailbox, and Error Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="17bf6-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="17bf6-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="17bf6-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="17bf6-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="17bf6-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="17bf6-125">Qualifiers: Implemented</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="17bf6-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17bf6-126">Properties</span></span>

<span data-ttu-id="17bf6-127">La clase **MicrosoftDNS \_ MINFOType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="17bf6-127">The **MicrosoftDNS\_MINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17bf6-128">**ErrorMailbox**</span><span class="sxs-lookup"><span data-stu-id="17bf6-128">**ErrorMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17bf6-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17bf6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17bf6-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17bf6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17bf6-131">FQDN que especifica un buzón para recibir mensajes de error relacionados con la lista de distribución de correo o con el buzón especificado por el nombre del propietario del registro MINFO.</span><span class="sxs-lookup"><span data-stu-id="17bf6-131">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="17bf6-132">**ResponsibleMailbox**</span><span class="sxs-lookup"><span data-stu-id="17bf6-132">**ResponsibleMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17bf6-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17bf6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17bf6-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17bf6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17bf6-135">FQDN que especifica un buzón responsable de la lista de distribución de correo o el buzón especificado en el nombre del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="17bf6-135">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17bf6-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17bf6-136">Requirements</span></span>



| <span data-ttu-id="17bf6-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="17bf6-137">Requirement</span></span> | <span data-ttu-id="17bf6-138">Value</span><span class="sxs-lookup"><span data-stu-id="17bf6-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17bf6-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17bf6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="17bf6-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="17bf6-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="17bf6-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17bf6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="17bf6-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="17bf6-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="17bf6-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17bf6-143">Namespace</span></span><br/>                | <span data-ttu-id="17bf6-144">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="17bf6-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="17bf6-145">MOF</span><span class="sxs-lookup"><span data-stu-id="17bf6-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17bf6-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17bf6-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17bf6-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="17bf6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17bf6-148">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MINFOType**</span><span class="sxs-lookup"><span data-stu-id="17bf6-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="17bf6-149">**Método Modify de la \_ clase MicrosoftDNS MINFOType**</span><span class="sxs-lookup"><span data-stu-id="17bf6-149">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="17bf6-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="17bf6-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





