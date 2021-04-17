---
description: Define el formato de un archivo que contiene información de certificados.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: Enumeración CAPICOM_CERTIFICATES_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 3cbde0e8a64fa931ce50d2277d33b5fd5c27ee68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670854"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a><span data-ttu-id="8839d-103">La \_ \_ enumeración de los certificados de CAPICOM se guardan \_ como \_ tipo</span><span class="sxs-lookup"><span data-stu-id="8839d-103">CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="8839d-104">El tipo de enumeración de los **certificados de CAPICOM \_ \_ Save \_ as \_** define el formato de un archivo que contiene información de certificados.</span><span class="sxs-lookup"><span data-stu-id="8839d-104">The **CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificates information.</span></span> <span data-ttu-id="8839d-105">CAPICOM 2,0 presentó este tipo de enumeración.</span><span class="sxs-lookup"><span data-stu-id="8839d-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="8839d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8839d-106">Members</span></span>



| <span data-ttu-id="8839d-107">Miembro</span><span class="sxs-lookup"><span data-stu-id="8839d-107">Member</span></span>                                          | <span data-ttu-id="8839d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8839d-108">Description</span></span>                                          | <span data-ttu-id="8839d-109">Value</span><span class="sxs-lookup"><span data-stu-id="8839d-109">Value</span></span> |
|-------------------------------------------------|------------------------------------------------------|-------|
| <span data-ttu-id="8839d-110">**los \_ certificados \_ de CAPICOM se guardan \_ como \_ serializados**</span><span class="sxs-lookup"><span data-stu-id="8839d-110">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</span></span> | <span data-ttu-id="8839d-111">Los certificados guardados se serializan.</span><span class="sxs-lookup"><span data-stu-id="8839d-111">The saved certificates are serialized.</span></span><br/>    | <span data-ttu-id="8839d-112">0</span><span class="sxs-lookup"><span data-stu-id="8839d-112">0</span></span>     |
| <span data-ttu-id="8839d-113">**Los \_ certificados \_ de CAPICOM se guardan \_ como \_ pkcs7**</span><span class="sxs-lookup"><span data-stu-id="8839d-113">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</span></span>      | <span data-ttu-id="8839d-114">Los certificados se guardan como PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="8839d-114">The certificates are saved as a PKCS \#7.</span></span><br/> | <span data-ttu-id="8839d-115">1</span><span class="sxs-lookup"><span data-stu-id="8839d-115">1</span></span>     |
| <span data-ttu-id="8839d-116">**los \_ certificados \_ de CAPICOM se guardan \_ como \_ pfx**</span><span class="sxs-lookup"><span data-stu-id="8839d-116">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</span></span>        | <span data-ttu-id="8839d-117">Los certificados se guardan como un archivo PFX.</span><span class="sxs-lookup"><span data-stu-id="8839d-117">The certificates are saved as a PFX.</span></span><br/>      | <span data-ttu-id="8839d-118">2</span><span class="sxs-lookup"><span data-stu-id="8839d-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="8839d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8839d-119">Remarks</span></span>

<span data-ttu-id="8839d-120">El método de los certificados \_ \_ \_ \_ [**. Save**](certificates-save.md) usa el tipo de enumeración de tipo guardar certificados de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="8839d-120">The CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration type is used by the [**Certificates.Save**](certificates-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8839d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8839d-121">Requirements</span></span>



| <span data-ttu-id="8839d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8839d-122">Requirement</span></span> | <span data-ttu-id="8839d-123">Value</span><span class="sxs-lookup"><span data-stu-id="8839d-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8839d-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="8839d-124">Redistributable</span></span><br/> | <span data-ttu-id="8839d-125">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="8839d-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="8839d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8839d-126">Header</span></span><br/>          | <dl> <span data-ttu-id="8839d-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="8839d-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




