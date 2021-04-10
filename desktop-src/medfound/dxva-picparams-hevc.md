---
description: Proporciona los parámetros de nivel de imagen de una imagen comprimida para la descodificación de vídeo HEVC.
ms.assetid: F73AE9CD-5BBC-4A9F-8D05-707AD5E2E92A
title: DXVA_PicParams_HEVC estructura (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicParams_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: cafcbf31a7d4b7fee84e6c695f1d0f0a1e0302ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153636"
---
# <a name="dxva_picparams_hevc-structure"></a><span data-ttu-id="1b4f4-103">PicParams de DXVA \_ \_ HEVC estructura</span><span class="sxs-lookup"><span data-stu-id="1b4f4-103">DXVA\_PicParams\_HEVC structure</span></span>

<span data-ttu-id="1b4f4-104">Proporciona los parámetros de nivel de imagen de una imagen comprimida para la descodificación de vídeo HEVC.</span><span class="sxs-lookup"><span data-stu-id="1b4f4-104">Provides the picture-level parameters of a compressed picture for HEVC video decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b4f4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b4f4-105">Syntax</span></span>


```C++
typedef struct _DXVA_PicParams_HEVC {
  USHORT             PicWidthInMinCbsY;
  USHORT             PicHeightInMinCbsY;
  union {
    struct {
      USHORT chroma_format_idc  :2;
      USHORT separate_colour_plane_flag   :1;
      USHORT bit_depth_luma_minus8   :3;
      USHORT bit_depth_chroma_minus8  :3;
      USHORT log2_max_pic_order_cnt_lsb_minus4  :4;
      USHORT NoPicReorderingFlag   :1;
      USHORT  NoBiPredFlag   :1;
      USHORT ReservedBits1     :1;
    };
    USHORT  wFormatAndSequenceInfoFlags;
  };
  DXVA_PicEntry_HEVC CurrPic;
  UCHAR              sps_max_dec_pic_buffering_minus1;
  UCHAR              log2_min_luma_coding_block_size_minus3;
  UCHAR              log2_diff_max_min_luma_coding_block_size;
  UCHAR              log2_min_transform_block_size_minus2;
  UCHAR              log2_diff_max_min_transform_block_size;
  UCHAR              max_transform_hierarchy_depth_inter;
  UCHAR              max_transform_hierarchy_depth_intra;
  UCHAR              num_short_term_ref_pic_sets;
  UCHAR              num_long_term_ref_pics_sps;
  UCHAR              num_ref_idx_l0_default_active_minus1;
  UCHAR              num_ref_idx_l1_default_active_minus1;
  CHAR               init_qp_minus26;
  UCHAR              ucNumDeltaPocsOfRefRpsIdx;
  USHORT             wNumBitsForShortTermRPSInSlice;
  USHORT             ReservedBits2;
  union {
    struct {
      UINT32 scaling_list_enabled_flag  :1;
      UINT32 amp_enabled_flag  :1;
      UINT32 sample_adaptive_offset_enabled_flag  :1;
      UINT32 pcm_enabled_flag   :1;
      UINT32 pcm_sample_bit_depth_luma_minus1   :4;
      UINT32 pcm_sample_bit_depth_chroma_minus1     :4;
      UINT32 log2_min_pcm_luma_coding_block_size_minus3    :2;
      UINT32 log2_diff_max_min_pcm_luma_coding_block_size  :2;
      UINT32 pcm_loop_filter_disabled_flag  :1;
      UINT32 long_term_ref_pics_present_flag   :1;
      UINT32 sps_temporal_mvp_enabled_flag  :1;
      UINT32 strong_intra_smoothing_enabled_flag   :1;
      UINT32 dependent_slice_segments_enabled_flag    :1;
      UINT32 output_flag_present_flag   :1;
      UINT32 num_extra_slice_header_bits    :3;
      UINT32 sign_data_hiding_enabled_flag  :1;
      UINT32 cabac_init_present_flag  :1;
      UINT32 ReservedBits3    :5;
    };
    UINT32             dwCodingParamToolFlags;
    union {
      struct {
        UINT32 constrained_intra_pred_flag  :1;
        UINT32 transform_skip_enabled_flag  :1;
        UINT32 cu_qp_delta_enabled_flag  :1;
        UINT32 pps_slice_chroma_qp_offsets_present_flag  :1;
        UINT32 weighted_pred_flag  :1;
        UINT32 weighted_bipred_flag  :1;
        UINT32 transquant_bypass_enabled_flag  :1;
        UINT32 tiles_enabled_flag   :1;
        UINT32 entropy_coding_sync_enabled_flag   :1;
        UINT32 uniform_spacing_flag    :1;
        UINT32 loop_filter_across_tiles_enabled_flag   :1;
        UINT32 pps_loop_filter_across_slices_enabled_flag  :1;
        UINT32 deblocking_filter_override_enabled_flag  :1;
        UINT32 pps_deblocking_filter_disabled_flag  :1;
        UINT32 lists_modification_present_flag  :1;
        UINT32 slice_segment_header_extension_present_flag  :1;
        UINT32 IrapPicFlag  :1;
        UINT32 IdrPicFlag     :1;
        UINT32 IntraPicFlag   :1;
        UINT32 ReservedBits4     :13;
      };
      UINT32   dwCodingSettingPicturePropertyFlags;
    };
    CHAR               pps_cb_qp_offset;
    CHAR               pps_cr_qp_offset;
    UCHAR              num_tile_columns_minus1;
    UCHAR              num_tile_rows_minus1;
    USHORT             column_width_minus1[19];
    USHORT             row_height_minus1[21];
    UCHAR              diff_cu_qp_delta_depth;
    CHAR               pps_beta_offset_div2;
    CHAR               pps_tc_offset_div2;
    UCHAR              log2_parallel_merge_level_minus2;
    INT                CurrPicOrderCntVal;
    DXVA_PicEntry_HEVC RefPicList[15];
    UCHAR              ReservedBits5;
    INT                PicOrderCntValList[15];
    UCHAR              RefPicSetStCurrBefore[8];
    UCHAR              RefPicSetStCurrAfter[8];
    UCHAR              RefPicSetLtCurr[8];
    USHORT             ReservedBits6;
    USHORT             ReservedBits7;
    UINT               StatusReportFeedbackNumber;
  };
} DXVA_PicParams_HEVC, *PDXVA_PicParams_HEVC;
```



## <a name="members"></a><span data-ttu-id="1b4f4-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1b4f4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b4f4-107">**PicWidthInMinCbsY**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-107">**PicWidthInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-108">**PicHeightInMinCbsY**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-108">**PicHeightInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-109">**formato de croma \_ \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-109">**chroma\_format\_idc**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-110">**\_marca de \_ plano de color independiente \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-110">**separate\_colour\_plane\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-111">**\_minus8 de \_ luminancia de profundidad de bits \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-111">**bit\_depth\_luma\_minus8**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-112">**croma de profundidad de bits \_ \_ \_ minus8**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-112">**bit\_depth\_chroma\_minus8**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-113">**LOG2 \_ Max \_ PIC \_ Order \_ CNT \_ LSB \_ minus4**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-113">**log2\_max\_pic\_order\_cnt\_lsb\_minus4**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-114">**NoPicReorderingFlag**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-114">**NoPicReorderingFlag**</span></span> 
</dt> <dd></dd> <dt>

 <span data-ttu-id="1b4f4-115">**NoBiPredFlag**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-115">**NoBiPredFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-116">**ReservedBits1**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-116">**ReservedBits1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-117">**wFormatAndSequenceInfoFlags**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-117">**wFormatAndSequenceInfoFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-118">**CurrPic**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-118">**CurrPic**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-119">**\_búfer máximo \_ Dec \_ PIC \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-119">**sps\_max\_dec\_pic\_buffering\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-120">**\_tamaño de bloque de codificación LOG2 min \_ Luma \_ \_ \_ \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-120">**log2\_min\_luma\_coding\_block\_size\_minus3**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-121">**\_tamaño de \_ \_ bloque de \_ codificación Max Luma min \_ \_ \_ LOG2**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-121">**log2\_diff\_max\_min\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-122">**LOG2 \_ min \_ Transform \_ \_ size Block \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-122">**log2\_min\_transform\_block\_size\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-123">**LOG2 \_ diff \_ \_ Min Max \_ Transform \_ \_ size Block**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-123">**log2\_diff\_max\_min\_transform\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-124">**profundidad de jerarquía de transformación máxima en \_ \_ \_ \_ inter**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-124">**max\_transform\_hierarchy\_depth\_inter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-125">**profundidad de jerarquía de transformación máxima en \_ \_ \_ \_ intra**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-125">**max\_transform\_hierarchy\_depth\_intra**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-126">**número \_ de \_ \_ \_ conjuntos PIC de referencia a corto plazo \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-126">**num\_short\_term\_ref\_pic\_sets**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-127">**número \_ de \_ \_ SPS de \_ fotos de referencia \_ a largo plazo**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-127">**num\_long\_term\_ref\_pics\_sps**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-128">**Num \_ ref \_ IDX \_ \_ \_ minus1 Active default \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-128">**num\_ref\_idx\_l0\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-129">**Num \_ ref \_ IDX \_ L1 \_ default \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-129">**num\_ref\_idx\_l1\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-130">**init \_ QP \_ minus26**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-130">**init\_qp\_minus26**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-131">**ucNumDeltaPocsOfRefRpsIdx**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-131">**ucNumDeltaPocsOfRefRpsIdx**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-132">**wNumBitsForShortTermRPSInSlice**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-132">**wNumBitsForShortTermRPSInSlice**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-133">**ReservedBits2**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-133">**ReservedBits2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-134">**marca de escala \_ habilitada de la lista \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-134">**scaling\_list\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-135">**\_marca habilitada para amp \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-135">**amp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-136">**ejemplo \_ de \_ marca de desplazamiento adaptable \_ habilitado \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-136">**sample\_adaptive\_offset\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-137">**marca de PCM \_ habilitado \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-137">**pcm\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-138">**\_densidad de bits de ejemplo PCM \_ \_ \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-138">**pcm\_sample\_bit\_depth\_luma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-139">**\_croma de profundidad de bits de ejemplo PCM \_ \_ \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-139">**pcm\_sample\_bit\_depth\_chroma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-140">**\_tamaño de bloque de codificación LOG2 min \_ PCM \_ \_ \_ \_ \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-140">**log2\_min\_pcm\_luma\_coding\_block\_size\_minus3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-141">**LOG2 \_ diff \_ \_ Min Max \_ PCM \_ \_ \_ size bloque Coding \_ size**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-141">**log2\_diff\_max\_min\_pcm\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-142">**\_marca de filtro de bucle PCM \_ \_ deshabilitada \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-142">**pcm\_loop\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-143">**\_marca de \_ \_ presentación pics \_ de \_ referencia a largo plazo**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-143">**long\_term\_ref\_pics\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-144">**\_marca de MVP temporal de SPS \_ \_ habilitada \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-144">**sps\_temporal\_mvp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-145">**\_marca fuerte \_ \_ habilitada para intra-smoothing \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-145">**strong\_intra\_smoothing\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-146">**\_marca de segmentos de segmento dependiente \_ \_ habilitada \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-146">**dependent\_slice\_segments\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-147">**marca de presentación de la marca de salida \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-147">**output\_flag\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-148">**número \_ de \_ \_ bits de encabezado de segmento adicional \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-148">**num\_extra\_slice\_header\_bits**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-149">**\_marca de \_ ocultación de datos \_ habilitada \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-149">**sign\_data\_hiding\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-150">**CABAC \_ init \_ present \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-150">**cabac\_init\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-151">**ReservedBits3**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-151">**ReservedBits3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-152">**dwCodingParamToolFlags**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-152">**dwCodingParamToolFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-153">**\_marca de intra \_ Pred \_ restringida**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-153">**constrained\_intra\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-154">**marca de omisión de transformación \_ \_ habilitada \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-154">**transform\_skip\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-155">**marca cu de \_ \_ Delta QP \_ habilitada \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-155">**cu\_qp\_delta\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-156">**\_marca de \_ los \_ \_ desplazamientos \_ de \_ croma de la rodaja de PPS**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-156">**pps\_slice\_chroma\_qp\_offsets\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-157">**\_marca Pred ponderada \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-157">**weighted\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-158">**\_marca bipred ponderada \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-158">**weighted\_bipred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-159">**marca de omisión de transquant \_ \_ habilitada \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-159">**transquant\_bypass\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-160">**marca de iconos \_ habilitados \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-160">**tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-161">**marca de \_ codificación de entropía \_ \_ habilitada \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-161">**entropy\_coding\_sync\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-162">**\_marca de espaciado uniforme \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-162">**uniform\_spacing\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-163">**filtro de bucle \_ \_ en la \_ \_ marca habilitada en iconos \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-163">**loop\_filter\_across\_tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-164">**\_filtro de bucle PPS en la \_ \_ \_ \_ marca habilitada para segmentos \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-164">**pps\_loop\_filter\_across\_slices\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-165">**marca de desbloqueo de \_ \_ invalidación \_ habilitada de filtro \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-165">**deblocking\_filter\_override\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-166">**\_ \_ \_ marca deshabilitado de filtro de desbloqueo PPS \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-166">**pps\_deblocking\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-167">**muestra \_ la \_ marca de presentación de modificación \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-167">**lists\_modification\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-168">**marca de presentación de la \_ extensión de encabezado de segmento de segmento \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-168">**slice\_segment\_header\_extension\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-169">**IrapPicFlag**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-169">**IrapPicFlag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-170">**IdrPicFlag**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-170">**IdrPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-171">**IntraPicFlag**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-171">**IntraPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-172">**ReservedBits4**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-172">**ReservedBits4**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-173">**dwCodingSettingPicturePropertyFlags**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-173">**dwCodingSettingPicturePropertyFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-174">**\_desplazamiento CB \_ de PPC de PPS \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-174">**pps\_cb\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-175">**\_desplazamiento CR \_ QP de PPS \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-175">**pps\_cr\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-176">**numerar \_ columnas de mosaico \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-176">**num\_tile\_columns\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-177">**número \_ de \_ filas de mosaico \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-177">**num\_tile\_rows\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-178">**ancho de columna \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-178">**column\_width\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-179">**alto de fila \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-179">**row\_height\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-180">**diferencia de la profundidad de la diferencia de \_ cu de cor \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-180">**diff\_cu\_qp\_delta\_depth**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-181">**\_DIV2 de \_ desplazamiento \_ beta de PPS**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-181">**pps\_beta\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-182">**\_DIV2 de \_ desplazamiento \_ TC de PPS**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-182">**pps\_tc\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-183">**LOG2 \_ \_ nivel de combinación paralelo \_ \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-183">**log2\_parallel\_merge\_level\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-184">**CurrPicOrderCntVal**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-184">**CurrPicOrderCntVal**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-185">**RefPicList**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-185">**RefPicList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-186">**ReservedBits5**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-186">**ReservedBits5**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-187">**PicOrderCntValList**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-187">**PicOrderCntValList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-188">**RefPicSetStCurrBefore**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-188">**RefPicSetStCurrBefore**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-189">**RefPicSetStCurrAfter**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-189">**RefPicSetStCurrAfter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-190">**RefPicSetLtCurr**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-190">**RefPicSetLtCurr**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-191">**ReservedBits6**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-191">**ReservedBits6**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-192">**ReservedBits7**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-192">**ReservedBits7**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1b4f4-193">**StatusReportFeedbackNumber**</span><span class="sxs-lookup"><span data-stu-id="1b4f4-193">**StatusReportFeedbackNumber**</span></span>
<span data-ttu-id="1b4f4-194"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1b4f4-194"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1b4f4-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b4f4-195">Requirements</span></span>



| <span data-ttu-id="1b4f4-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b4f4-196">Requirement</span></span> | <span data-ttu-id="1b4f4-197">Value</span><span class="sxs-lookup"><span data-stu-id="1b4f4-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1b4f4-198">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b4f4-198">Minimum supported client</span></span><br/> | <span data-ttu-id="1b4f4-199">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="1b4f4-199">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1b4f4-200">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b4f4-200">Minimum supported server</span></span><br/> | <span data-ttu-id="1b4f4-201">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b4f4-201">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1b4f4-202">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b4f4-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b4f4-203"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b4f4-203"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b4f4-204">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b4f4-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4f4-205">Media Foundation estructuras</span><span class="sxs-lookup"><span data-stu-id="1b4f4-205">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




