---
description: Define qué certificados de una cadena se guardan.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: Enumeración CAPICOM_CERTIFICATE_INCLUDE_OPTION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671133"
---
# <a name="capicom_certificate_include_option-enumeration"></a><span data-ttu-id="bac21-103">\_ \_ Enumeración de opciones de inclusión de certificado de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="bac21-103">CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION enumeration</span></span>

<span data-ttu-id="bac21-104">El tipo de enumeración de la **\_ \_ \_ opción incluir certificado de CAPICOM** define qué certificados de una cadena se guardan.</span><span class="sxs-lookup"><span data-stu-id="bac21-104">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type defines which certificates in a chain are saved.</span></span> <span data-ttu-id="bac21-105">Este tipo de enumeración se presentó en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="bac21-105">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="bac21-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bac21-106">Members</span></span>



| <span data-ttu-id="bac21-107">Miembro</span><span class="sxs-lookup"><span data-stu-id="bac21-107">Member</span></span>                                                 | <span data-ttu-id="bac21-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bac21-108">Description</span></span>                                                                           | <span data-ttu-id="bac21-109">Value</span><span class="sxs-lookup"><span data-stu-id="bac21-109">Value</span></span> |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="bac21-110">**el \_ certificado de CAPICOM \_ incluye una \_ cadena excepto la \_ \_ raíz**</span><span class="sxs-lookup"><span data-stu-id="bac21-110">**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</span></span> | <span data-ttu-id="bac21-111">Guarda todos los certificados de la cadena con la excepción de la entidad raíz.</span><span class="sxs-lookup"><span data-stu-id="bac21-111">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> | <span data-ttu-id="bac21-112">0</span><span class="sxs-lookup"><span data-stu-id="bac21-112">0</span></span>     |
| <span data-ttu-id="bac21-113">**el \_ certificado de CAPICOM \_ incluye una \_ \_ cadena entera**</span><span class="sxs-lookup"><span data-stu-id="bac21-113">**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</span></span>        | <span data-ttu-id="bac21-114">Guarda la cadena de certificados completa.</span><span class="sxs-lookup"><span data-stu-id="bac21-114">Saves the complete certificate chain.</span></span><br/>                                      | <span data-ttu-id="bac21-115">1</span><span class="sxs-lookup"><span data-stu-id="bac21-115">1</span></span>     |
| <span data-ttu-id="bac21-116">**el \_ certificado de CAPICOM \_ incluye \_ \_ solo la entidad final \_**</span><span class="sxs-lookup"><span data-stu-id="bac21-116">**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</span></span>   | <span data-ttu-id="bac21-117">Guarda solo el certificado de entidad final.</span><span class="sxs-lookup"><span data-stu-id="bac21-117">Saves only the end entity certificate.</span></span><br/>                                     | <span data-ttu-id="bac21-118">2</span><span class="sxs-lookup"><span data-stu-id="bac21-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="bac21-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bac21-119">Remarks</span></span>

<span data-ttu-id="bac21-120">El método [**Certificate. Save**](certificate-save.md) usa el tipo de enumeración de la **\_ opción de \_ inclusión \_ de certificado CAPICOM** .</span><span class="sxs-lookup"><span data-stu-id="bac21-120">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bac21-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bac21-121">Requirements</span></span>



| <span data-ttu-id="bac21-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bac21-122">Requirement</span></span> | <span data-ttu-id="bac21-123">Value</span><span class="sxs-lookup"><span data-stu-id="bac21-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bac21-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="bac21-124">Redistributable</span></span><br/> | <span data-ttu-id="bac21-125">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="bac21-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="bac21-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bac21-126">Header</span></span><br/>          | <dl> <span data-ttu-id="bac21-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="bac21-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




