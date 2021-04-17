---
description: Inscribe un equipo en una jerarquía de certificados mediante una plantilla, un nombre para mostrar del certificado y la descripción del certificado.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687759"
---
# <a name="enrollsimplemachinecert"></a>enrollSimpleMachineCert

El ejemplo enrollSimpleMachineCert inscribe un equipo en una jerarquía de certificados mediante una plantilla, un nombre para mostrar del certificado y la descripción del certificado.

## <a name="location"></a>Location

Cuando se instala el kit de desarrollo de software (SDK) de Microsoft Windows, se instala una versión de C++ del ejemplo, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ EnrollSimpleMachineCert Se instala una versión de VBScript en la carpeta *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VBS \\ EnrollSimpleMachineCert

## <a name="discussion"></a>Debate

El ejemplo enrollSimpleMachineCert:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de la plantilla, un nombre para mostrar del certificado y una descripción del certificado.
2.  Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) y lo Inicializa utilizando la plantilla especificada en la línea de comandos. El valor ContextAdministratorForceMachine para el primer parámetro especifica que un administrador que actúa en nombre de un equipo solicita el certificado.
3.  Agrega el nombre para mostrar y la descripción al objeto de inscripción.
4.  Intenta inscribir la solicitud de certificado y comprueba el estado del proceso. La función checkEnrollStatus se define en enrollCommon. cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



