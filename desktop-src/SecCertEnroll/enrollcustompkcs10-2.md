---
description: Crea una solicitud PKCS \# 10 personalizada e intenta inscribirla en una entidad de certificación (CA) empresarial.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb88a2295217874a12da8b701a46f8dafe3db1cbf53d01273222e607195a789a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780044"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

El ejemplo enrollCustomPKCS10 2 crea una solicitud PKCS 10 personalizada e intenta inscribirla en una entidad de \_ \# [*certificación*](/windows/desktop/SecGloss/c-gly) (CA) empresarial.

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala de forma predeterminada en la carpeta *%ProgramFiles%* \\ microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCustomPKCS10 \_ 2 .

## <a name="discussion"></a>Debate

El ejemplo enrollCustomPKCS10 \_ 2:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de una plantilla y el nombre de un proveedor de servicios criptográficos.
2.  Crea un [**objeto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) y lo inicializa con el nombre de la plantilla especificada en la línea de comandos.
3.  Recupera la solicitud [*de certificado del*](/windows/desktop/SecGloss/c-gly) objeto de inscripción.
4.  Recupera la solicitud PKCS \# 10 más interna del objeto de solicitud de certificado obtenido en el paso 3.
5.  Recupera una [*clave privada de*](/windows/desktop/SecGloss/p-gly) la solicitud PKCS \# 10.
6.  Crea una [**colección ICspInformations,**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) agrega los proveedores criptográficos disponibles a la colección y, a continuación, recupera un objeto [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) para el proveedor especificado en la línea de comandos.
7.  Establece el objeto de estado en la clave privada.
8.  Intenta inscribir la solicitud [*de certificado*](/windows/desktop/SecGloss/c-gly).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
