---
title: WINBIO_BIR_DATA_FLAGS constantes (Winbio \_ types.h)
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
ms.openlocfilehash: 87769500de02dedc7247b15e94064a43b7c6d528234c27ad700d4a336f42a092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622635"
---
# <a name="winbio_bir_data_flags-constants"></a>Constantes DE \_ MARCAS \_ DE DATOS \_ DE WINBIO BIR

El miembro **DataFlags** de la estructura [**WINBIO \_ BIR \_ HEADER**](winbio-bir-header.md) usa las siguientes constantes.



| Constante o valor                                                                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ Privacidad \_ de \_ marca de**</dt> datos <dt>0x02</dt> </dl>                                       | Los datos se cifran.<br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ INTEGRIDAD \_ DE \_ LA MARCA**</dt> DE DATOS <dt>0x01</dt> </dl>                                 | Los datos están firmados digitalmente o están protegidos por un código de autenticación de mensajes (MAC).<br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ MARCA \_ DE \_ DATOS CON**</dt> <dt>0X04</dt> </dl>                                          | Si se establecen esta marca y la marca INTEGRIDAD DE LA MARCA DE DATOS **\_ \_ \_ WINBIO,** los datos se firman. Si esta marca no está establecida pero la marca INTEGRIDAD DE LA MARCA DE DATOS WINBIO está establecida, se calcula un MAC en los datos. **\_ \_ \_**<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ Marca \_ de \_ datos sin**</dt> formato <dt>0x20</dt> </dl>                                                   | Los datos tienen el formato con el que se capturaron.<br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ MARCA \_ DE DATOS \_ 0X40**</dt> <dt></dt> </dl>                        | Los datos no son sin procesar, pero no se han procesado por completo.<br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ MARCA \_ DE \_ DATOS PROCESADA**</dt> <dt>0X80</dt> </dl>                                 | Los datos se han procesado.<br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ OPCIÓN \_ DE MARCA DE DATOS MASK \_ \_ \_ PRESENT**</dt> <dt>0x08</dt> </dl> | Máscara de marca. Este valor siempre es uno (1).<br/>                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





