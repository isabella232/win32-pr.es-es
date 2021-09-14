---
title: WINBIO_BIR_FIELD constantes (Winbio \_ types.h)
description: Especifique una máscara de bits.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160784"
---
# <a name="winbio_bir_field-constants"></a>Constantes DE \_ CAMPO BIR DE WINBIO \_

Las constantes siguientes se usan para crear una máscara de bits para el **miembro ValidFields** de la [**estructura WINBIO BIR \_ \_ HEADER.**](winbio-bir-header.md)



| Constante o valor                                                                                                                                                                                                                                                                                           | Descripción                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <dt>**WINBIO \_ RECUENTO \_ DE \_ \_ SUBHEADS DE CAMPO**</dt> BIR <dt>0x0001</dt> </dl>                          | Se proporciona para conformidad con NISTIR 6529-A, common biometric Exchange Formats Framework (CBEFF) Formato A, pero no se usa.<br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <dt>**WINBIO \_ Id. \_ \_ DE PRODUCTO DEL \_ CAMPO BIR**</dt> <dt>0x0002</dt> </dl>                                   | El **miembro ProductId** es válido.<br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <dt>**WINBIO \_ ID. \_ \_ DE CAMPO BIR \_ 0X0004**</dt> <dt></dt> </dl>                                      | Se proporciona para conformidad con NISTIR 6529-A, CBEFF Con formato A, pero no se usa.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <dt>**WINBIO \_ ÍNDICE \_ DE \_ CAMPO DE BIR**</dt> <dt>0x0008</dt> </dl>                                                   | Se proporciona para conformidad con NISTIR 6529-A, CBEFF Con formato A, pero no se usa.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <dt>**WINBIO \_ FECHA DE CREACIÓN DEL CAMPO BIR \_ \_ \_ 0x0010**</dt> <dt></dt> </dl>                          | El **miembro CreationDate** es válido.<br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <dt>**WINBIO \_ PERÍODO \_ DE VALIDEZ DEL CAMPO BIR \_ \_ 0x0020**</dt> <dt></dt> </dl>                    | El **miembro ValidityPeriod** es válido.<br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <dt>**WINBIO \_ TIPO \_ \_ BIOMÉTRICO \_ DE**</dt> CAMPO <dt>BIR 0x0040</dt> </dl>                       | El **miembro Type** es válido.<br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <dt>**WINBIO \_ SUBTIPO \_ \_ BIOMÉTRICO DE \_**</dt> CAMPO BIR <dt>0x0080</dt> </dl>              | El **miembro Subtype** es válido.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <dt>**WINBIO \_ VERSIÓN \_ DEL \_ ENCABEZADO CBEFF \_ \_ DEL**</dt> CAMPO <dt>BIR 0X0100</dt> </dl>    | El **miembro HeaderVersion** es válido.<br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <dt>**WINBIO \_ VERSIÓN \_ DEL ENCABEZADO BIR FIELD QUE \_ \_ \_ 0X0200**</dt> <dt></dt> </dl> | El **miembro DenheaderVersion** es válido.<br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <dt>**WINBIO \_ PROPÓSITO \_ \_ BIOMÉTRICO \_ DEL CAMPO BIR**</dt> <dt>0x0400</dt> </dl>              | El **miembro Purpose** es válido.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <dt>**WINBIO \_ CONDICIÓN \_ \_ BIOMÉTRICA \_ DEL CAMPO BIR**</dt> <dt>0x0800</dt> </dl>        | Se proporciona para conformidad con NISTIR 6529-A, CBEFF Con formato A, pero no se usa.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <dt>**WINBIO \_ CALIDAD \_ DEL \_ CAMPO BIR**</dt> <dt>0x1000</dt> </dl>                                             | El **miembro DataQuality** es válido.<br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ CREATOR**</dt> <dt>0x2000</dt> </dl>                                             | Se proporciona para conformidad con NISTIR 6529-A, CBEFF Con formato A, pero no se usa.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <dt>**WINBIO \_ PRUEBA \_ DE BIR FIELD \_ CHALLENGE**</dt> <dt>0x4000</dt> </dl>                                       | Se proporciona para conformidad con NISTIR 6529-A, CBEFF Con formato A, pero no se usa.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <dt>**WINBIO \_ CARGA \_ ÚTIL DEL \_ CAMPO BIR**</dt> <dt>0x8000</dt> </dl>                                             | Se proporciona para conformidad con NISTIR 6529-A, CBEFF Con formato A, pero no se usa.<br/>                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





