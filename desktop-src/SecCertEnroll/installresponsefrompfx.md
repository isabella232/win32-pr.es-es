---
description: Instala un certificado inscrito desde un archivo de Exchange personal (PFX) en el almacén de certificados.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540e719f098d227afac4af59fd2d296d9d06606d04b9de80cf1e24081918d6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117777611"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

El ejemplo installResponseFromPFX instala un certificado inscrito desde un archivo Exchange información personal (PFX) en el almacén de certificados.

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta vc installResponseFromPFX *%ProgramFiles%* de los SDK de \\ Microsoft Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ installResponseFromPFX.

## <a name="discussion"></a>Debate

El ejemplo installResponseFromPFX:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener:
    -   Nombre del ejemplo.
    -   Nombre del archivo PFX que contiene el certificado inscrito.
    -   Contraseña asociada al archivo PFX.
2.  Lee el archivo PFX, intentando primero el formato base64 y el formato binario si se produce un error en base64. La función DecodeFileW() se define en enrollCommon.cpp.
3.  Convierte el certificado inscrito en un **BSTR** y lo usa para inicializar un [**objeto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) La función convertWszToBstr se define en enrollCommon.cpp.
4.  Instala el certificado en el almacén de certificados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[enrollEOBOCMC](enrolleobocmc.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



