---
title: Constantes de WINBIO_BIR_DATA_FLAGS (Winbio \_ Types. h)
description: Especifique la condición de los datos.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8195cf17040c35b9e42f8977b36c5ddc6f2ea33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422615"
---
# <a name="winbio_bir_data_flags-constants"></a><span data-ttu-id="9a8f0-103">\_Constantes de \_ marcadores de datos de WINBIO Bir \_</span><span class="sxs-lookup"><span data-stu-id="9a8f0-103">WINBIO\_BIR\_DATA\_FLAGS Constants</span></span>

<span data-ttu-id="9a8f0-104">**El miembro** WINBIO de la estructura de [**\_ \_ encabezado Bir**](winbio-bir-header.md) utiliza las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="9a8f0-104">The following constants are used by the **DataFlags** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="9a8f0-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="9a8f0-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="9a8f0-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a8f0-106">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="9a8f0-107"><dt>**WINBIO \_ \_ \_ Privacidad de marca de datos**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="9a8f0-107"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>0x02</dt></span></span> </dl>                                       | <span data-ttu-id="9a8f0-108">Los datos se cifran.</span><span class="sxs-lookup"><span data-stu-id="9a8f0-108">The data is encrypted.</span></span><br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="9a8f0-109"><dt>**WINBIO \_ \_ \_ Integridad de marca de datos**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="9a8f0-109"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>0x01</dt></span></span> </dl>                                 | <span data-ttu-id="9a8f0-110">Los datos están firmados digitalmente o están protegidos por un código de autenticación de mensajes (MAC).</span><span class="sxs-lookup"><span data-stu-id="9a8f0-110">The data is digitally signed or is protected by a message authentication code (MAC).</span></span><br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="9a8f0-111"><dt>**WINBIO \_ Marca de datos \_ \_ con la firma**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="9a8f0-111"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>0x04</dt></span></span> </dl>                                          | <span data-ttu-id="9a8f0-112">Si se establece esta marca y la marca de integridad de la **\_ marca de datos \_ \_ WINBIO** , los datos se firman.</span><span class="sxs-lookup"><span data-stu-id="9a8f0-112">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="9a8f0-113">Si no se establece esta marca pero se establece la marca de integridad de la **\_ marca de datos \_ \_ WINBIO** , se calcula un equipo Mac en los datos.</span><span class="sxs-lookup"><span data-stu-id="9a8f0-113">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed on the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="9a8f0-114"><dt>**WINBIO \_ Marca de datos \_ \_ raw**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="9a8f0-114"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>0x20</dt></span></span> </dl>                                                   | <span data-ttu-id="9a8f0-115">Los datos están en el formato con el que se capturaron.</span><span class="sxs-lookup"><span data-stu-id="9a8f0-115">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="9a8f0-116"><dt>**WINBIO \_ Marca de datos \_ \_ intermedio**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="9a8f0-116"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>0x40</dt></span></span> </dl>                        | <span data-ttu-id="9a8f0-117">Los datos no son sin procesar, pero no se han procesado completamente.</span><span class="sxs-lookup"><span data-stu-id="9a8f0-117">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="9a8f0-118"><dt>**WINBIO \_ Marca de datos \_ \_ procesada**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="9a8f0-118"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>0x80</dt></span></span> </dl>                                 | <span data-ttu-id="9a8f0-119">Se han procesado los datos.</span><span class="sxs-lookup"><span data-stu-id="9a8f0-119">The data has been processed.</span></span><br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="9a8f0-120"><dt>**WINBIO \_ Máscara de opción de marca de datos \_ \_ \_ \_ presente**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="9a8f0-120"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="9a8f0-121">Máscara de la marca.</span><span class="sxs-lookup"><span data-stu-id="9a8f0-121">The flag mask.</span></span> <span data-ttu-id="9a8f0-122">Este valor siempre es uno (1).</span><span class="sxs-lookup"><span data-stu-id="9a8f0-122">This value is always one (1).</span></span><br/>                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="9a8f0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a8f0-123">Requirements</span></span>



| <span data-ttu-id="9a8f0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a8f0-124">Requirement</span></span> | <span data-ttu-id="9a8f0-125">Value</span><span class="sxs-lookup"><span data-stu-id="9a8f0-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a8f0-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a8f0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9a8f0-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a8f0-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="9a8f0-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a8f0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9a8f0-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a8f0-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9a8f0-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a8f0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a8f0-131"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a8f0-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a8f0-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a8f0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a8f0-133">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="9a8f0-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





