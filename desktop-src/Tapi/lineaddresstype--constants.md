---
description: El tipo de dirección identifica el formato de la dirección, como el número de teléfono estándar o la dirección de correo electrónico. Solo las aplicaciones que negocien la versión 3,0 o posterior de TAPI pueden utilizar tipos de direcciones.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: Constantes de LINEADDRESSTYPE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0a46eff2a7a0c38fa17aed4b831ef8701c565
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679516"
---
# <a name="lineaddresstype_-constants"></a><span data-ttu-id="97772-104">Constantes de LINEADDRESSTYPE \_</span><span class="sxs-lookup"><span data-stu-id="97772-104">LINEADDRESSTYPE\_ Constants</span></span>

<span data-ttu-id="97772-105">El tipo de dirección identifica el formato de la dirección, como el número de teléfono estándar o la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="97772-105">The address type identifies address format, such as standard phone number or e-mail address.</span></span> <span data-ttu-id="97772-106">Solo las aplicaciones que negocien la versión 3,0 o posterior de TAPI pueden utilizar tipos de direcciones.</span><span class="sxs-lookup"><span data-stu-id="97772-106">Only applications that negotiate TAPI version 3.0 or higher can use address types.</span></span>

<dl> <dt>

<span data-ttu-id="97772-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE \_ PHONENUMBER**</span><span class="sxs-lookup"><span data-stu-id="97772-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE\_PHONENUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97772-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="97772-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="97772-109">El tipo de dirección es un número de teléfono estándar.</span><span class="sxs-lookup"><span data-stu-id="97772-109">Address type is a standard phone number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97772-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE \_ SDP**</span><span class="sxs-lookup"><span data-stu-id="97772-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE\_SDP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97772-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="97772-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="97772-112">El tipo de dirección es Conferencia del Protocolo de descripción de la sesión (SDP).</span><span class="sxs-lookup"><span data-stu-id="97772-112">Address type is Session Description Protocol (SDP) conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97772-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EMAILNAME**</span><span class="sxs-lookup"><span data-stu-id="97772-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE\_EMAILNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97772-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="97772-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="97772-115">El tipo de dirección es un nombre de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="97772-115">Address type is an e-mail name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97772-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ domainname**</span><span class="sxs-lookup"><span data-stu-id="97772-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97772-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="97772-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="97772-118">El tipo de dirección es un nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="97772-118">Address type is a domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97772-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="97772-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE\_IPADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97772-120">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97772-120">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="97772-121">El tipo de dirección es una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="97772-121">Address type is an IP address.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97772-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97772-122">Requirements</span></span>



| <span data-ttu-id="97772-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="97772-123">Requirement</span></span> | <span data-ttu-id="97772-124">Value</span><span class="sxs-lookup"><span data-stu-id="97772-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="97772-125">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="97772-125">TAPI version</span></span><br/> | <span data-ttu-id="97772-126">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="97772-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="97772-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97772-127">Header</span></span><br/>       | <dl> <span data-ttu-id="97772-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="97772-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




