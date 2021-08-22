---
title: Uso del Kit para la certificación de aplicaciones en Windows
description: Para ofrecer a la aplicación de escritorio la mejor oportunidad de obtener la certificación, valide y pruebe en el equipo antes de enviarla para su certificación y publicación en Windows Store.
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8692e87f8bd152b730129c0d8684bc7ec2ca91964ecd6c25e98eb3db3e0fce44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118708753"
---
# <a name="using-the-windows-app-certification-kit"></a>Uso del Kit para la certificación de aplicaciones en Windows

Para ofrecer a la aplicación de escritorio la mejor oportunidad de obtener la certificación, valide y pruebe en el equipo antes de enviarla para su certificación y publicación en Windows Store. Para certificar la aplicación, debe instalar y ejecutar el Windows [App Certification Kit](/previous-versions//mt637081(v=vs.85)). Para obtener más información sobre las pruebas específicas dentro del kit, consulte Windows App Certification Kit tests (Pruebas del Kit de [certificación de aplicaciones).](windows-app-certification-kit-tests.md)

Para ver de alto nivel el proceso de certificación y dónde encaja el uso de esta herramienta, consulte [Certificación de la aplicación de escritorio.](windows-certification-portal.md)

La versión actual de Windows ACK está disponible en 14 idiomas (checo, inglés, francés, alemán, italiano, japonés, coreano, polaco, portugués (Brasil), ruso, chino simplificado, español, chino tradicional y turco).

## <a name="prerequisites"></a>Requisitos previos

Antes de instalar Windows ACK, debe instalar y ejecutar el sistema operativo.

1. Instale y ejecute el sistema operativo para el que está desarrollando aplicaciones.

-   Si va a desarrollar aplicaciones para Windows 7, puede instalar y ejecutar Windows 7, Windows 8 o Windows 8.1.
-   Si está desarrollando una aplicación de escritorio Windows 8 o una Windows 8 de dispositivo de escritorio, puede instalar y ejecutar Windows 8 o Windows 8.1.
-   Si está desarrollando una aplicación de escritorio Windows 8.1 o una Windows 8 de dispositivo de escritorio, instale Windows 8.1.

2. Instale Windows [App Certification Kit 3.3](/previous-versions//mt637081(v=vs.85)), que se incluye en el Kit de desarrollo de software (SDK) de Windows para Windows 8.1.

**Nota:** Al instalar Windows App Certification Kit 3.3 o posterior en el equipo, reemplaza cualquier versión instalada previamente del kit.

## <a name="instructions-to-run-windows-app-certification-kit-33"></a>Instrucciones para ejecutar Windows App Certification Kit 3.3

**Validación de la aplicación de escritorio mediante Windows App Certification Kit 3.3 de forma interactiva**

1.  En el menú Inicio, busque Windows App Cert Kit.
2.  En el Windows App Certification Kit, haga clic en la categoría de validación de pruebas que desea ejecutar. Si va a validar una aplicación de escritorio, seleccione **Validar aplicación de escritorio.**
3.  En la siguiente pantalla, vaya al archivo de instalación de la aplicación de escritorio que desea validar.
    -   **Nota:** Puede usar los pasos de [la línea de comandos](#commandlinesteps) para incluir opciones o un conmutador de instalación, si es necesario.
4.  Indique el tipo de uso de la aplicación y, a continuación, haga clic **en Siguiente.** El Windows App Certification Kit comienza a instalar la aplicación de escritorio mediante los archivos de instalación para que pueda validar la instalación.
5.  Si se le pide que reinicie el sistema para completar la instalación, elija **No**. Si la aplicación necesita instalar varios componentes o dependencias externas, seleccione cuidadosamente el nombre de la aplicación. El nombre que elija aquí es el nombre que se le da a la aplicación si aparece en Windows Store. Una vez completada la validación, guarde el informe con el nombre que agregó a la aplicación en el paso 6. El Windows App Certification Kit crea un archivo de informe XML y lo guarda.
6.  Vaya a la carpeta donde guardó el informe y ábralo para ver los resultados de la prueba. Si la prueba no se ha podido realizar y es apto para una exención, la información que necesita enviar se muestra aquí. Debe enviar una descripción detallada de cada solicitud de anulación posible.

**Validación de Windows aplicación de escritorio mediante Windows App Certification Kit 3.3 desde una línea de comandos**

1.  Vaya a la carpeta donde guardó el informe y ábralo para ver los resultados de la prueba. Aquí se enumeran las pruebas con errores con una posible solicitud de anulación. Debe enviar una descripción detallada de cada solicitud de anulación posible.
2.  En la carpeta que contiene Windows App Certification Kit, escriba estos comandos en este orden:

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    where: `[report file name]` es el nombre de archivo completo del archivo XML que el kit creará para contener el informe de prueba.

3.  Una vez completada la prueba, abra el archivo de informe denominado \[ nombre del archivo de informe y vea los \] resultados de la prueba.

    **Nota:** Para obtener más información sobre la línea de comandos Windows App Certification Kit, escriba el comando appcert.exe /?

    El Windows App Certification Kit debe ejecutarse en el contexto de una sesión de usuario activa, pero no puede iniciar aplicaciones en una sesión no interactiva. La forma en que el kit controla los tokens para ejecutar pruebas con o sin privilegios administrativos depende también de este contexto de sesión de usuario. El kit se puede ejecutar desde un servicio, pero el servicio debe ser capaz de generar el proceso del kit en una sesión de usuario activa.

**Use el kit de Windows app certification kit para validar Windows 7 aplicaciones**

-   El kit Windows app certification kit reemplaza al kit de logotipos Windows software. Si quiere el logotipo Windows 7 de la aplicación, use el kit de certificación de Windows app para las pruebas de validación y el informe. El kit puede detectar en qué sistema operativo se ejecuta y se inicia automáticamente para Windows 7 aplicaciones. Siga el mismo proceso para validar Windows 7 aplicaciones.

**Envío para la certificación**

-   Una vez validada la aplicación, está listo para enviarla para su certificación a través [del proceso de envío del portal.](https://www.microsoft.com/?ref=go)

## <a name="reference-documents"></a>Documentos de referencia

-   [Requisitos de certificación para Windows aplicaciones de escritorio](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [Documento técnico de certificación de aplicaciones](https://www.microsoft.com/download/details.aspx?id=27414)
-   [Windows Incorporación de store para aplicaciones de escritorio](/previous-versions//dn322034(v=vs.85))
-   [Windows 7 requisitos de certificación de aplicaciones de escritorio](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a>Pruebas del Kit para la certificación de aplicaciones en Windows

Hemos cambiado el kit para que las pruebas [Windows ACK sean](windows-app-certification-kit-tests.md) más fáciles de usar. El kit ahora tiene:

-   Nueva interfaz de usuario simplificada
-   Prueba de varios usuarios mejorada, que ya no requiere que configure una segunda cuenta de usuario.

 

 