---
title: Método Modify de la clase MicrosoftDNS_ATMAType
description: El método Modify actualiza un registro de recursos de dirección ATM a nombre (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_ATMAType clase
- MicrosoftDNS_ATMAType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079384"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="f59a3-106">Método Modify de la \_ clase MicrosoftDNS ATMAType</span><span class="sxs-lookup"><span data-stu-id="f59a3-106">Modify method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="f59a3-107">El método **Modify** actualiza un registro de recursos de dirección ATM a nombre (Atma).</span><span class="sxs-lookup"><span data-stu-id="f59a3-107">The **Modify** method updates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f59a3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f59a3-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f59a3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f59a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f59a3-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f59a3-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f59a3-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="f59a3-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f59a3-112">*Formato* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f59a3-112">*Format* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f59a3-113">Formato de dirección ATM.</span><span class="sxs-lookup"><span data-stu-id="f59a3-113">ATM address format.</span></span> <span data-ttu-id="f59a3-114">Dos valores posibles para FORMAT son: 0, que indica el formato de dirección del sistema de finalización (AESA) de ATM y 1 que indica el formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="f59a3-114">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="f59a3-115">*ATMAddress* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f59a3-115">*ATMAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f59a3-116">Cadena de longitud variable de octetos que contiene la dirección ATM del nodo/propietario al que pertenece este RR.</span><span class="sxs-lookup"><span data-stu-id="f59a3-116">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="f59a3-117">Los primeros cuatro bytes de la matriz se utilizan para almacenar el tamaño de la cadena de octeto.</span><span class="sxs-lookup"><span data-stu-id="f59a3-117">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="f59a3-118">El byte más significativo se almacena en byte 0.</span><span class="sxs-lookup"><span data-stu-id="f59a3-118">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="f59a3-119">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f59a3-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f59a3-120">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="f59a3-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f59a3-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f59a3-121">Return value</span></span>

<span data-ttu-id="f59a3-122">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f59a3-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f59a3-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f59a3-123">Remarks</span></span>

<span data-ttu-id="f59a3-124">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="f59a3-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="f59a3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f59a3-125">Requirements</span></span>



| <span data-ttu-id="f59a3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f59a3-126">Requirement</span></span> | <span data-ttu-id="f59a3-127">Value</span><span class="sxs-lookup"><span data-stu-id="f59a3-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f59a3-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f59a3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f59a3-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f59a3-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f59a3-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f59a3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f59a3-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f59a3-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f59a3-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f59a3-132">Namespace</span></span><br/>                | <span data-ttu-id="f59a3-133">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="f59a3-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f59a3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f59a3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f59a3-135"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f59a3-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f59a3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f59a3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f59a3-137">**MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="f59a3-137">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="f59a3-138">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS ATMAType**</span><span class="sxs-lookup"><span data-stu-id="f59a3-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f59a3-139">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="f59a3-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





