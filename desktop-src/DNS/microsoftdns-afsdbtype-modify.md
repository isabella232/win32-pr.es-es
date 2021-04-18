---
title: Método Modify de la clase MicrosoftDNS_AFSDBType
description: El método Modify actualiza un registro de recursos de servidor de base de datos del sistema de archivos (AFSDB) Andrew.
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_AFSDBType clase
- MicrosoftDNS_AFSDBType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658180"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="215af-106">Método Modify de la \_ clase MicrosoftDNS AFSDBType</span><span class="sxs-lookup"><span data-stu-id="215af-106">Modify method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="215af-107">El método **Modify** actualiza un registro de recursos de servidor de base de datos del sistema de archivos (AFSDB) Andrew.</span><span class="sxs-lookup"><span data-stu-id="215af-107">The **Modify** method updates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="215af-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="215af-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="215af-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="215af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="215af-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="215af-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="215af-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="215af-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="215af-112">*Subtipo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="215af-112">*Subtype* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="215af-113">Subtipo del servidor AFS del host.</span><span class="sxs-lookup"><span data-stu-id="215af-113">Subtype of the host AFS server.</span></span> <span data-ttu-id="215af-114">Para el subtipo 1 (valor = 1), el host tiene un servidor de ubicación del volumen AFS versión 3,0 para la celda AFS con nombre.</span><span class="sxs-lookup"><span data-stu-id="215af-114">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="215af-115">En el caso del subtipo 2 (valor = 2), el host tiene un servidor de nombres autenticado que contiene el nodo del directorio raíz de la celda para la celda de DCE/NCA con nombre.</span><span class="sxs-lookup"><span data-stu-id="215af-115">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="215af-116">*NombreDeServidor* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="215af-116">*ServerName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="215af-117">FQDN que especifica un host que tiene un servidor para la celda AFS especificada en el nombre del propietario.</span><span class="sxs-lookup"><span data-stu-id="215af-117">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="215af-118">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="215af-118">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="215af-119">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="215af-119">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="215af-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="215af-120">Return value</span></span>

<span data-ttu-id="215af-121">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="215af-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="215af-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="215af-122">Remarks</span></span>

<span data-ttu-id="215af-123">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="215af-123">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="215af-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="215af-124">Requirements</span></span>



| <span data-ttu-id="215af-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="215af-125">Requirement</span></span> | <span data-ttu-id="215af-126">Value</span><span class="sxs-lookup"><span data-stu-id="215af-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="215af-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="215af-127">Minimum supported client</span></span><br/> | <span data-ttu-id="215af-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="215af-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="215af-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="215af-129">Minimum supported server</span></span><br/> | <span data-ttu-id="215af-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="215af-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="215af-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="215af-131">Namespace</span></span><br/>                | <span data-ttu-id="215af-132">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="215af-132">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="215af-133">MOF</span><span class="sxs-lookup"><span data-stu-id="215af-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="215af-134"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="215af-134"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="215af-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="215af-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="215af-136">**MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="215af-136">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="215af-137">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="215af-137">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="215af-138">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="215af-138">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





