---
title: EAPHost y esquema heredado
description: Describe el esquema de EAPHost y el esquema heredado para crear el XML de configuración y el XML de credenciales.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420033"
---
# <a name="eaphost-and-legacy-schema"></a>EAPHost y esquema heredado

En este tema se describe el esquema de EAPHost y el esquema heredado para crear XML de configuración y el XML de credenciales.

## <a name="about-eaphost-and-legacy-schema"></a>Acerca de EAPHost y el esquema heredado

La creación de XML de configuración comienza con el esquema [eaphostconfig](eaphostconfigschema-schema.md) ; la creación de XML de credenciales comienza con el esquema [eaphostusercredentials](eaphostusercredentialsschema-schema.md) .

Algunos de los esquemas nativos y heredados contienen elementos de esquema comunes. Los elementos comunes que se usan en la configuración de métodos y las credenciales de método se abstraen en un solo archivo de esquema, que se conoce como "esquema común".

Los términos "configuración de método" y "propiedades de conexión" se usan indistintamente. Del mismo modo, los términos "credenciales de método" y "propiedades de usuario" también se usan indistintamente.

## <a name="eaphost-schema"></a>Esquema de EAPHost



| Schema                                                                        | Descripción                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [baseeapmethodconfig](baseeapmethodconfigschema-schema.md)                   | Contiene elementos de esquema de configuración comunes.     |
| [baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md) | Contiene elementos comunes del esquema de credenciales.        |
| [eapcommon](eapcommonschema-schema.md)                                       | Contiene la definición del elemento **EapMethodType** . |
| [eaphostconfig](eaphostconfigschema-schema.md)                               | Contiene el esquema de configuración de EAPHost.             |
| [eaphostusercredentials](eaphostusercredentialsschema-schema.md)             | Contiene el esquema de credenciales de EAPHost.                |



 

## <a name="legacy-schema"></a>Esquema heredado



| Schema                                                                            | Descripción                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)   | Contiene elementos de esquema de configuración comunes.                                               |
| [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)               | Contiene elementos comunes del esquema de credenciales.                                                  |
| [eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)           | Contiene elementos de esquema de configuración comunes.                                               |
| [eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)                       | Contiene elementos comunes del esquema de credenciales.                                                  |
| [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)     | Se usa con EAP-TLS para describir los datos de configuración de autenticación.                          |
| [eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)     | Se usa con EAP-TLS para describir los datos de configuración de autenticación a partir de Windows 7. |
| [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)                 | Se usa con EAP-TLS para describir las credenciales de autenticación y las opciones de credenciales.          |
| [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) | Se utiliza con MS-CHAPv2 para describir los datos de configuración de autenticación.                        |
| [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)             | Se usa con MS-CHAPv2 para describir las credenciales de autenticación y las opciones de credenciales.        |
| [mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)     | Se usa con PEAPv0 para describir los datos de configuración de autenticación.                           |
| [mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)     | Se usa con PEAPv0 para describir los datos de configuración de autenticación a partir de Windows 7.  |
| [mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)                 | Se usa con PEAPv0 para describir las credenciales de autenticación y las opciones de credenciales.           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Revisión de los ejemplos de los esquemas de EAPHost y heredado](eaphost-schemas.md)
</dt> </dl>

 

 




