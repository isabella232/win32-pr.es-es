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
# <a name="winbio_bir_data_flags-constants"></a>\_Constantes de \_ marcadores de datos de WINBIO Bir \_

**El miembro** WINBIO de la estructura de [**\_ \_ encabezado Bir**](winbio-bir-header.md) utiliza las siguientes constantes.



| Constante o valor                                                                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ \_ \_ Privacidad de marca de datos**</dt> <dt>0x02</dt> </dl>                                       | Los datos se cifran.<br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ \_ \_ Integridad de marca de datos**</dt> <dt>0x01</dt> </dl>                                 | Los datos están firmados digitalmente o están protegidos por un código de autenticación de mensajes (MAC).<br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ Marca de datos \_ \_ con la firma**</dt> <dt>0x04</dt> </dl>                                          | Si se establece esta marca y la marca de integridad de la **\_ marca de datos \_ \_ WINBIO** , los datos se firman. Si no se establece esta marca pero se establece la marca de integridad de la **\_ marca de datos \_ \_ WINBIO** , se calcula un equipo Mac en los datos.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ Marca de datos \_ \_ raw**</dt> <dt>0x20</dt> </dl>                                                   | Los datos están en el formato con el que se capturaron.<br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ Marca de datos \_ \_ intermedio**</dt> <dt>0x40</dt> </dl>                        | Los datos no son sin procesar, pero no se han procesado completamente.<br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ Marca de datos \_ \_ procesada**</dt> <dt>0x80</dt> </dl>                                 | Se han procesado los datos.<br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ Máscara de opción de marca de datos \_ \_ \_ \_ presente**</dt> <dt>0x08</dt> </dl> | Máscara de la marca. Este valor siempre es uno (1).<br/>                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





