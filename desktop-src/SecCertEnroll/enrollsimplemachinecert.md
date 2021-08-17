---
description: Inscribe un equipo en una jerarquía de certificados mediante una plantilla, un nombre para mostrar de certificado y la descripción del certificado.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb533dc2c0d262a64f8fd1d2245c310880586c04900ef028e7c2609f1a6b4577
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976905"
---
# <a name="enrollsimplemachinecert"></a>enrollSimpleMachineCert

El ejemplo enrollSimpleMachineCert inscribe un equipo en una jerarquía de certificados mediante una plantilla, un nombre para mostrar de certificado y la descripción del certificado.

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, se instala una versión de C++ del ejemplo, de forma predeterminada, en la carpeta *%ProgramFiles% microsoft* \\ SDKs \\ Windows \\ v7.0 Samples Security \\ \\ \\ X509 Certificate Enrollment \\ VC \\ EnrollSimpleMachineCert . Se instala una versión de VBScript en la carpeta *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VBS \\ EnrollSimpleMachineCert .

## <a name="discussion"></a>Debate

El ejemplo enrollSimpleMachineCert:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de la plantilla, un nombre para mostrar del certificado y una descripción del certificado.
2.  Crea un [**objeto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) y lo inicializa mediante la plantilla especificada en la línea de comandos. El valor ContextAdministratorForceMachine del primer parámetro especifica que el certificado lo solicita un administrador que actúa en nombre de un equipo.
3.  Agrega el nombre para mostrar y la descripción al objeto de inscripción.
4.  Intenta inscribir la solicitud de certificado y comprueba el estado del proceso. La función checkEnrollStatus se define en enrollCommon.cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



