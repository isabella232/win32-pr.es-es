---
description: Instala un certificado inscrito de un archivo de intercambio de información personal (PFX) en el almacén de certificados.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002677"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

El ejemplo installResponseFromPFX instala un certificado inscrito de un archivo de intercambio de información personal (PFX) en el almacén de certificados.

## <a name="location"></a>Location

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ installResponseFromPFX

## <a name="discussion"></a>Debate

El ejemplo installResponseFromPFX:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener:
    -   Nombre del ejemplo.
    -   Nombre del archivo PFX que contiene el certificado inscrito.
    -   Una contraseña asociada con el archivo PFX.
2.  Lee el archivo PFX, intentando primero el formato Base64 y el formato binario si se produce un error en Base64. La función DecodeFileW () se define en enrollCommon. cpp.
3.  Convierte el certificado inscrito en un **BSTR** y lo utiliza para inicializar un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . La función convertWszToBstr se define en enrollCommon. cpp.
4.  Instala el certificado en el almacén de certificados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[enrollEOBOCMC](enrolleobocmc.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



