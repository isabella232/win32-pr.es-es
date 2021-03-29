---
title: Uso del Kit para la certificación de aplicaciones en Windows
description: Para proporcionar a la aplicación de escritorio la mejor oportunidad de obtener la certificación, validarla y probarla en el equipo antes de enviarla para su certificación y publicarla en la tienda Windows.
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89b3c6e4de3286dd6418c4c8e186bcadaddf00b7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421527"
---
# <a name="using-the-windows-app-certification-kit"></a>Uso del Kit para la certificación de aplicaciones en Windows

Para proporcionar a la aplicación de escritorio la mejor oportunidad de obtener la certificación, validarla y probarla en el equipo antes de enviarla para su certificación y publicarla en la tienda Windows. Para certificar la aplicación, debe instalar y ejecutar el [Kit de certificación de aplicaciones de Windows](/previous-versions//mt637081(v=vs.85)). Para obtener más información sobre las pruebas específicas del kit, consulte [pruebas del kit de certificación de aplicaciones de Windows](windows-app-certification-kit-tests.md).

Para obtener una visión general del proceso de certificación y el uso de esta herramienta en, consulte certificación de la [aplicación de escritorio](windows-certification-portal.md).

La versión actual de ACK de Windows está disponible en 14 idiomas (Checo, Inglés, Francés, alemán, Italiano, Japonés, Coreano, Polaco, Portugués (Brasil), Ruso, Chino simplificado, español, Chino tradicional y Turco).

## <a name="prerequisites"></a>Requisitos previos

Antes de instalar la confirmación de Windows, debe instalar y ejecutar el sistema operativo.

1. Instale y ejecute el sistema operativo para el que está desarrollando aplicaciones.

-   Si está desarrollando aplicaciones para Windows 7, puede instalar y ejecutar Windows 7, Windows 8 o Windows 8.1.
-   Si está desarrollando una aplicación de escritorio de Windows 8 o de dispositivo de escritorio de Windows 8, puede instalar y ejecutar Windows 8 o Windows 8.1.
-   Si está desarrollando una aplicación de escritorio Windows 8.1 o una aplicación de dispositivo de escritorio de Windows 8, instale Windows 8.1.

2. Instale el [Kit de certificación de aplicaciones de windows 3,3](/previous-versions//mt637081(v=vs.85)), que se incluye en el kit de desarrollo de software (SDK) de windows para Windows 8.1.

**Nota:** Al instalar el kit de certificación de aplicaciones de Windows 3,3 o superior en el equipo, se reemplaza cualquier versión instalada previamente del kit.

## <a name="instructions-to-run-windows-app-certification-kit-33"></a>Instrucciones para ejecutar el kit de certificación de aplicaciones de Windows 3,3

**Validar la aplicación de escritorio mediante el kit de certificación de aplicaciones de Windows 3,3 de forma interactiva**

1.  En el menú Inicio, busque el kit de certificación de aplicaciones de Windows.
2.  En el kit de certificación de aplicaciones de Windows, haga clic en la categoría de validación de prueba que quiere ejecutar. Si va a validar una aplicación de escritorio, seleccione **validar aplicación de escritorio**.
3.  En la siguiente pantalla, busque el archivo de instalación de la aplicación de escritorio que desea validar.
    -   **Nota:** Puede usar los pasos de la [línea de comandos](#commandlinesteps) para incluir opciones o un modificador de instalación, si es necesario.
4.  Indique el tipo de uso de la aplicación y, a continuación, haga clic en **siguiente**. El kit para la certificación de aplicaciones de Windows inicia la instalación de la aplicación de escritorio con los archivos de instalación para que pueda validar la instalación.
5.  Si se le pide que reinicie el sistema para completar la instalación, elija **no**. Si la aplicación necesita instalar varios componentes o dependencias externas, seleccione cuidadosamente el nombre de la aplicación. El nombre que elija aquí es el nombre de la aplicación si aparece en la tienda Windows. Una vez finalizada la validación, guarde el informe con el nombre que asignó a la aplicación en el paso 6. El kit para la certificación de aplicaciones de Windows crea un archivo de informe XML y lo guarda.
6.  Navegue hasta la carpeta donde guardó el informe y ábralo para ver los resultados de la prueba. Si se produce un error en la prueba y es válido para una renuncia, la información que necesita enviar se muestra aquí. Debe enviar una descripción detallada de cada solicitud de exención posible.

**Validar la aplicación de escritorio de Windows con el kit de certificación de aplicaciones de Windows 3,3 desde una línea de comandos**

1.  Navegue hasta la carpeta donde guardó el informe y ábralo para ver los resultados de la prueba. Aquí se enumeran las pruebas con errores con una posible solicitud de exención. Debe enviar una descripción detallada de cada solicitud de exención posible.
2.  En la carpeta que contiene el kit para la certificación de aplicaciones de Windows, escriba estos comandos en este orden:

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    donde: `[report file name]` es el nombre de archivo completo del archivo XML que creará el kit para que contenga el informe de prueba.

3.  Una vez finalizada la prueba, abra el archivo de informe denominado \[ nombre \] del archivo de informe y vea los resultados de la prueba.

    **Nota:** Para obtener más información acerca de la línea de comandos del kit para la certificación de aplicaciones de Windows, escriba el comando appcert.exe/?

    El kit para la certificación de aplicaciones de Windows debe ejecutarse en el contexto de una sesión de usuario activa, pero no puede iniciar aplicaciones en una sesión no interactiva. La forma en que el kit controla los tokens para ejecutar pruebas con o sin privilegios administrativos depende también de este contexto de sesión de usuario. El kit se puede ejecutar desde un servicio, pero el servicio debe ser capaz de generar el proceso del kit en una sesión de usuario activa.

**Usar el kit de certificación de aplicaciones de Windows para validar las aplicaciones de Windows 7**

-   El kit de certificación de aplicaciones de Windows ha reemplazado al kit de logotipo de software de Windows. Si desea usar el logotipo de Windows 7 para su aplicación, use el kit para la certificación de aplicaciones de Windows para las pruebas de validación y el informe. El kit puede detectar el sistema operativo en el que se ejecuta y se inicia automáticamente para las aplicaciones de Windows 7. Siga el mismo proceso para validar las aplicaciones de Windows 7.

**Envío para la certificación**

-   Una vez validada la aplicación, está listo para enviarla para su certificación [a través del proceso de envío del portal](https://www.microsoft.com/?ref=go).

## <a name="reference-documents"></a>Documentos de referencia

-   [Requisitos de certificación para aplicaciones de escritorio de Windows](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [Notas del producto de certificación de aplicaciones](https://www.microsoft.com/download/details.aspx?id=27414)
-   [Incorporación de la tienda Windows para aplicaciones de escritorio](/previous-versions//dn322034(v=vs.85))
-   [Requisitos de certificación de aplicaciones de escritorio de Windows 7](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a>Pruebas del Kit para la certificación de aplicaciones en Windows

Hemos cambiado el kit para que las [pruebas de confirmación de Windows](windows-app-certification-kit-tests.md) sean más fáciles de usar. El kit ahora tiene:

-   Una nueva interfaz de usuario simplificada
-   Se ha mejorado la prueba de varios usuarios, que ya no requiere la configuración de una segunda cuenta de usuario.

 

 