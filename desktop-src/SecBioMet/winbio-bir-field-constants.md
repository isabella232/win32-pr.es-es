---
title: Constantes de WINBIO_BIR_FIELD (Winbio \_ Types. h)
description: Especifique una máscara de máscara.
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104710f1686f13227fbe65782c2baf9c13149650
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359744"
---
# <a name="winbio_bir_field-constants"></a><span data-ttu-id="cdc70-103">WINBIO \_ \_ constantes de campo Bir</span><span class="sxs-lookup"><span data-stu-id="cdc70-103">WINBIO\_BIR\_FIELD Constants</span></span>

<span data-ttu-id="cdc70-104">Las constantes siguientes se usan para crear una máscara de máscara para el miembro **ValidFields** de la estructura de [**\_ \_ encabezado Bir de WINBIO**](winbio-bir-header.md) .</span><span class="sxs-lookup"><span data-stu-id="cdc70-104">The following constants are used to create a bitmask for the **ValidFields** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="cdc70-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="cdc70-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="cdc70-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdc70-106">Description</span></span>                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <span data-ttu-id="cdc70-107"><dt>**WINBIO \_ Recuento de \_ \_ subencabezados \_ de campo Bir**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-107"><dt>**WINBIO\_BIR\_FIELD\_SUBHEAD\_COUNT**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="cdc70-108">Proporcionado para la conformidad con NISTIR 6529-A, el marco de trabajo de formatos biométricos (CBEFF) de los empleados es el formato A, pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="cdc70-108">Provided for conformity with NISTIR 6529-A, the Common Biometric Exchange Formats Framework (CBEFF) Patron Format A, but not used.</span></span><br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <span data-ttu-id="cdc70-109"><dt>**WINBIO \_ \_ \_ \_ ID. de producto de campo Bir**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-109"><dt>**WINBIO\_BIR\_FIELD\_PRODUCT\_ID**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="cdc70-110">El miembro **ProductID** es válido.</span><span class="sxs-lookup"><span data-stu-id="cdc70-110">The **ProductId** member is valid.</span></span><br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <span data-ttu-id="cdc70-111"><dt>**WINBIO \_ BIR \_ campo \_ \_ ID**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-111"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_ID**</dt> <dt>0x0004</dt></span></span> </dl>                                      | <span data-ttu-id="cdc70-112">Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="cdc70-112">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <span data-ttu-id="cdc70-113"><dt>**WINBIO \_ BIR \_ \_ Índice de campo**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-113"><dt>**WINBIO\_BIR\_FIELD\_INDEX**</dt> <dt>0x0008</dt></span></span> </dl>                                                   | <span data-ttu-id="cdc70-114">Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="cdc70-114">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <span data-ttu-id="cdc70-115"><dt>**WINBIO \_ BIR \_ \_ \_ fecha de creación de campos**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-115"><dt>**WINBIO\_BIR\_FIELD\_CREATION\_DATE**</dt> <dt>0x0010</dt></span></span> </dl>                          | <span data-ttu-id="cdc70-116">El miembro **CreationDate** es válido.</span><span class="sxs-lookup"><span data-stu-id="cdc70-116">The **CreationDate** member is valid.</span></span><br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <span data-ttu-id="cdc70-117"><dt>**WINBIO \_ BIR \_ \_ \_ período de validez del campo**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-117"><dt>**WINBIO\_BIR\_FIELD\_VALIDITY\_PERIOD**</dt> <dt>0x0020</dt></span></span> </dl>                    | <span data-ttu-id="cdc70-118">El miembro **ValidityPeriod** es válido.</span><span class="sxs-lookup"><span data-stu-id="cdc70-118">The **ValidityPeriod** member is valid.</span></span><br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <span data-ttu-id="cdc70-119"><dt>**WINBIO \_ \_ \_ \_ Tipo biométrico de campo Bir**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-119"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_TYPE**</dt> <dt>0x0040</dt></span></span> </dl>                       | <span data-ttu-id="cdc70-120">El miembro de **tipo** es válido.</span><span class="sxs-lookup"><span data-stu-id="cdc70-120">The **Type** member is valid.</span></span><br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <span data-ttu-id="cdc70-121"><dt>**WINBIO \_ BIR \_ campo \_ biométrico \_**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-121"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_SUBTYPE**</dt> <dt>0x0080</dt></span></span> </dl>              | <span data-ttu-id="cdc70-122">El miembro del **subtipo** es válido.</span><span class="sxs-lookup"><span data-stu-id="cdc70-122">The **Subtype** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <span data-ttu-id="cdc70-123"><dt>**WINBIO \_ BIR \_ campo \_ CBEFF \_ \_ versión de encabezado**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-123"><dt>**WINBIO\_BIR\_FIELD\_CBEFF\_HEADER\_VERSION**</dt> <dt>0x0100</dt></span></span> </dl>    | <span data-ttu-id="cdc70-124">El miembro **HeaderVersion** es válido.</span><span class="sxs-lookup"><span data-stu-id="cdc70-124">The **HeaderVersion** member is valid.</span></span><br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <span data-ttu-id="cdc70-125"><dt>**WINBIO \_ BIR \_ campo de la \_ \_ \_ versión de encabezado**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-125"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_HEADER\_VERSION**</dt> <dt>0x0200</dt></span></span> </dl> | <span data-ttu-id="cdc70-126">El miembro **PatronHeaderVersion** es válido.</span><span class="sxs-lookup"><span data-stu-id="cdc70-126">The **PatronHeaderVersion** member is valid.</span></span><br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <span data-ttu-id="cdc70-127"><dt>**WINBIO \_ BIR \_ de \_ \_ uso biométrico de campo**</dt> <dt>0x0400</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-127"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_PURPOSE**</dt> <dt>0x0400</dt></span></span> </dl>              | <span data-ttu-id="cdc70-128">El miembro **purpose** es válido.</span><span class="sxs-lookup"><span data-stu-id="cdc70-128">The **Purpose** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <span data-ttu-id="cdc70-129"><dt>**WINBIO \_ BIR \_ \_ \_ condición biométrica de campo**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-129"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_CONDITION**</dt> <dt>0x0800</dt></span></span> </dl>        | <span data-ttu-id="cdc70-130">Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="cdc70-130">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <span data-ttu-id="cdc70-131"><dt>**WINBIO \_ \_ \_ Calidad de campo Bir**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-131"><dt>**WINBIO\_BIR\_FIELD\_QUALITY**</dt> <dt>0x1000</dt></span></span> </dl>                                             | <span data-ttu-id="cdc70-132">El miembro de calidad de la **cualidad** es válido.</span><span class="sxs-lookup"><span data-stu-id="cdc70-132">The **DataQuality** member is valid.</span></span><br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <span data-ttu-id="cdc70-133"><dt>**WINBIO \_ \_ \_ Creador del campo Bir**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-133"><dt>**WINBIO\_BIR\_FIELD\_CREATOR**</dt> <dt>0x2000</dt></span></span> </dl>                                             | <span data-ttu-id="cdc70-134">Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="cdc70-134">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <span data-ttu-id="cdc70-135"><dt>**WINBIO \_ \_ \_ Desafío de campo Bir**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-135"><dt>**WINBIO\_BIR\_FIELD\_CHALLENGE**</dt> <dt>0x4000</dt></span></span> </dl>                                       | <span data-ttu-id="cdc70-136">Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="cdc70-136">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <span data-ttu-id="cdc70-137"><dt>**WINBIO \_ \_ \_ Carga de campo Bir**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-137"><dt>**WINBIO\_BIR\_FIELD\_PAYLOAD**</dt> <dt>0x8000</dt></span></span> </dl>                                             | <span data-ttu-id="cdc70-138">Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="cdc70-138">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="cdc70-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdc70-139">Requirements</span></span>



| <span data-ttu-id="cdc70-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdc70-140">Requirement</span></span> | <span data-ttu-id="cdc70-141">Value</span><span class="sxs-lookup"><span data-stu-id="cdc70-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc70-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdc70-142">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc70-143">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="cdc70-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="cdc70-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdc70-144">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc70-145">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cdc70-145">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cdc70-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdc70-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc70-147"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc70-147"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdc70-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdc70-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc70-149">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="cdc70-149">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





