---
description: Instala un certificado inscrito desde un archivo de Exchange personal (PFX) en el almacén de certificados.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361836"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

El ejemplo installResponseFromPFX instala un certificado inscrito de un archivo de Exchange personal (PFX) en el almacén de certificados.

## <a name="location"></a>Location

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *%ProgramFiles%* \\ microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ installResponseFromPFX .

## <a name="discussion"></a>Debate

El ejemplo installResponseFromPFX:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener:
    -   Nombre del ejemplo.
    -   Nombre del archivo PFX que contiene el certificado inscrito.
    -   Contraseña asociada al archivo PFX.
2.  Lee el archivo PFX, intentando primero el formato base64 y el formato binario si se produce un error en Base64. La función DecodeFileW() se define en enrollCommon.cpp.
3.  Convierte el certificado inscrito en un **BSTR** y lo usa para inicializar un [**objeto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) La función convertWszToBstr se define en enrollCommon.cpp.
4.  Instala el certificado en el almacén de certificados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[enrollEOBOCMC](enrolleobocmc.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



