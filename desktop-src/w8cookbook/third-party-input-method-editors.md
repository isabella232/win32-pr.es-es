---
title: Editores de métodos de entrada de terceros
description: Editores de métodos de entrada de terceros
ms.assetid: 7FFD7210-2335-4499-A36A-ACFAECEB01F9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e12b2c2788ed95509b785dd7fc2c5ba3ec0a31ac46a736bc7dfdc92c7289f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815124"
---
# <a name="third-party-input-method-editors"></a>Editores de métodos de entrada de terceros

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

Los editores de métodos de entrada (IME) son componentes de software que permiten a un usuario escribir texto en un idioma con más caracteres de los que se pueden representar en un teclado. (Esto es común, pero no se limita a los idiomas de Asia Oriental). En lugar de cada carácter individual que aparece en una sola clave, los usuarios escriben combinaciones de claves que luego interpreta el IME. El IME genera el carácter que coincide con el conjunto de trazos clave, a veces presenta al usuario una lista de posibles caracteres entre los que elegir y, a continuación, inserta el carácter en la ventana de control de edición de la aplicación del usuario.

En el pasado, Windows permite que los IME de terceros se ejecuten en el sistema Windows y esta funcionalidad continúa durante Windows 8. Los usuarios pueden instalar un IME de terceros y usarlo. Además, vamos a reforzar el sistema y los procesos para evitar EME malintencionadas, mejorar la seguridad y mejorar la experiencia del usuario.

En Windows 8, encontrará:

-   Compatibilidad con IME de terceros para teclados de hardware y teclados táctiles
-   Los proveedores de IME de terceros deben seguir las directrices de Microsoft para desarrollar sus EME para Windows 8
-   Los IME de terceros deben estar firmados digitalmente
-   Los EME de terceros deben ser Text Services Framework (TSF) y las marcas de IME adecuadas deben establecerse para que se ejecuten correctamente en Windows 8
-   Los EME de terceros heredados se podrán ejecutar en aplicaciones de escritorio, pero se bloquearán en Windows Store
-   Los EME de terceros pueden usar el diseño de teclado táctil proporcionado por Windows para vincular su IME, de modo que los usuarios puedan usar su IME con teclados táctiles. Sin embargo, ciertas funciones de LOS EME de entrada para teclados táctiles no estarán disponibles para los EME de terceros.
-   Windows Defender quitará los IME malintencionados del sistema de Windows.

## <a name="manifestation"></a>Manifestación

**Cambios en el idioma de entrada y el modificador del método de entrada**

En lugar de mostrar todos los iconos de modo IME junto con el icono de personal de marca de IME, solo se muestra un icono de modo IME junto con el icono de personal de marca de IME. Las dos cifras siguientes muestran el Windows 8 de entrada y el control flyout IME, con el IME japonés como método de entrada actual. Si hace clic en el icono de personal de marca de IME, puede cambiar los métodos de entrada.

![métodos de entrada switch](images/inputindicator2.png)

Si hace clic en el icono de modo IME, puede cambiar a otro modo IME.

![cambiar los modos de ime](images/inputindicator1.png)

Si un IME se basa en la barra de idioma para mostrar sus iconos de modo en Windows 7, el IME debe cambiarse para mostrar su icono de personal de marca y el icono de modo en el indicador de entrada en Windows 8.

> [!Note]  
> Nota: Los detalles sobre cómo un IME puede mostrar su icono de marca y el icono de modo en sysTray en la barra de tareas del escritorio se documentarán y publicarán públicamente en las directrices de Windows 8 IME.

 

**Nuevo Windows de datos**

El entorno de Windows 8 cambia el panorama de los IME. Los conceptos de Windows Store, los contenedores de aplicaciones de contexto local y las restricciones de API en los IME no estaban presentes en Windows 7. Algunas aplicaciones existentes Windows 7 IME dejan de responder cuando se ejecutan dentro de una aplicación de Windows Store y, por tanto, no permiten que los IME heredados se ejecuten dentro de Windows Store. Además, asegúrese de que las nuevas versiones de los IME se validan para asegurarse de que son compatibles con el nuevo entorno de interfaz de usuario antes de que se ejecuten dentro de Windows Store.

## <a name="mitigation"></a>Mitigación

Puede usar un IME compatible con el escritorio en el sistema. Esta podría ser la mejor opción si usa principalmente aplicaciones de escritorio y desea seguir usando un IME heredado preferido para la entrada. Se recomienda usar un Windows 8 IME y dejar de usar EME heredadas o no certificadas. El CPL de lenguaje y el conmutador de entrada proporcionan notificaciones para advertirle de los efectos del uso de un IME compatible con el escritorio.

Verá cualquiera de los comportamientos siguientes si un IME compatible con el escritorio no funciona en el sistema:

-   La interfaz de usuario de CPL del lenguaje etiqueta los IME compatibles con el escritorio y muestra un mensaje que indica que los IME no compatibles solo funcionan en aplicaciones de escritorio.
-   El control desplegable de entrada desancha los IME compatibles con el escritorio cuando el usuario está dentro Windows aplicaciones de la Tienda. Esto indica que el IME no funciona en esta aplicación. (En el escritorio, los IME compatibles con el escritorio no están en gris). Si cambia a Windows Store con un IME no compatible y se da cuenta de que el IME está desactivado, use el indicador de entrada para cambiar a un IME compatible con las aplicaciones de Windows Store.

Las EME heredadas o compatibles con el escritorio se limitan a estas condiciones:

-   Actualización de Windows 7 a Windows 8, con EME de terceros en el sistema
-   El proveedor no ha publicado una versión compatible con Windows 8 y el usuario intenta usar una versión Windows 7 mientras tanto

## <a name="solution"></a>Solución

**General**

Use la infraestructura de marco de servicios de texto (TSF) existente para implementar la lógica de IME y los controles comunes de la aplicación Windows Store para las especificaciones de usuario. Cree ventanas propias para hospedar la interfaz de usuario.

Se están agregando nuevas API de búsqueda para mejorar la predicción de búsqueda y proporcionar una experiencia de búsqueda más limpia en la interfaz de usuario.

También se están agregando API para notificar a los EME de terceros cuando se invoca un teclado táctil para proteger la interfaz de usuario frente a la cobertura del teclado táctil. Se carga automáticamente un diseño de teclado táctil clásico predeterminado para los EME de terceros. No se necesita ningún trabajo adicional para la integración con este diseño de teclado táctil clásico. Sin embargo, los EME de terceros podrán solicitar un diseño táctil alternativo.

Familiarícese con las Windows 8 de IME para que pueda promover los principios clave de experiencia del usuario de la aplicación Windows Store en el IME. Los EME que cumplan las directrices deben establecer una marca para indicar que el IME es compatible con el diseño de Microsoft. Windows 8 impide que todos los IME compatibles con el escritorio se ejecuten en Windows Store.

La firma digital, además de la revocación por Windows Defender, impide que los IME malintencionados se instalen en Windows 8 sistema. Tras la comprobación de la identidad, la firma de un .dll IME de terceros se firma digitalmente. Solo los IME que tienen esta firma digital se pueden instalar en el sistema sin que aparezca un mensaje de advertencia crítico para el usuario. Los usuarios pueden notificar imes malintencionados. Una vez que se ha determinado que un IME es malintencionado, Windows Defender lo quita del Windows sistema.

**Text Services Framework (TSF)**

El IME debe tener en cuenta TSF para poder ejecutarse en Windows 8. Windows 8 impide que los IME que no son compatibles con TSF se ejecuten en Windows Store. Cuando se inicia una aplicación, TSF carga el .dll IME para el IME que el usuario ha seleccionado en el proceso de aplicación.

> [!Note]  
> Para proporcionar funcionalidad o URI independientes entre las aplicaciones de Windows Store y las aplicaciones de escritorio, el .dll cargado por TSF puede comprobar en qué tipo de aplicación se carga. El IME llama al método [ITfThreadMgrEx::GetActiveFlags,](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags) comprueba la marca TF TMF IMMERSIVEMODE y puede desencadenar una lógica de aplicación diferente en función del \_ \_ resultado.

 

Cuando se carga un IME en una aplicación Windows Store, está sujeto a las mismas restricciones de contenedor de aplicaciones que la propia aplicación. Este comportamiento garantiza que los IME no puedan infringir los contratos de seguridad de aplicaciones de Windows Store, a pesar de tener acceso al SDK de escritorio (porque no están distribuidos ni certificados por Windows Store). Algunas funciones que realizan actualmente los IME se ven afectadas dentro de un contenedor de aplicaciones. Estas funciones incluyen:

-   Archivos de diccionario
-   Actualización de Internet
-   Aprendizaje sobre la marcha
-   Uso compartido de información entre procesos

Consulte las Windows 8 IME guidelines (Directrices de IME) para obtener más información.

Los IME heredados no funcionan en Windows store para evitar la posibilidad de experiencias de usuario negativas, incluidas las detenciones del sistema. Los IME que son compatibles con Windows store deben declararse por sí solos estableciendo una marca que indique esta compatibilidad. TSF proporciona esta marca en la estructura \_ INPUTPROCESSORPROFILE de TF. Los detalles sobre cómo usar esta marca para declarar un IME de terceros como compatible con aplicaciones de Windows Store se documentarán y publicarán públicamente en las directrices de Windows 8 IME.

Los IME que son compatibles con Windows Store pueden ejecutarse en aplicaciones de escritorio o Windows store. Los IME que no son compatibles solo se pueden ejecutar en procesos de escritorio.

**Interfaz de usuario**

Aunque los IME de terceros tienen acceso a las API de ventanas de escritorio, deben seguir las mismas restricciones de LA API de ventana que la aplicación en la que se ejecutan. Por ejemplo, un IME no se puede dibujar sobre una aplicación Windows Store mientras está activa en una aplicación de escritorio. Las restricciones de API están destinadas a evitar estos escenarios:

-   Aplicaciones de escritorio centradas en Windows Store
-   Aplicaciones de escritorio dibujadas en Windows Store
-   Aplicaciones de escritorio que interfieren con Windows Store

**Compatibilidad con teclado táctil**

Aunque la compatibilidad con el teclado táctil (TKB) sigue estando disponible para proveedores de IME de terceros, no se proporciona una experiencia de teclado táctil totalmente personalizable e integrada en Windows 8. Sin embargo, los EME de terceros pueden asignar sus EME con el diseño de teclado optimizado para el toque. El panel Windows entrada flexible (SIP) proporciona un diseño de teclado clásico de forma predeterminada para los IME de terceros. Dado que el teclado clásico genera eventos clave similares a los de un teclado de hardware, actualmente no hay ningún requisito de implementación especial para que los EME de terceros funcionen con un teclado táctil. El control de entrada para los eventos de clave de hardware también controlará los eventos clave de los diseños táctiles clásicos.

> [!Note]  
> Nota: Es posible que los EME deba empezar a controlar los eventos de entrada Unicode si se amplía la compatibilidad con TKB para incluir también diseños de teclado optimizados.

 

Un IME de terceros puede optar por usar el diseño de teclado optimizado para su IME. Consulte la guía de IME de terceros para obtener más información.

Asegúrese de que la interfaz de usuario del panel candidato (y otros elementos de la interfaz de usuario) no se dibujan debajo del teclado táctil. En la mayoría de los casos, la aplicación debe cambiar el tamaño de su ventana para tener en cuenta el teclado táctil. Sin embargo, si una aplicación no lo hace, los IME todavía pueden usar inputPaneFramework API para aprender la posición del teclado táctil. Los IME de terceros pueden usar esta API para obtener el espacio de pantalla consumido por el teclado táctil antes de dibujar las IU candidatas (u otras) y volver a flujo de su interfaz de usuario para evitar dibujar debajo del teclado táctil.

**Buscando**

En Windows 8, Windows Store puede proporcionar fácilmente a sus usuarios características de [](/previous-versions/windows/apps/hh464906(v=win.10)) búsqueda mediante la implementación del contrato de búsqueda y la integración con el panel De búsqueda. El panel Búsqueda es una ubicación central para que los usuarios realicen búsquedas en todas sus aplicaciones. Windows ayuda a las aplicaciones que usan el panel De búsqueda a obtener a sus usuarios dónde quieren ir lo más rápido posible. En concreto, para los usuarios de IME, proporciona una experiencia de búsqueda única que permite que los IME compatibles se integren con el Windows 8 para una mayor eficacia y facilidad de uso.

Un IME es compatible con la experiencia de búsqueda integrada si cumple estos criterios:

-   Es compatible con el entorno de Windows Store
-   Implementa las API de modo sin interfaz de usuario de TFS
-   Implementa las API de integración de búsqueda de TFS:
-   -   ItfSearchCandidateProvider
    -   ItfSearchHardwareKeyboardBehaviors

Cuando se activa en el panel Buscar, el IME compatible se coloca en modo sin interfaz de usuario y no puede mostrar su interfaz de usuario. En su lugar, envía candidatos de conversión a Windows, que luego los mostrarán en el control de lista de candidatos en línea.

El IME también envía Windows candidatos que se deben usar para ejecutar la búsqueda actual: estos candidatos podrían ser los mismos que los candidatos de conversión o podrían adaptarse para la búsqueda. Los candidatos de búsqueda buenos cumplen estos criterios:

-   Sin superposición de prefijo
-   Sin candidato de predicción (solo finalización)

Los IME que no cumplen los criterios y no son compatibles con la búsqueda se muestran de la misma manera que en otros controles de aplicación de Windows Store y no pueden aprovechar la integración de la interfaz de usuario y los candidatos de búsqueda. (Las aplicaciones reciben consultas solo después de que el usuario haya terminado de crear).

Cuando una aplicación que admite el contrato de búsqueda recibe una consulta, el evento de consulta incluirá una matriz "queryTextAlternatives" que contiene todas las alternativas conocidas, clasificadas de la más relevante (probablemente) a la menos relevante (improbable). Cada vez que se proporcionan alternativas, la aplicación debe tratar cada alternativa como una consulta y devolver todos los resultados que coincidan con cualquiera de las alternativas (como si el usuario hubiera emitido varias consultas al mismo tiempo), emitiendo básicamente una consulta "o" al servicio que proporciona los resultados. Para mejorar el rendimiento, las aplicaciones suelen limitar la coincidencia con las 10 alternativas más relevantes.

**Firma digital de IME**

Todos los IME de terceros deben estar firmados digitalmente para poder instalarse en el Windows 8 como un IME. Con SmartScreen, los usuarios pueden ver un mensaje de advertencia al descargar un IME sin signo desde la web. Para obtener un certificado y firmar los archivos:

-   **Uso de una firma Authenticode para firmar digitalmente programas**
    -   Obtenga un certificado de firma de código Authenticode válido de una de las muchas autoridades de certificación admitidas por Windows
    -   Uso de herramientas de desarrollo [ (comosigntool.exe](../seccrypto/signtool.md)) para firmar las aplicaciones antes de la distribución
    -   Para obtener más información y una descripción paso a paso del proceso de firma de código, vea la entrada de blog Everything you need to know about Authenticode code signing (Todo lo que necesita saber sobre la firma de código [Authenticode).](/archive/blogs/ieinternals/everything-you-need-to-know-about-authenticode-code-signing)
-   **Asegurarse de que las descargas no se detectan como malware**
    -   Los programas descargados que se detectan y confirman como malware afectan a la reputación de la descarga y a la reputación del certificado digital usado para firmar ese archivo.
-   **Solicitud de certificación Windows certificado**
    -   Visite la página Windows certificación de aplicaciones en MSDN

Para más información, consulte estos artículos sobre firmas digitales y firma de código:

-   [Información general sobre Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Garantía de integridad y autenticidad](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Procedimientos recomendados de firma de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [¿Qué son los certificados digitales?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

Si un IME **no está firmado,** el usuario recibe este mensaje de advertencia cuando intenta descargar el IME:

![ime is not signed warning message](images/downloadwarning02-fhu-ivu.png)

Si un IME está firmado, los usuarios ven este mensaje en su lugar:

![ime is signed message](images/downloadwarning01-fhu-vcu.png)

En función de estas notificaciones, los usuarios pueden elegir si eliminar el archivo o omitir la advertencia y ejecutar el programa descargado.

**Revocación de IME**

Los IME que son malintencionados o que no siguen las Windows 8 de IME se pueden quitar del sistema mediante Windows Defender. Para obtener más información sobre los IME malintencionados, consulte el artículo sobre los [IME](/previous-versions/windows/apps/hh967426(v=win.10))de terceros en Windows 8 .

## <a name="resources"></a>Recursos

-   [ITfThreadMgrEx::Get Active Flags (Método)](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags)
-   [SignTool](../seccrypto/signtool.md)
-   [Todo lo que necesita saber sobre la firma de código Authenticode](https://blogs.msdn.com/b/ieinternals/archive/2011/03/22/authenticode-code-signing-for-developers-for-file-downloads-building-smartscreen-application-reputation.aspx)
-   [Windows contratos de aplicación y extensiones](/previous-versions/windows/apps/hh464906(v=win.10))
-   [Requisitos de certificación para Windows 8 aplicaciones de escritorio](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [Requisitos de certificación para Windows aplicaciones](https://msdn.microsoft.com/library/windows/apps/51A7C609-94AB-49ab-B8E0-F26FF776DDB4.aspx)
-   [Uso del Kit para la certificación de aplicaciones en Windows](../win_cert/using-the-windows-app-certification-kit.md)
-   [Información general sobre Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Garantía de integridad y autenticidad](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)#Ensuring_Integrity_a)
-   [Procedimientos recomendados de firma de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [¿Qué son los certificados digitales?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

 

 