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
# <a name="winbio_bir_field-constants"></a>WINBIO \_ \_ constantes de campo Bir

Las constantes siguientes se usan para crear una máscara de máscara para el miembro **ValidFields** de la estructura de [**\_ \_ encabezado Bir de WINBIO**](winbio-bir-header.md) .



| Constante o valor                                                                                                                                                                                                                                                                                           | Descripción                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <dt>**WINBIO \_ Recuento de \_ \_ subencabezados \_ de campo Bir**</dt> <dt>0x0001</dt> </dl>                          | Proporcionado para la conformidad con NISTIR 6529-A, el marco de trabajo de formatos biométricos (CBEFF) de los empleados es el formato A, pero no se usa.<br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <dt>**WINBIO \_ \_ \_ \_ ID. de producto de campo Bir**</dt> <dt>0x0002</dt> </dl>                                   | El miembro **ProductID** es válido.<br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <dt>**WINBIO \_ BIR \_ campo \_ \_ ID**</dt> <dt>0x0004</dt> </dl>                                      | Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <dt>**WINBIO \_ BIR \_ \_ Índice de campo**</dt> <dt>0x0008</dt> </dl>                                                   | Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <dt>**WINBIO \_ BIR \_ \_ \_ fecha de creación de campos**</dt> <dt>0x0010</dt> </dl>                          | El miembro **CreationDate** es válido.<br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <dt>**WINBIO \_ BIR \_ \_ \_ período de validez del campo**</dt> <dt>0x0020</dt> </dl>                    | El miembro **ValidityPeriod** es válido.<br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Tipo biométrico de campo Bir**</dt> <dt>0x0040</dt> </dl>                       | El miembro de **tipo** es válido.<br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <dt>**WINBIO \_ BIR \_ campo \_ biométrico \_**</dt> <dt>0x0080</dt> </dl>              | El miembro del **subtipo** es válido.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <dt>**WINBIO \_ BIR \_ campo \_ CBEFF \_ \_ versión de encabezado**</dt> <dt>0x0100</dt> </dl>    | El miembro **HeaderVersion** es válido.<br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <dt>**WINBIO \_ BIR \_ campo de la \_ \_ \_ versión de encabezado**</dt> <dt>0x0200</dt> </dl> | El miembro **PatronHeaderVersion** es válido.<br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <dt>**WINBIO \_ BIR \_ de \_ \_ uso biométrico de campo**</dt> <dt>0x0400</dt> </dl>              | El miembro **purpose** es válido.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <dt>**WINBIO \_ BIR \_ \_ \_ condición biométrica de campo**</dt> <dt>0x0800</dt> </dl>        | Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <dt>**WINBIO \_ \_ \_ Calidad de campo Bir**</dt> <dt>0x1000</dt> </dl>                                             | El miembro de calidad de la **cualidad** es válido.<br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <dt>**WINBIO \_ \_ \_ Creador del campo Bir**</dt> <dt>0x2000</dt> </dl>                                             | Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <dt>**WINBIO \_ \_ \_ Desafío de campo Bir**</dt> <dt>0x4000</dt> </dl>                                       | Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <dt>**WINBIO \_ \_ \_ Carga de campo Bir**</dt> <dt>0x8000</dt> </dl>                                             | Se proporciona para la conformidad con el formato de NISTIR 6529-A, CBEFF A, pero no se usa.<br/>                                                   |



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

 

 





