---
description: CryptXML define los siguientes límites globales en el archivo de encabezado Cryptxml.h.
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: Límites de CryptXML (Cryptxml.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a0dcdf5dc8f8bd9efed4dcdb15ca316ecb1645e5775f3d714f46c6835b3a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100925"
---
# <a name="cryptxml-limits"></a>Límites de CryptXML

CryptXML define los siguientes límites globales en el archivo de encabezado Cryptxml.h.



| Constante o valor                                                                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <dt>**CRYPT \_ XML \_ BLOB \_ MAX**</dt> <dt>0x7FFFFFF8</dt> </dl>                             | Los datos codificados no pueden superar los 2 gigabytes (GB).<br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <dt>**CRYPT \_ ID. \_ \_ XML MÁX.**</dt> <dt>256</dt> </dl>                                          | La longitud del identificador no puede superar los 256 caracteres.<br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <dt>**CRYPT \_ URI \_ XML \_ MÁX.**</dt> <dt>8 \* 1024</dt> </dl>                                   | La longitud del URI no puede superar los 8192 caracteres.<br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <dt>**CRYPT \_ FIRMAS XML \_ \_ MÁX.**</dt> <dt>16</dt> </dl>                   | Número máximo predeterminado de elementos **Signature** por documento. Este valor se puede invalidar especificando un nuevo máximo al pasar valores de propiedad como [**estructuras \_ CRYPT XML \_ PROPERTY.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property)<br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <dt>**CRYPT \_ TRANSFORMACIÓN \_ XML \_ MÁX.**</dt> <dt>16</dt> </dl>                      | Número máximo de transformaciones, representadas por estructuras [**CRYPT \_ XML \_ ALGORITHM,**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) por referencia, representadas por una [**estructura CRYPT XML \_ \_ REFERENCE.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference)<br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <dt>**CRYPT \_ VALOR \_ MÁXIMO DE FIRMA \_ \_ XML**</dt> <dt>2048</dt> </dl> | Longitud máxima, en bytes, de una [**estructura CRYPT \_ XML \_ SIGNATURE.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature)<br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <dt>**CRYPT \_ VALOR \_ DE RESUMEN XML \_ \_ MÁXIMO**</dt> <dt>128</dt> </dl>           | Longitud máxima, en bytes, de un resumen.<br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <dt>**CRYPT \_ XML \_ OBJECTS \_ MAX**</dt> <dt>256</dt> </dl>                           | Se usa internamente para especificar el número máximo de **elementos Object** permitidos por firma.<br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <dt>**CRYPT \_ NÚMERO \_ MÁXIMO DE REFERENCIAS \_ XML**</dt> <dt>0x7FF8</dt> </dl>               | Número máximo de elementos **Reference** permitidos.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cryptxml.h</dt> </dl> |



 

 




