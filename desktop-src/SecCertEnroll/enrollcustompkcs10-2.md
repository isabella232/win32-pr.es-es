---
description: Crea una solicitud PKCS \# 10 personalizada e intenta inscribirla en una entidad de certificación (CA) empresarial.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686992"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

En el \_ ejemplo enrollCustomPKCS10 2 se crea una \# solicitud de PKCS 10 personalizada y se intenta inscribir en una [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA) empresarial.

## <a name="location"></a>Location

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala de forma predeterminada en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollCustomPKCS10 \_ 2.

## <a name="discussion"></a>Debate

El \_ ejemplo enrollCustomPKCS10 2:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de una plantilla y el nombre de un proveedor de servicios criptográficos.
2.  Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) y lo Inicializa utilizando el nombre de la plantilla especificada en la línea de comandos.
3.  Recupera la [*solicitud de certificado*](/windows/desktop/SecGloss/c-gly) del objeto de inscripción.
4.  Recupera la solicitud PKCS 10 más interna \# del objeto de solicitud de certificado obtenido en el paso 3.
5.  Recupera una [*clave privada*](/windows/desktop/SecGloss/p-gly) de la solicitud PKCS \# 10.
6.  Crea una colección [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) y agrega los proveedores de servicios criptográficos disponibles a la colección y, a continuación, recupera un objeto [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) para el proveedor especificado en la línea de comandos.
7.  Establece el objeto de estado en la clave privada.
8.  Intenta inscribir la [*solicitud de certificado*](/windows/desktop/SecGloss/c-gly).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\#Solicitud PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
