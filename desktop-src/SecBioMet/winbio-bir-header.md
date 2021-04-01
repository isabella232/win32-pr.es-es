---
title: Estructura de WINBIO_BIR_HEADER (Winbio \_ Types. h)
description: Contiene el encabezado de un registro de información biométrica (BIR).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- Plataforma de biometría de Windows API de WINBIO_BIR_HEADER Structure
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1479c0db3ee826d79cf95a311215c8cf76f1c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150292"
---
# <a name="winbio_bir_header-structure"></a><span data-ttu-id="75439-104">WINBIO \_ \_ estructura de encabezado Bir</span><span class="sxs-lookup"><span data-stu-id="75439-104">WINBIO\_BIR\_HEADER structure</span></span>

<span data-ttu-id="75439-105">La estructura del **\_ \_ encabezado WINBIO Bir** contiene el encabezado de un registro de información biométrica (BIR).</span><span class="sxs-lookup"><span data-stu-id="75439-105">The **WINBIO\_BIR\_HEADER** structure contains the header of a biometric information record (BIR).</span></span>

## <a name="syntax"></a><span data-ttu-id="75439-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75439-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a><span data-ttu-id="75439-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="75439-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="75439-108">**ValidFields**</span><span class="sxs-lookup"><span data-stu-id="75439-108">**ValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="75439-109">Máscara de máscara que especifica los campos de esta estructura válidos.</span><span class="sxs-lookup"><span data-stu-id="75439-109">Bitmask that specifies which fields in this structure are valid.</span></span> <span data-ttu-id="75439-110">Para obtener más información, [**consulte \_ \_ constantes de campo WINBIO Bir**](winbio-bir-field-constants.md).</span><span class="sxs-lookup"><span data-stu-id="75439-110">For more information, see [**WINBIO\_BIR\_FIELD Constants**](winbio-bir-field-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="75439-111">**HeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="75439-111">**HeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="75439-112">Una constante de la **\_ \_ versión de WINBIO Bir** que especifica la versión del encabezado.</span><span class="sxs-lookup"><span data-stu-id="75439-112">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="75439-113">Los números de versión son valores de 8 bits en los que los cuatro bits superiores especifican el número principal y los cuatro bits inferiores especifican el número de versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="75439-113">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="75439-114">Actualmente, esta debe ser WINBIO \_ CBEFF \_ Header \_ version (0x11).</span><span class="sxs-lookup"><span data-stu-id="75439-114">Currently this must be WINBIO\_CBEFF\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="75439-115">**PatronHeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="75439-115">**PatronHeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="75439-116">Una constante de la **\_ \_ versión de WINBIO Bir** que especifica la versión del encabezado.</span><span class="sxs-lookup"><span data-stu-id="75439-116">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="75439-117">Los números de versión son valores de 8 bits en los que los cuatro bits superiores especifican el número principal y los cuatro bits inferiores especifican el número de versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="75439-117">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="75439-118">Actualmente, este debe ser WINBIO de la versión de encabezado de un \_ patrocinador \_ \_ (0x11).</span><span class="sxs-lookup"><span data-stu-id="75439-118">Currently this must be WINBIO\_PATRON\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="75439-119">**Marcadores de la**</span><span class="sxs-lookup"><span data-stu-id="75439-119">**DataFlags**</span></span>
</dt> <dd>

<span data-ttu-id="75439-120">Valor que especifica el formato de los datos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="75439-120">A value that specifies the format of the header data.</span></span> <span data-ttu-id="75439-121">Puede ser **una operación OR bit a bit** de las siguientes marcas de nivel de procesamiento y de seguridad.</span><span class="sxs-lookup"><span data-stu-id="75439-121">This can be a bitwise **OR** of the following security and processing level flags.</span></span> <span data-ttu-id="75439-122">Para obtener más información, vea [**WINBIO \_ Bir \_ Data \_ Flags constantes**](winbio-bir-data-flags-constants.md).</span><span class="sxs-lookup"><span data-stu-id="75439-122">For more information, see [**WINBIO\_BIR\_DATA\_FLAGS Constants**](winbio-bir-data-flags-constants.md).</span></span>



| <span data-ttu-id="75439-123">Value</span><span class="sxs-lookup"><span data-stu-id="75439-123">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="75439-124">Significado</span><span class="sxs-lookup"><span data-stu-id="75439-124">Meaning</span></span>                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="75439-125"><dt>**WINBIO \_ \_ \_ Privacidad de marca de datos**</dt> <dt>((UCHAR) 0x02)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-125"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>((UCHAR)0x02)</dt></span></span> </dl>                                       | <span data-ttu-id="75439-126">Los datos se cifran.</span><span class="sxs-lookup"><span data-stu-id="75439-126">The data is encrypted.</span></span><br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="75439-127"><dt>**WINBIO \_ \_ \_ Integridad**</dt> de la marca de datos <dt>((UCHAR) 0x01)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-127"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>((UCHAR)0x01)</dt></span></span> </dl>                                 | <span data-ttu-id="75439-128">Los datos están firmados digitalmente o protegidos por un código de autenticación de mensajes (MAC).</span><span class="sxs-lookup"><span data-stu-id="75439-128">The data is digitally signed or protected by a message authentication code (MAC).</span></span><br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="75439-129"><dt>**WINBIO \_ Marca de datos \_ \_ firmada**</dt> <dt>((UCHAR) 0x04)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-129"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>((UCHAR)0x04)</dt></span></span> </dl>                                          | <span data-ttu-id="75439-130">Si se establece esta marca y la marca de integridad de la **\_ marca de datos \_ \_ WINBIO** , los datos se firman.</span><span class="sxs-lookup"><span data-stu-id="75439-130">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="75439-131">Si no se establece esta marca pero se establece la marca de integridad de la **\_ marca de datos \_ \_ WINBIO** , se calcula un equipo Mac a través de los datos.</span><span class="sxs-lookup"><span data-stu-id="75439-131">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed over the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="75439-132"><dt>**WINBIO \_ Marca de datos \_ \_ sin formato**</dt> <dt>((UCHAR) 0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-132"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>((UCHAR)0x20)</dt></span></span> </dl>                                                   | <span data-ttu-id="75439-133">Los datos están en el formato con el que se capturaron.</span><span class="sxs-lookup"><span data-stu-id="75439-133">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="75439-134"><dt>**WINBIO \_ Marca de datos \_ \_ intermedia**</dt> <dt>((UCHAR) 0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-134"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>((UCHAR)0x40)</dt></span></span> </dl>                        | <span data-ttu-id="75439-135">Los datos no son sin procesar, pero no se han procesado completamente.</span><span class="sxs-lookup"><span data-stu-id="75439-135">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="75439-136"><dt>**WINBIO \_ Marca de datos \_ \_ procesada**</dt> <dt>((UCHAR) 0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-136"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>((UCHAR)0x80)</dt></span></span> </dl>                                 | <span data-ttu-id="75439-137">Se han procesado los datos.</span><span class="sxs-lookup"><span data-stu-id="75439-137">The data has been processed.</span></span><br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="75439-138"><dt>**WINBIO \_ Máscara de opción de marca de datos \_ \_ \_ \_ presente**</dt> <dt>((UCHAR) 0x08)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-138"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>((UCHAR)0x08)</dt></span></span> </dl> | <span data-ttu-id="75439-139">Este valor siempre es 1.</span><span class="sxs-lookup"><span data-stu-id="75439-139">This value is always 1.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="75439-140">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="75439-140">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="75439-141">Un \_ \_ valor de tipo biométrico WINBIO que especifica el tipo de datos biométricos a los que se hace referencia en el registro de información biométrico.</span><span class="sxs-lookup"><span data-stu-id="75439-141">A WINBIO\_BIOMETRIC\_TYPE value that specifies the type of biometric data referenced in the biometric information record.</span></span> <span data-ttu-id="75439-142">Actualmente solo se admite la **\_ \_ huella digital de tipo WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="75439-142">Currently only **WINBIO\_TYPE\_FINGERPRINT** is supported.</span></span> <span data-ttu-id="75439-143">Para obtener más información, [**vea \_ constantes de \_ tipo biométrico WINBIO**](winbio-biometric-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="75439-143">For more information, see [**WINBIO\_BIOMETRIC\_TYPE Constants**](winbio-biometric-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="75439-144">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="75439-144">**Subtype**</span></span>
</dt> <dd>

<span data-ttu-id="75439-145">Valor **de \_ \_ subtipo biométrico WINBIO** que especifica el subfactor asociado a los datos biométricos.</span><span class="sxs-lookup"><span data-stu-id="75439-145">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="75439-146">Para obtener más información, vea comentarios y [**WINBIO las \_ constantes de \_ subtipo biométrico**](winbio-biometric-subtype-constants.md).</span><span class="sxs-lookup"><span data-stu-id="75439-146">For more information, see Remarks and [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="75439-147">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="75439-147">**Purpose**</span></span>
</dt> <dd>

<span data-ttu-id="75439-148">Una máscara de **\_ \_ propósito de WINBIO Bir** que especifica el uso previsto de los datos.</span><span class="sxs-lookup"><span data-stu-id="75439-148">A **WINBIO\_BIR\_PURPOSE** mask that specifies the intended use of the data.</span></span> <span data-ttu-id="75439-149">Puede ser **una operación OR bit a bit** de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="75439-149">This can be a bitwise **OR** of the following values.</span></span> <span data-ttu-id="75439-150">Para obtener más información, consulte [**WINBIO \_ Bir \_ purpose Constant**](winbio-bir-purpose-constants.md).</span><span class="sxs-lookup"><span data-stu-id="75439-150">For more information, see [**WINBIO\_BIR\_PURPOSE Constants**](winbio-bir-purpose-constants.md).</span></span>

-   <span data-ttu-id="75439-151">\_comprobación de propósito de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="75439-151">WINBIO\_PURPOSE\_VERIFY</span></span>
-   <span data-ttu-id="75439-152">\_identificación de propósito de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="75439-152">WINBIO\_PURPOSE\_IDENTIFY</span></span>
-   <span data-ttu-id="75439-153">\_inscripción de propósito de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="75439-153">WINBIO\_PURPOSE\_ENROLL</span></span>
-   <span data-ttu-id="75439-154">WINBIO \_ propósito \_ inscribirse \_ para la \_ comprobación</span><span class="sxs-lookup"><span data-stu-id="75439-154">WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION</span></span>
-   <span data-ttu-id="75439-155">WINBIO \_ propósito \_ inscribirse \_ para \_ identificación</span><span class="sxs-lookup"><span data-stu-id="75439-155">WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION</span></span>
-   <span data-ttu-id="75439-156">\_Auditoría de propósito de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="75439-156">WINBIO\_PURPOSE\_AUDIT</span></span>

</dd> <dt>

<span data-ttu-id="75439-157">**Calidad de los**</span><span class="sxs-lookup"><span data-stu-id="75439-157">**DataQuality**</span></span>
</dt> <dd>

<span data-ttu-id="75439-158">Valor que especifica la calidad relativa de los datos biométricos en el registro de información biométrica (BIR).</span><span class="sxs-lookup"><span data-stu-id="75439-158">A value that specifies the relative quality of the biometric data in the biometric information record (BIR).</span></span> <span data-ttu-id="75439-159">Puede ser un entero comprendido entre 0 y 100 o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="75439-159">This can be an integer from 0 to 100 or one of the following values.</span></span> <span data-ttu-id="75439-160">Para obtener más información, vea [**WINBIO \_ Bir \_ Quality constantes**](winbio-bir-quality-constants.md).</span><span class="sxs-lookup"><span data-stu-id="75439-160">For more information, see [**WINBIO\_BIR\_QUALITY Constants**](winbio-bir-quality-constants.md).</span></span>



| <span data-ttu-id="75439-161">Value</span><span class="sxs-lookup"><span data-stu-id="75439-161">Value</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="75439-162">Significado</span><span class="sxs-lookup"><span data-stu-id="75439-162">Meaning</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="75439-163"><dt>**WINBIO \_ Calidad de datos \_ \_ no \_ establecida**</dt> <dt>((WINBIO \_ Bir \_ Quality)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-163"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt>((WINBIO\_BIR\_QUALITY)-1)</dt></span></span> </dl>                   | <span data-ttu-id="75439-164">El creador de BIR admite las medidas de calidad, pero no se establece ningún valor en BIR.</span><span class="sxs-lookup"><span data-stu-id="75439-164">Quality measurements are supported by the BIR creator but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="75439-165"><dt>**WINBIO \_ Calidad de datos \_ \_ no \_ admitida**</dt> <dt>((WINBIO \_ Bir \_ Quality)-2)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-165"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt>((WINBIO\_BIR\_QUALITY)-2)</dt></span></span> </dl> | <span data-ttu-id="75439-166">El creador de BIR no admite las medidas de calidad.</span><span class="sxs-lookup"><span data-stu-id="75439-166">Quality measurements are not supported by the BIR creator.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="75439-167">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="75439-167">**CreationDate**</span></span>
</dt> <dd>

<span data-ttu-id="75439-168">Fecha y hora, en hora universal coordinada (hora del meridiano de Greenwich), a la que se creó el BIR.</span><span class="sxs-lookup"><span data-stu-id="75439-168">The date and time, in Coordinated Universal Time (Greenwich Mean Time), that the BIR was created.</span></span>

</dd> <dt>

<span data-ttu-id="75439-169">**ValidityPeriod**</span><span class="sxs-lookup"><span data-stu-id="75439-169">**ValidityPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="75439-170">Período para el que el BIR es válido.</span><span class="sxs-lookup"><span data-stu-id="75439-170">The period for which the BIR is valid.</span></span>

<dl> <dt>

<span data-ttu-id="75439-171">**BeginDate**</span><span class="sxs-lookup"><span data-stu-id="75439-171">**BeginDate**</span></span>
</dt> <dd>

<span data-ttu-id="75439-172">Fecha y hora, en hora universal coordinada, a la que comienza el período de validez.</span><span class="sxs-lookup"><span data-stu-id="75439-172">The date and time, in Coordinated Universal Time, that the validity period starts.</span></span>

</dd> <dt>

<span data-ttu-id="75439-173">**EndDate**</span><span class="sxs-lookup"><span data-stu-id="75439-173">**EndDate**</span></span>
</dt> <dd>

<span data-ttu-id="75439-174">Fecha y hora, en hora universal coordinada, a la que el BIR deja de ser válido.</span><span class="sxs-lookup"><span data-stu-id="75439-174">The date and time, in Coordinated Universal Time, at which the BIR ceases to be valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="75439-175">**BiometricDataFormat**</span><span class="sxs-lookup"><span data-stu-id="75439-175">**BiometricDataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="75439-176">Estructura [**de \_ \_ formato registrada WINBIO**](winbio-registered-format.md) que especifica el formato de datos del bloque de datos estándar en la estructura [**\_ Bir de WINBIO**](winbio-bir.md) .</span><span class="sxs-lookup"><span data-stu-id="75439-176">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the data format of the standard data block in the [**WINBIO\_BIR**](winbio-bir.md) structure.</span></span> <span data-ttu-id="75439-177">Los miembros de **\_ \_ formato registrados WINBIO** no pueden ser cero.</span><span class="sxs-lookup"><span data-stu-id="75439-177">The **WINBIO\_REGISTERED\_FORMAT** members cannot be zero.</span></span> <span data-ttu-id="75439-178">Puede utilizar las siguientes constantes para simplificar la comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="75439-178">You can use the following constants to simplify error checking.</span></span>



| <span data-ttu-id="75439-179">Value</span><span class="sxs-lookup"><span data-stu-id="75439-179">Value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="75439-180">Significado</span><span class="sxs-lookup"><span data-stu-id="75439-180">Meaning</span></span>                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <span data-ttu-id="75439-181"><dt>**WINBIO \_ NO hay ningún \_ propietario de formato \_ \_ disponible**</dt> <dt>((USHORT) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-181"><dt>**WINBIO\_NO\_FORMAT\_OWNER\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl> | <span data-ttu-id="75439-182">No se ha especificado ningún valor de propietario asignado IBIA (Asociación del sector biométrico internacional).</span><span class="sxs-lookup"><span data-stu-id="75439-182">No IBIA (International Biometric Industry Association) assigned owner value has been specified.</span></span><br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <span data-ttu-id="75439-183"><dt>**WINBIO \_ NO hay ningún \_ tipo de formato \_ \_ disponible**</dt> <dt>((USHORT) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-183"><dt>**WINBIO\_NO\_FORMAT\_TYPE\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl>    | <span data-ttu-id="75439-184">No se ha especificado ningún tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="75439-184">No format type has been specified.</span></span><br/>                                                              |



 

</dd> <dt>

<span data-ttu-id="75439-185">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="75439-185">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="75439-186">Estructura [**de \_ \_ formato registrada en WINBIO**](winbio-registered-format.md) que especifica el identificador de producto del componente que generó el bloque de datos estándar en el Bir.</span><span class="sxs-lookup"><span data-stu-id="75439-186">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the product ID of the component that generated the standard data block in the BIR.</span></span> <span data-ttu-id="75439-187">Los miembros de **\_ \_ formato registrados WINBIO** pueden ser cero.</span><span class="sxs-lookup"><span data-stu-id="75439-187">The **WINBIO\_REGISTERED\_FORMAT** members can be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75439-188">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75439-188">Remarks</span></span>

<span data-ttu-id="75439-189">El parámetro *SubType* especifica el subfactor asociado a los datos biométricos.</span><span class="sxs-lookup"><span data-stu-id="75439-189">The *Subtype* parameter specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="75439-190">Actualmente, el Plataforma de biometría de Windows (WBF) solo admite la captura de huellas digitales y usa las siguientes constantes para representar información de subtipos:</span><span class="sxs-lookup"><span data-stu-id="75439-190">Currently, the Windows Biometric Framework (WBF) supports only fingerprint capture and uses the following constants to represent sub-type information:</span></span>

-   <span data-ttu-id="75439-191">WINBIO \_ ANSI \_ 381 \_ pos \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="75439-191">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="75439-192">\_Thumb WINBIO ANSI \_ 381 \_ pos \_ RH \_</span><span class="sxs-lookup"><span data-stu-id="75439-192">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="75439-193">\_Dedo de \_ \_ \_ \_ índice RH \_ de WINBIO ANSI 381 pos</span><span class="sxs-lookup"><span data-stu-id="75439-193">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="75439-194">\_Dedo central de WINBIO ANSI \_ 381 \_ pos \_ dcha \_ \_</span><span class="sxs-lookup"><span data-stu-id="75439-194">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="75439-195">\_Dedo de \_ \_ \_ \_ anillo RH \_ de WINBIO ANSI 381 pos</span><span class="sxs-lookup"><span data-stu-id="75439-195">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="75439-196">\_ \_ \_ \_ \_ Pequeño \_ dedo de WINBIO ANSI 381 pos</span><span class="sxs-lookup"><span data-stu-id="75439-196">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="75439-197">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="75439-197">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="75439-198">WINBIO \_ de \_ Índice de LH de pdv ANSI 381 \_ pos \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="75439-198">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="75439-199">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ central \_</span><span class="sxs-lookup"><span data-stu-id="75439-199">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="75439-200">WINBIO \_ el \_ \_ dedo de \_ anillo de LH ANSI 381 pos \_ \_</span><span class="sxs-lookup"><span data-stu-id="75439-200">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="75439-201">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="75439-201">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="75439-202">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ cuatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="75439-202">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="75439-203">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ cuatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="75439-203">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="75439-204">WINBIO \_ ANSI \_ 381 \_ pos \_ dos \_ Thumbs</span><span class="sxs-lookup"><span data-stu-id="75439-204">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="75439-205">No intente validar el valor proporcionado para el valor del parámetro de *subtipo* .</span><span class="sxs-lookup"><span data-stu-id="75439-205">Do not attempt to validate the value supplied for the *Subtype* parameter value.</span></span> <span data-ttu-id="75439-206">El servicio biométrico de Windows validará el valor proporcionado antes de pasarlo a su implementación.</span><span class="sxs-lookup"><span data-stu-id="75439-206">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="75439-207">Si el valor es **WINBIO \_ SubType \_ no \_ Information** o **WINBIO \_ SubType \_ any**, valide cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="75439-207">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

<span data-ttu-id="75439-208">Si se declara alguno de los bits siguientes, la estructura **del \_ \_ encabezado WINBIO Bir** no tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="75439-208">If any of the following bits are asserted, the **WINBIO\_BIR\_HEADER** structure is not correctly formed.</span></span>


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a><span data-ttu-id="75439-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75439-209">Requirements</span></span>



| <span data-ttu-id="75439-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="75439-210">Requirement</span></span> | <span data-ttu-id="75439-211">Value</span><span class="sxs-lookup"><span data-stu-id="75439-211">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75439-212">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75439-212">Minimum supported client</span></span><br/> | <span data-ttu-id="75439-213">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="75439-213">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="75439-214">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75439-214">Minimum supported server</span></span><br/> | <span data-ttu-id="75439-215">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="75439-215">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="75439-216">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75439-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="75439-217"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75439-217"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75439-218">Vea también</span><span class="sxs-lookup"><span data-stu-id="75439-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75439-219">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="75439-219">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="75439-220">**WINBIO \_ constantes de \_ subtipo de biométrico**</span><span class="sxs-lookup"><span data-stu-id="75439-220">**WINBIO\_BIOMETRIC\_SUBTYPE Constants**</span></span>](winbio-biometric-subtype-constants.md)
</dt> <dt>

[<span data-ttu-id="75439-221">**WINBIO \_ Bir**</span><span class="sxs-lookup"><span data-stu-id="75439-221">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="75439-222">**\_Constantes de \_ marcadores de datos de WINBIO Bir \_**</span><span class="sxs-lookup"><span data-stu-id="75439-222">**WINBIO\_BIR\_DATA\_FLAGS Constants**</span></span>](winbio-bir-data-flags-constants.md)
</dt> <dt>

[<span data-ttu-id="75439-223">**WINBIO \_ \_ constantes de campo Bir**</span><span class="sxs-lookup"><span data-stu-id="75439-223">**WINBIO\_BIR\_FIELD Constants**</span></span>](winbio-bir-field-constants.md)
</dt> <dt>

[<span data-ttu-id="75439-224">**\_Constantes WINBIO Bir \_ purpose**</span><span class="sxs-lookup"><span data-stu-id="75439-224">**WINBIO\_BIR\_PURPOSE Constants**</span></span>](winbio-bir-purpose-constants.md)
</dt> <dt>

[<span data-ttu-id="75439-225">**Constantes de calidad de WINBIO \_ Bir \_**</span><span class="sxs-lookup"><span data-stu-id="75439-225">**WINBIO\_BIR\_QUALITY Constants**</span></span>](winbio-bir-quality-constants.md)
</dt> <dt>

[<span data-ttu-id="75439-226">**Constantes de versión de WINBIO \_ Bir \_**</span><span class="sxs-lookup"><span data-stu-id="75439-226">**WINBIO\_BIR\_VERSION Constants**</span></span>](winbio-bir-version-constants.md)
</dt> </dl>

 

 





