---
description: La API de inscripción de certificados incluye varios ejemplos diseñados para ayudarle a crear aplicaciones personalizadas. La mayoría de los ejemplos se escriben mediante C++, pero también se incluyen ejemplos de C# y Visual Basic Scripting Edition (VBScript).
ms.assetid: 70ac7b75-542c-4d79-85ce-4b1bac414879
title: Uso de los ejemplos incluidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511d9d5424455c1b54c6bd03cc72138b3672b256d535dcbdaf31d2393b2cb5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127214"
---
# <a name="using-the-included-samples"></a>Uso de los ejemplos incluidos

La API de inscripción de certificados incluye varios ejemplos diseñados para ayudarle a crear aplicaciones personalizadas. La mayoría de los ejemplos se escriben mediante C++, pero también se incluyen ejemplos de C# y Visual Basic Scripting Edition (VBScript).

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, los ejemplos siguientes se instalan, de forma predeterminada, en la carpeta *%ProgramFiles%* \\ Microsoft SDK Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ .



| Muestra                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                | Idioma            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [createCNGCustomCMC](createcngcustomcmc.md)                           | Crea un objeto de solicitud de CMC a partir de una solicitud PKCS \# 10 anidada interna.<br/>                                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCommon](enrollcommon.md)                                       | Contiene las siguientes funciones auxiliares y macros usadas por los ejemplos incluidos.<br/>                                                                                                                                                                                                                                                                | C++<br/>      |
| [enrollCustomCMC](enrollcustomcmc.md)                                 | Crea una solicitud de certificado de CMC e inscribe un equipo en una jerarquía de certificados.<br/>                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCustomPKCS10](enrollcustompkcs10.md)                           | Crea una solicitud PKCS 10 personalizada, la envía a una entidad de certificación independiente (CA) e instala el certificado emitido en el \# almacén de [*certificados*](/windows/desktop/SecGloss/c-gly). [](/windows/desktop/SecGloss/c-gly)<br/> | C++<br/>      |
| [enrollCustomPKCS10 \_ 2](enrollcustompkcs10-2.md)                      | Crea una solicitud PKCS \# 10 personalizada e intenta inscribirla en una entidad de certificación empresarial.<br/>                                                                                                                                                                                                                                                               | C++<br/>      |
| [enrollEOBOCMC](enrolleobocmc.md)                                     | Crea una solicitud de certificado de CMC en nombre de otro usuario e inscribe al usuario en una jerarquía de certificados.<br/>                                                                                                                                                                                                                                    | C++<br/>      |
| [enrollFromPublicKey](enrollfrompublickey.md)                         | Inicializa un objeto de solicitud de certificado PKCS 10, lo encapsula en un objeto de solicitud de CMC, envía la solicitud de CMC a una CA empresarial y guarda el certificado devuelto por la CA en un \# archivo.<br/>                                                                                                                                                      | C++<br/>      |
| [enrollKeyArchivalCMC](enrollkeyarchivalcmc.md)                       | Crea una solicitud de certificado de CMC para archivar [*una clave privada*](/windows/desktop/SecGloss/p-gly) en una entidad de certificación.<br/>                                                                                                                                                                                                     | C++<br/>      |
| [enrollNestedCMC](enrollnestedcmc.md)                                 | Lee una solicitud de certificado de CMC existente de un archivo, la encapsula en otra solicitud de CMC, firma esta solicitud externa, la envía a una CA y guarda la respuesta del certificado de la CA en un archivo.<br/>                                                                                                                                                 | C++<br/>      |
| [enrollPKCS7](enrollpkcs7.md)                                         | Crea una [*solicitud PKCS \# 7*](/windows/desktop/SecGloss/p-gly) a partir de un certificado existente mediante la herencia de las claves públicas y privadas y la plantilla de certificado. El ejemplo inscribe al usuario en una jerarquía de certificados e instala la respuesta del certificado.<br/>                                   | C++<br/>      |
| [enrollRenewalPKCS7](enrollrenewalpkcs7.md)                           | Crea un objeto de solicitud PKCS \# 7 para renovar un certificado existente.<br/>                                                                                                                                                                                                                                                                             | C++<br/>      |
| [enrollSimpleMachineCert](enrollsimplemachinecert.md)                 | Inscribe un equipo en una jerarquía de certificados mediante una plantilla, un nombre para mostrar de certificado y la descripción del certificado.<br/>                                                                                                                                                                                                                 | C++, VBS<br/> |
| [enrollSimpleUserCert](enrollsimpleusercert.md)                       | Inscribe un usuario final con una entidad de certificación mediante una plantilla, el nombre del sujeto y la longitud, en bits, de la clave.<br/>                                                                                                                                                                                                                                       | C++, C #<br/> |
| [enrollWithIX509EnrollmentHelper](enrollwithix509enrollmenthelper.md) | Muestra cómo usar el protocolo HTTP Windows 7 para inscribir un certificado en una CA empresarial.<br/>                                                                                                                                                                                                                                                | C#<br/>      |
| [installResponseFromPFX](installresponsefrompfx.md)                   | Instala un certificado inscrito desde un archivo de Exchange personal (PFX) en el almacén de certificados.<br/>                                                                                                                                                                                                                                      | C++<br/>      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

