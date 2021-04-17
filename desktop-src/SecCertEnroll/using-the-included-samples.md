---
description: La API de inscripción de certificados incluye varios ejemplos diseñados para ayudarle a crear aplicaciones personalizadas. La mayoría de los ejemplos se escriben con C++, pero también se incluyen ejemplos de C# y Visual Basic Scripting Edition (VBScript).
ms.assetid: 70ac7b75-542c-4d79-85ce-4b1bac414879
title: Usar los ejemplos incluidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3cbf17d35e65ade52e97438d638cbd4f1489e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668109"
---
# <a name="using-the-included-samples"></a>Usar los ejemplos incluidos

La API de inscripción de certificados incluye varios ejemplos diseñados para ayudarle a crear aplicaciones personalizadas. La mayoría de los ejemplos se escriben con C++, pero también se incluyen ejemplos de C# y Visual Basic Scripting Edition (VBScript).

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, los ejemplos siguientes se instalan de forma predeterminada en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ .



| Muestra                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                | Idioma            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [createCNGCustomCMC](createcngcustomcmc.md)                           | Crea un objeto de solicitud CMC a partir de una solicitud PKCS 10 anidada interna \# .<br/>                                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCommon](enrollcommon.md)                                       | Contiene las siguientes funciones auxiliares y macros utilizadas por los ejemplos incluidos.<br/>                                                                                                                                                                                                                                                                | C++<br/>      |
| [enrollCustomCMC](enrollcustomcmc.md)                                 | Crea una solicitud de certificado CMC e inscribe un equipo en una jerarquía de certificados.<br/>                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCustomPKCS10](enrollcustompkcs10.md)                           | Crea una solicitud PKCS \# 10 personalizada, la envía a una [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA) independiente y lo instala en el [*almacén de certificados*](/windows/desktop/SecGloss/c-gly).<br/> | C++<br/>      |
| [enrollCustomPKCS10 \_ 2](enrollcustompkcs10-2.md)                      | Crea una solicitud PKCS \# 10 personalizada e intenta inscribirla en una CA empresarial.<br/>                                                                                                                                                                                                                                                               | C++<br/>      |
| [enrollEOBOCMC](enrolleobocmc.md)                                     | Crea una solicitud de certificado CMC en nombre de otro usuario e inscribe el usuario en una jerarquía de certificados.<br/>                                                                                                                                                                                                                                    | C++<br/>      |
| [enrollFromPublicKey](enrollfrompublickey.md)                         | Inicializa un objeto de \# solicitud de certificado PKCS 10, lo encapsula en un objeto de solicitud CMC, envía la solicitud CMC a una CA empresarial y guarda el certificado devuelto por la entidad de certificación en un archivo.<br/>                                                                                                                                                      | C++<br/>      |
| [enrollKeyArchivalCMC](enrollkeyarchivalcmc.md)                       | Crea una solicitud de certificado CMC para archivar una [*clave privada*](/windows/desktop/SecGloss/p-gly) en una entidad de certificación.<br/>                                                                                                                                                                                                     | C++<br/>      |
| [enrollNestedCMC](enrollnestedcmc.md)                                 | Lee una solicitud de certificado CMC existente desde un archivo, la incluye en otra solicitud CMC, firma esta solicitud externa, la envía a una CA y guarda la respuesta del certificado de la CA en un archivo.<br/>                                                                                                                                                 | C++<br/>      |
| [enrollPKCS7](enrollpkcs7.md)                                         | Crea una solicitud [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) desde un certificado existente heredando las claves públicas y privadas y la plantilla de certificado. En el ejemplo se inscribe el usuario en una jerarquía de certificados y se instala la respuesta del certificado.<br/>                                   | C++<br/>      |
| [enrollRenewalPKCS7](enrollrenewalpkcs7.md)                           | Crea un \# objeto de solicitud PKCS 7 para renovar un certificado existente.<br/>                                                                                                                                                                                                                                                                             | C++<br/>      |
| [enrollSimpleMachineCert](enrollsimplemachinecert.md)                 | Inscribe un equipo en una jerarquía de certificados mediante una plantilla, un nombre para mostrar del certificado y la descripción del certificado.<br/>                                                                                                                                                                                                                 | C++, VBS<br/> |
| [enrollSimpleUserCert](enrollsimpleusercert.md)                       | Inscribe un usuario final con una entidad de certificación usando una plantilla, el nombre del firmante y la longitud, en bits, de la clave.<br/>                                                                                                                                                                                                                                       | C++, C #<br/> |
| [enrollWithIX509EnrollmentHelper](enrollwithix509enrollmenthelper.md) | Muestra cómo usar el protocolo HTTP de Windows 7 para inscribir un certificado en una CA empresarial.<br/>                                                                                                                                                                                                                                                | C#<br/>      |
| [installResponseFromPFX](installresponsefrompfx.md)                   | Instala un certificado inscrito de un archivo de intercambio de información personal (PFX) en el almacén de certificados.<br/>                                                                                                                                                                                                                                      | C++<br/>      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

