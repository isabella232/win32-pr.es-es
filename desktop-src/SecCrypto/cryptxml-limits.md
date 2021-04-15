---
description: CryptXML define los siguientes límites globales en el archivo de encabezado Cryptxml. h.
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: Límites de CryptXML (Cryptxml. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc56ee6459be2160efdeb8e9874e7dd0c53518d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497201"
---
# <a name="cryptxml-limits"></a>Límites de CryptXML

CryptXML define los siguientes límites globales en el archivo de encabezado Cryptxml. h.



| Constante o valor                                                                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <dt>**Cifrado \_ \_BLOB XML \_ máximo**</dt> <dt>0x7FFFFFF8</dt> </dl>                             | Los datos codificados no pueden superar los 2 gigabytes (GB).<br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <dt>**Cifrado \_ \_ID. \_ de XML máximo**</dt> <dt>256</dt> </dl>                                          | La longitud del identificador no puede superar los 256 caracteres.<br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <dt>**Cifrado \_ URI de XML \_ \_ máximo**</dt> <dt>8 \* 1024</dt> </dl>                                   | La longitud del URI no puede superar los 8192 caracteres.<br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <dt>**Cifrado \_ \_Firmas XML \_ máx**</dt> . <dt>16</dt> </dl>                   | Número máximo predeterminado de elementos de **firma** por documento. Este valor se puede invalidar especificando un nuevo máximo al pasar los valores de propiedad como estructuras de [**\_ \_ propiedades de CRYPT XML**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property) .<br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <dt>**Cifrado \_ \_Transformación XML \_ máx**</dt> . <dt>16</dt> </dl>                      | Número máximo de transformaciones, representadas por estructuras de [**\_ \_ algoritmos XML cifradas**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) , por referencia, representadas por una estructura de [**\_ \_ referencia XML de Crypt**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference) .<br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <dt>**Cifrado \_ \_Valor de firma XML \_ \_ máximo**</dt> <dt>2048</dt> </dl> | La longitud máxima, en bytes, de una estructura de [**\_ \_ firma de XML de cifrado**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) .<br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <dt>**Cifrado \_ Valor de Resumen de XML \_ \_ \_ máximo**</dt> <dt>128</dt> </dl>           | Longitud máxima, en bytes, de un resumen.<br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <dt>**Cifrado \_ \_Objetos XML \_ máx**</dt> . <dt>256</dt> </dl>                           | Se utiliza internamente para especificar el número máximo de elementos de **objeto** permitidos por firma.<br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <dt>**Cifrado \_ \_Referencias XML \_ Max**</dt> <dt>0x7FF8</dt> </dl>               | Número máximo de elementos de **referencia** permitidos.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Cryptxml. h</dt> </dl> |



 

 




