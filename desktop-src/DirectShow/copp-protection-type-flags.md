---
description: Las constantes siguientes se usan con el protocolo de protección de salida (COPP) certificado para los mecanismos de protección de salida específicos.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Marcas de tipo de protección COPP (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671802"
---
# <a name="copp-protection-type-flags"></a><span data-ttu-id="a33bd-103">Marcas de tipo de protección COPP</span><span class="sxs-lookup"><span data-stu-id="a33bd-103">COPP Protection Type Flags</span></span>

<span data-ttu-id="a33bd-104">Las constantes siguientes se usan con el protocolo de protección de salida (COPP) certificado para los mecanismos de protección de salida específicos.</span><span class="sxs-lookup"><span data-stu-id="a33bd-104">The follow constants are used with Certified Output Protection Protocol (COPP) to specific output protection mechanisms.</span></span>



| <span data-ttu-id="a33bd-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="a33bd-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="a33bd-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a33bd-106">Description</span></span>                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <span data-ttu-id="a33bd-107"><dt>**COPP \_ ProtectionType \_**</dt> de <dt>0x80000000</dt> desconocido</span><span class="sxs-lookup"><span data-stu-id="a33bd-107"><dt>**COPP\_ProtectionType\_Unknown**</dt> <dt>0x80000000</dt></span></span> </dl>     | <span data-ttu-id="a33bd-108">Mecanismo de protección desconocido.</span><span class="sxs-lookup"><span data-stu-id="a33bd-108">Unknown protection mechanism.</span></span><br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <span data-ttu-id="a33bd-109"><dt>**COPP \_ ProtectionType \_ None**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="a33bd-109"><dt>**COPP\_ProtectionType\_None**</dt> <dt>0x00000000</dt></span></span> </dl>                 | <span data-ttu-id="a33bd-110">Sin mecanismos de protección.</span><span class="sxs-lookup"><span data-stu-id="a33bd-110">No protection mechanisms.</span></span><br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <span data-ttu-id="a33bd-111"><dt>**COPP \_ ProtectionType \_ HDCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a33bd-111"><dt>**COPP\_ProtectionType\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="a33bd-112">High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="a33bd-112">High-Bandwidth Digital Content Protection (HDCP).</span></span><br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <span data-ttu-id="a33bd-113"><dt>**COPP \_ ProtectionType \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="a33bd-113"><dt>**COPP\_ProtectionType\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                     | <span data-ttu-id="a33bd-114">Protección de copia analógica (ACP).</span><span class="sxs-lookup"><span data-stu-id="a33bd-114">Analog Copy Protection (ACP).</span></span><br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <span data-ttu-id="a33bd-115"><dt>**COPP \_ ProtectionType \_ CGMSA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="a33bd-115"><dt>**COPP\_ProtectionType\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="a33bd-116">Copiar sistema de administración de generación analógico (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="a33bd-116">Copy Generation Management System   Analog (CGMS-A).</span></span><br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <span data-ttu-id="a33bd-117"><dt>**COPP \_ ProtectionType \_ Mask**</dt> <dt>0x80000007</dt></span><span class="sxs-lookup"><span data-stu-id="a33bd-117"><dt>**COPP\_ProtectionType\_Mask**</dt> <dt>0x80000007</dt></span></span> </dl>                 | <span data-ttu-id="a33bd-118">Máscara de máscara para aislar marcas válidas.</span><span class="sxs-lookup"><span data-stu-id="a33bd-118">Bitmask to isolate valid flags.</span></span><br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <span data-ttu-id="a33bd-119"><dt>**COPP \_ ProtectionType \_ reservado**</dt> <dt>0x7FFFFFF8</dt></span><span class="sxs-lookup"><span data-stu-id="a33bd-119"><dt>**COPP\_ProtectionType\_Reserved**</dt> <dt>0x7FFFFFF8</dt></span></span> </dl> | <span data-ttu-id="a33bd-120">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a33bd-120">Reserved.</span></span> <span data-ttu-id="a33bd-121">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a33bd-121">Must be zero.</span></span><br/>                              |



## <a name="remarks"></a><span data-ttu-id="a33bd-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a33bd-122">Remarks</span></span>

<span data-ttu-id="a33bd-123">Algunos métodos devuelven una única marca de este tipo de enumeración y algunos métodos devuelven una **o** varias de ellas.</span><span class="sxs-lookup"><span data-stu-id="a33bd-123">Some methods return a single flag from this enumeration type, and some methods return a bitwise **OR** of one or more flags.</span></span>

<span data-ttu-id="a33bd-124">Estas marcas se usan en las siguientes consultas y comandos de COPP.</span><span class="sxs-lookup"><span data-stu-id="a33bd-124">These flags are used in the following COPP queries and commands.</span></span>

-   <span data-ttu-id="a33bd-125">Nivel de protección global</span><span class="sxs-lookup"><span data-stu-id="a33bd-125">Global Protection Level</span></span>
-   <span data-ttu-id="a33bd-126">Nivel de protección local</span><span class="sxs-lookup"><span data-stu-id="a33bd-126">Local Protection Level</span></span>
-   <span data-ttu-id="a33bd-127">Tipo de protección</span><span class="sxs-lookup"><span data-stu-id="a33bd-127">Protection Type</span></span>
-   <span data-ttu-id="a33bd-128">Establecer el nivel de protección</span><span class="sxs-lookup"><span data-stu-id="a33bd-128">Set Protection Level</span></span>

## <a name="requirements"></a><span data-ttu-id="a33bd-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a33bd-129">Requirements</span></span>



| <span data-ttu-id="a33bd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33bd-130">Requirement</span></span> | <span data-ttu-id="a33bd-131">Value</span><span class="sxs-lookup"><span data-stu-id="a33bd-131">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a33bd-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a33bd-132">Header</span></span><br/> | <dl> <span data-ttu-id="a33bd-133"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a33bd-133"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a33bd-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a33bd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33bd-135">Constantes y GUID</span><span class="sxs-lookup"><span data-stu-id="a33bd-135">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="a33bd-136">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="a33bd-136">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




