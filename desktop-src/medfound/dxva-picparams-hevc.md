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
# <a name="dxva_picparams_hevc-structure"></a>PicParams de DXVA \_ \_ HEVC estructura

Proporciona los parámetros de nivel de imagen de una imagen comprimida para la descodificación de vídeo HEVC.

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Miembros

<dl> <dt>

**PicWidthInMinCbsY**
</dt> <dd></dd> <dt>

**PicHeightInMinCbsY**
</dt> <dd></dd> <dt>

**formato de croma \_ \_ IDC**
</dt> <dd></dd> <dt>

**\_marca de \_ plano de color independiente \_** 
</dt> <dd></dd> <dt>

**\_minus8 de \_ luminancia de profundidad de bits \_** 
</dt> <dd></dd> <dt>

**croma de profundidad de bits \_ \_ \_ minus8**
</dt> <dd></dd> <dt>

**LOG2 \_ Max \_ PIC \_ Order \_ CNT \_ LSB \_ minus4**
</dt> <dd></dd> <dt>

**NoPicReorderingFlag** 
</dt> <dd></dd> <dt>

 **NoBiPredFlag** 
</dt> <dd></dd> <dt>

**ReservedBits1** 
</dt> <dd></dd> <dt>

**wFormatAndSequenceInfoFlags**
</dt> <dd></dd> <dt>

**CurrPic**
</dt> <dd></dd> <dt>

**\_búfer máximo \_ Dec \_ PIC \_ \_ minus1**
</dt> <dd></dd> <dt>

**\_tamaño de bloque de codificación LOG2 min \_ Luma \_ \_ \_ \_ minus3**
</dt> <dd></dd> <dt>

**\_tamaño de \_ \_ bloque de \_ codificación Max Luma min \_ \_ \_ LOG2**
</dt> <dd></dd> <dt>

**LOG2 \_ min \_ Transform \_ \_ size Block \_ minus2**
</dt> <dd></dd> <dt>

**LOG2 \_ diff \_ \_ Min Max \_ Transform \_ \_ size Block**
</dt> <dd></dd> <dt>

**profundidad de jerarquía de transformación máxima en \_ \_ \_ \_ inter**
</dt> <dd></dd> <dt>

**profundidad de jerarquía de transformación máxima en \_ \_ \_ \_ intra**
</dt> <dd></dd> <dt>

**número \_ de \_ \_ \_ conjuntos PIC de referencia a corto plazo \_**
</dt> <dd></dd> <dt>

**número \_ de \_ \_ SPS de \_ fotos de referencia \_ a largo plazo**
</dt> <dd></dd> <dt>

**Num \_ ref \_ IDX \_ \_ \_ minus1 Active default \_**
</dt> <dd></dd> <dt>

**Num \_ ref \_ IDX \_ L1 \_ default \_ \_ minus1**
</dt> <dd></dd> <dt>

**init \_ QP \_ minus26**
</dt> <dd></dd> <dt>

**ucNumDeltaPocsOfRefRpsIdx**
</dt> <dd></dd> <dt>

**wNumBitsForShortTermRPSInSlice**
</dt> <dd></dd> <dt>

**ReservedBits2**
</dt> <dd></dd> <dt>

**marca de escala \_ habilitada de la lista \_ \_**
</dt> <dd></dd> <dt>

**\_marca habilitada para amp \_**
</dt> <dd></dd> <dt>

**ejemplo \_ de \_ marca de desplazamiento adaptable \_ habilitado \_**
</dt> <dd></dd> <dt>

**marca de PCM \_ habilitado \_** 
</dt> <dd></dd> <dt>

**\_densidad de bits de ejemplo PCM \_ \_ \_ \_ minus1** 
</dt> <dd></dd> <dt>

**\_croma de profundidad de bits de ejemplo PCM \_ \_ \_ \_ minus1** 
</dt> <dd></dd> <dt>

**\_tamaño de bloque de codificación LOG2 min \_ PCM \_ \_ \_ \_ \_ minus3** 
</dt> <dd></dd> <dt>

**LOG2 \_ diff \_ \_ Min Max \_ PCM \_ \_ \_ size bloque Coding \_ size**
</dt> <dd></dd> <dt>

**\_marca de filtro de bucle PCM \_ \_ deshabilitada \_**
</dt> <dd></dd> <dt>

**\_marca de \_ \_ presentación pics \_ de \_ referencia a largo plazo** 
</dt> <dd></dd> <dt>

**\_marca de MVP temporal de SPS \_ \_ habilitada \_**
</dt> <dd></dd> <dt>

**\_marca fuerte \_ \_ habilitada para intra-smoothing \_** 
</dt> <dd></dd> <dt>

**\_marca de segmentos de segmento dependiente \_ \_ habilitada \_** 
</dt> <dd></dd> <dt>

**marca de presentación de la marca de salida \_ \_ \_** 
</dt> <dd></dd> <dt>

**número \_ de \_ \_ bits de encabezado de segmento adicional \_** 
</dt> <dd></dd> <dt>

**\_marca de \_ ocultación de datos \_ habilitada \_**
</dt> <dd></dd> <dt>

**CABAC \_ init \_ present \_**
</dt> <dd></dd> <dt>

**ReservedBits3** 
</dt> <dd></dd> <dt>

**dwCodingParamToolFlags**
</dt> <dd></dd> <dt>

**\_marca de intra \_ Pred \_ restringida**
</dt> <dd></dd> <dt>

**marca de omisión de transformación \_ \_ habilitada \_**
</dt> <dd></dd> <dt>

**marca cu de \_ \_ Delta QP \_ habilitada \_**
</dt> <dd></dd> <dt>

**\_marca de \_ los \_ \_ desplazamientos \_ de \_ croma de la rodaja de PPS**
</dt> <dd></dd> <dt>

**\_marca Pred ponderada \_**
</dt> <dd></dd> <dt>

**\_marca bipred ponderada \_**
</dt> <dd></dd> <dt>

**marca de omisión de transquant \_ \_ habilitada \_**
</dt> <dd></dd> <dt>

**marca de iconos \_ habilitados \_** 
</dt> <dd></dd> <dt>

**marca de \_ codificación de entropía \_ \_ habilitada \_** 
</dt> <dd></dd> <dt>

**\_marca de espaciado uniforme \_** 
</dt> <dd></dd> <dt>

**filtro de bucle \_ \_ en la \_ \_ marca habilitada en iconos \_** 
</dt> <dd></dd> <dt>

**\_filtro de bucle PPS en la \_ \_ \_ \_ marca habilitada para segmentos \_**
</dt> <dd></dd> <dt>

**marca de desbloqueo de \_ \_ invalidación \_ habilitada de filtro \_**
</dt> <dd></dd> <dt>

**\_ \_ \_ marca deshabilitado de filtro de desbloqueo PPS \_**
</dt> <dd></dd> <dt>

**muestra \_ la \_ marca de presentación de modificación \_**
</dt> <dd></dd> <dt>

**marca de presentación de la \_ extensión de encabezado de segmento de segmento \_ \_ \_ \_**
</dt> <dd></dd> <dt>

**IrapPicFlag**
</dt> <dd></dd> <dt>

**IdrPicFlag** 
</dt> <dd></dd> <dt>

**IntraPicFlag** 
</dt> <dd></dd> <dt>

**ReservedBits4** 
</dt> <dd></dd> <dt>

**dwCodingSettingPicturePropertyFlags**
</dt> <dd></dd> <dt>

**\_desplazamiento CB \_ de PPC de PPS \_**
</dt> <dd></dd> <dt>

**\_desplazamiento CR \_ QP de PPS \_**
</dt> <dd></dd> <dt>

**numerar \_ columnas de mosaico \_ \_ minus1**
</dt> <dd></dd> <dt>

**número \_ de \_ filas de mosaico \_ minus1**
</dt> <dd></dd> <dt>

**ancho de columna \_ \_ minus1**
</dt> <dd></dd> <dt>

**alto de fila \_ \_ minus1**
</dt> <dd></dd> <dt>

**diferencia de la profundidad de la diferencia de \_ cu de cor \_ \_ \_**
</dt> <dd></dd> <dt>

**\_DIV2 de \_ desplazamiento \_ beta de PPS**
</dt> <dd></dd> <dt>

**\_DIV2 de \_ desplazamiento \_ TC de PPS**
</dt> <dd></dd> <dt>

**LOG2 \_ \_ nivel de combinación paralelo \_ \_ minus2**
</dt> <dd></dd> <dt>

**CurrPicOrderCntVal**
</dt> <dd></dd> <dt>

**RefPicList**
</dt> <dd></dd> <dt>

**ReservedBits5**
</dt> <dd></dd> <dt>

**PicOrderCntValList**
</dt> <dd></dd> <dt>

**RefPicSetStCurrBefore**
</dt> <dd></dd> <dt>

**RefPicSetStCurrAfter**
</dt> <dd></dd> <dt>

**RefPicSetLtCurr**
</dt> <dd></dd> <dt>

**ReservedBits6**
</dt> <dd></dd> <dt>

**ReservedBits7**
</dt> <dd></dd> <dt>

**StatusReportFeedbackNumber**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation estructuras](media-foundation-structures.md)
</dt> </dl>

 

 




