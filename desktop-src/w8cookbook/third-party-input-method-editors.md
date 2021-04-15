---
title: Editores de métodos de entrada de terceros
description: Editores de métodos de entrada de terceros
ms.assetid: 7FFD7210-2335-4499-A36A-ACFAECEB01F9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca9768de96b9dcdeac7f4b0da210f7aa788801b
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "104554363"
---
# <a name="third-party-input-method-editors"></a>Editores de métodos de entrada de terceros

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

Los editores de métodos de entrada (IME) son componentes de software que permiten a los usuarios escribir texto en un idioma que tenga más caracteres de los que se pueden representar en un teclado. (Esto es habitual, pero no se limita a los idiomas de Asia oriental). En lugar de cada carácter individual que aparece en una sola clave, los usuarios escriben combinaciones de claves que, a continuación, el IME interpreta. El IME genera el carácter que coincide con el conjunto de trazos de tecla y, a veces, presenta al usuario una lista de los posibles caracteres que se deben seleccionar y, a continuación, inserta el carácter en la ventana de control de edición de la aplicación del usuario.

En el pasado, Windows permitía ejecutar IME de terceros en el sistema de Windows y esta funcionalidad continúa para Windows 8. Los usuarios pueden instalar un IME de terceros y usarlo. Además, estamos consolidando el sistema y los procesos para evitar los IME malintencionados, mejorar la seguridad y mejorar la experiencia del usuario.

En Windows 8, encontrará:

-   Compatibilidad de IME de terceros con teclados de hardware y teclados táctiles
-   Los proveedores de IME de terceros deben seguir las directrices de Microsoft para desarrollar sus IME para Windows 8
-   Los IME de terceros deben estar firmados digitalmente
-   Los IME de terceros deben ser compatibles con el marco de trabajo de servicios de texto (TSF) y las marcas de IME adecuadas deben configurarse para que se ejecuten correctamente en Windows 8.
-   Los IME de terceros heredados podrán ejecutarse en aplicaciones de escritorio, pero se bloquearán en aplicaciones de la tienda Windows.
-   Los IME de terceros pueden usar la distribución de teclado táctil proporcionada por Windows para vincular su IME, de modo que los usuarios puedan usar su IME con teclados táctiles. Sin embargo, algunas funciones de los IME integrados para los teclados táctiles no estarán disponibles para los IME de terceros.
-   Windows Defender quitará los IME malintencionados del sistema de Windows

## <a name="manifestation"></a>Manifestación

**Cambios en el idioma de entrada y en el método de entrada**

En lugar de Mostrar todos los iconos del modo IME junto con el icono de personalización de marca del IME, solo se muestra un icono de modo IME junto con el icono de personalización de marca del IME. Las dos figuras siguientes muestran el control flotante de entrada de Windows 8 y el control flotante de IME, con el IME japonés como el método de entrada actual. Si hace clic en el icono de personalización de marca del IME, puede cambiar los métodos de entrada.

![cambiar métodos de entrada](images/inputindicator2.png)

Si hace clic en el icono del modo IME, puede cambiar a un modo IME diferente.

![cambiar los modos IME](images/inputindicator1.png)

Si un IME se basa en la barra de idioma para mostrar sus iconos de modo en Windows 7, el IME debe cambiarse para mostrar su icono de personalización de marca y el icono de modo en el indicador de entrada en Windows 8.

> [!Note]  
> Nota: los detalles sobre cómo un IME puede mostrar el icono de personalización de marca y el icono de modo en el SysTray en la barra de tareas del escritorio se documentarán y publicarán públicamente en las directrices de Windows 8 IME.

 

**Nuevo entorno de Windows**

El entorno de Windows 8 cambia el panorama de los IME. Los conceptos de las aplicaciones de la tienda Windows, los contenedores de aplicaciones de contexto local y las restricciones de API en los IME no estaban presentes en Windows 7. Algunos IME existentes de Windows 7 dejan de responder cuando se ejecutan dentro de una aplicación de la tienda Windows y, por tanto, no permiten que los IME heredados se ejecuten dentro de aplicaciones de la tienda Windows Además, asegúrese de que se validan las nuevas versiones de los IME para asegurarse de que son compatibles con el nuevo entorno de interfaz de usuario antes de que se ejecuten dentro de las aplicaciones de la tienda Windows.

## <a name="mitigation"></a>Mitigación

Puede usar un IME compatible con el escritorio en el sistema. Esta es la mejor opción si usa principalmente aplicaciones de escritorio y desea seguir usando un IME heredado preferido para la entrada. Se recomienda usar un IME de Windows 8 y dejar de usar IME heredado o no certificado. Las notificaciones son proporcionadas por el CPL del lenguaje y el modificador de entrada para avisarle de los efectos del uso de un IME compatible con el escritorio.

Verá cualquiera de los siguientes comportamientos si un IME compatible con el escritorio no funciona en el sistema:

-   La interfaz de usuario del CPL de idioma etiqueta los IME compatibles con el escritorio y muestra un mensaje que indica que los IME no compatibles solo funcionan en aplicaciones de escritorio.
-   El control flotante de entrada atenúa los IME compatibles con el escritorio cuando el usuario está dentro de las aplicaciones de la tienda Windows. Esto indica que el IME no funciona en esta aplicación. (En el escritorio, los IME compatibles con el escritorio no están atenuados). Si cambia a aplicaciones de la tienda Windows con un IME no compatible y observa que el IME está desactivado, use el indicador de entrada para cambiar a un IME compatible con aplicaciones de la tienda Windows.

Los IME heredados o compatibles con el escritorio se limitan a estas condiciones:

-   Actualización de Windows 7 a Windows 8, con IME de terceros en el sistema
-   El proveedor no ha publicado una versión compatible con Windows 8 y el usuario intenta usar una versión existente de Windows 7 mientras tanto

## <a name="solution"></a>Solución

**General**

Use la infraestructura de Text Services Framework (TSF) existente para implementar la lógica del IME y los controles comunes de la aplicación de la tienda Windows para las ius. Cree ventanas de propiedad para hospedar su interfaz de usuario.

Se están agregando nuevas API de búsqueda para mejorar la predicción de búsqueda y proporcionar una experiencia de búsqueda más limpia en la interfaz de usuario.

También se agregan API para notificar a los IME de terceros cuando se invoca un teclado táctil para impedir que la interfaz de usuario esté incluida en el teclado táctil. Una distribución de teclado táctil clásica predeterminada se carga automáticamente para los IME de terceros. No es necesario realizar ningún trabajo adicional para integrar con esta distribución clásica del teclado táctil. Sin embargo, los IME de terceros podrán solicitar un diseño táctil alternativo.

Familiarícese con las directrices del IME de Windows 8 para poder promocionar los principios clave de la experiencia del usuario de la aplicación de la tienda Windows en el IME. Los IME que se adhieren a las instrucciones deben establecer una marca para indicar que el IME es compatible con el diseño de Microsoft. Windows 8 impide que todos los IME compatibles con el escritorio se ejecuten en aplicaciones de la tienda Windows.

La firma digital, además de la revocación de Windows Defender, impide que los IME malintencionados se instalen en el sistema de Windows 8. Tras la comprobación de la identidad, el archivo. dll de un IME de terceros está firmado digitalmente. Solo los IME que tienen esta firma digital se pueden instalar en el sistema sin que aparezca un mensaje de advertencia crítico para el usuario. Los usuarios pueden notificar a los IME malintencionados. Una vez que se ha determinado que un IME es malintencionado, Windows defender lo quita del sistema de Windows.

**Text Services Framework (TSF)**

El IME debe ser compatible con TSF para poder ejecutarse en Windows 8. Windows 8 impide que los IME no compatibles con TSF se ejecuten en aplicaciones de la tienda Windows. Cuando se inicia una aplicación, TSF carga el IME. dll para el IME que el usuario ha seleccionado en el proceso de la aplicación.

> [!Note]  
> Para proporcionar funcionalidad o ius independientes entre las aplicaciones de la tienda Windows y las aplicaciones de escritorio, el archivo. dll cargado por TSF puede comprobar en qué tipo de aplicación se está cargando. El IME llama al método [ITfThreadMgrEx:: GetActiveFlags](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags) y comprueba la \_ marca TF TMF \_ IMMERSIVEMODE, y puede desencadenar una lógica de aplicación diferente en función del resultado.

 

Cuando se carga un IME en una aplicación de la tienda Windows, está sujeto a las mismas restricciones de contenedor de la aplicación que la propia aplicación. Este comportamiento garantiza que los IME no pueden infringir los contratos de seguridad de las aplicaciones de la tienda Windows, a pesar de tener acceso al SDK de escritorio (porque no están distribuidos ni certificados por la tienda Windows). Algunas funciones que los IME realizan actualmente se ven afectadas dentro de un contenedor de la aplicación. Estas funciones incluyen:

-   Archivos de Diccionario
-   Actualización de Internet
-   Aprendizaje sobre la marcha
-   Compartir información entre procesos

Consulte las directrices de Windows 8 IME para obtener más información.

Los IME heredados no funcionan en las aplicaciones de la tienda Windows para evitar la posibilidad de que se produzcan experiencias de usuario incorrectas, incluidas las interrupciones del sistema. Los IME que son compatibles con las aplicaciones de la tienda Windows deben declararse automáticamente estableciendo una marca que indique esta compatibilidad. Este marcador lo proporciona TSF en la estructura TF \_ INPUTPROCESSORPROFILE. Los detalles sobre cómo usar esta marca para declarar un IME de terceros como compatible con aplicaciones de la tienda Windows se documentarán y publicarán de forma pública en las directrices de Windows 8 IME.

Los IME que son compatibles con las aplicaciones de la tienda Windows pueden ejecutarse en aplicaciones de escritorio o en aplicaciones de la tienda Windows. Los IME que no son compatibles solo se pueden ejecutar en procesos de escritorio.

**Interfaz de usuario**

Aunque los IME de terceros tienen acceso a las API de ventanas de escritorio, deben seguir las mismas restricciones de la API de Windows que la aplicación en la que se ejecutan. Por ejemplo, un IME no puede dibujar en la parte superior de una aplicación de la tienda Windows mientras esté activo en una aplicación de escritorio. Las restricciones de API se destinan a evitar estos escenarios:

-   Aplicaciones de escritorio que toman el foco de las aplicaciones de la tienda Windows
-   Dibujo de aplicaciones de escritorio en la aplicación de la tienda Windows
-   Aplicaciones de escritorio que interfieren con las aplicaciones de la tienda Windows

**Compatibilidad con teclado táctil**

Aunque la compatibilidad con el teclado táctil (TKB) sigue estando disponible para los proveedores de IME de terceros, una experiencia de teclado táctil totalmente personalizable e integrada no se proporciona en Windows 8. Sin embargo, los IME de terceros pueden asignar sus IME con la distribución de teclado optimizada para Touch. El panel de entrada de software (SIP) de Windows proporciona una distribución de teclado clásica de forma predeterminada para los IME de terceros. Dado que el teclado clásico genera eventos clave similares a la de un teclado de hardware, actualmente no hay ningún requisito de implementación especial para que los IME de terceros funcionen con un teclado táctil. El control de entrada para los eventos de clave de hardware también controlará los eventos clave de los diseños táctiles clásicos.

> [!Note]  
> Nota: es posible que los IME deban empezar a controlar los eventos de entrada Unicode si se amplía la compatibilidad con TKB para incluir también los diseños de teclado optimizados.

 

Un IME de terceros puede elegir usar la distribución de teclado optimizada para su IME. Para obtener más información, consulte la guía del IME de terceros.

Asegúrese de que la interfaz de usuario del panel candidato (y otros elementos de la interfaz de usuario) no se dibujen debajo del teclado táctil. En la mayoría de los casos, la aplicación debe cambiar el tamaño de su ventana para que tenga en cuenta el teclado táctil. Sin embargo, si una aplicación no hace esto, los IME pueden seguir usando la API InputPaneFramework para obtener información sobre la posición del teclado táctil. Los IME de terceros pueden usar esta API para obtener el espacio de pantalla utilizado por el teclado táctil antes de dibujar las ius candidatas (u otras) y redistribuir la interfaz de usuario para evitar que se dibuje debajo del teclado táctil.

**Buscándol**

En Windows 8, las aplicaciones de la tienda Windows pueden proporcionar fácilmente a sus usuarios características de búsqueda implementando el [contrato de búsqueda](/previous-versions/windows/apps/hh464906(v=win.10)) e integrando con el panel de búsqueda. El panel de búsqueda es una ubicación central para que los usuarios realicen búsquedas en todas sus aplicaciones. Windows ayuda a las aplicaciones que usan el panel de búsqueda a que los usuarios quieran ir lo más rápido posible. En concreto, para los usuarios de IME, proporciona una experiencia de búsqueda única que permite a los IME compatibles integrarse con Windows 8 para mayor eficacia y facilidad de uso.

Un IME es compatible con la experiencia de búsqueda integrada si cumple estos criterios:

-   Es compatible con el entorno de aplicaciones de la tienda Windows
-   Implementa las API del modo UILess de TFS
-   Implementa las API de integración de búsqueda de TFS:
-   -   ItfSearchCandidateProvider
    -   ItfSearchHardwareKeyboardBehaviors

Cuando se activa en el panel de búsqueda, el IME compatible se coloca en modo UILess y no puede mostrar su interfaz de usuario. En su lugar, envía candidatos de conversión a Windows, que después los mostrará en el control de lista de candidatos en línea.

El IME también envía candidatos de Windows que deben usarse para ejecutar la búsqueda actual: estos candidatos podrían ser los mismos que los candidatos de conversión o se pueden personalizar para la búsqueda. Los buenos candidatos de búsqueda cumplen estos criterios:

-   Sin superposición de prefijo
-   Ningún candidato de predicción (solo finalización)

Los IME que no cumplen los criterios y que no son compatibles con la búsqueda se muestran de la misma manera que en otros controles de aplicación de la tienda Windows y no pueden aprovechar las ventajas de la integración de la interfaz de usuario y los candidatos de búsqueda. (Las aplicaciones reciben consultas solo después de que el usuario haya terminado de redactar).

Cuando una aplicación que admite el contrato de búsqueda recibe una consulta, el evento de consulta incluirá una matriz "queryTextAlternatives" que contenga todas las alternativas conocidas, clasificadas desde la más relevante (probablemente) hasta la menos relevante (improbable). Cada vez que se proporcionan alternativas, la aplicación debe tratar cada alternativa como una consulta y devolver todos los resultados que coincidan con cualquiera de las alternativas (como si el usuario hubiera emitido varias consultas al mismo tiempo), y en esencia emitir una consulta "or" para el servicio que proporciona los resultados. Para mejorar el rendimiento, las aplicaciones a menudo limitarán la coincidencia a las 10 alternativas más relevantes.

**Firma digital de IME**

Todos los IME de terceros deben estar firmados digitalmente para instalarse en el sistema de Windows 8 como un IME. Con SmartScreen, los usuarios pueden ver un mensaje de advertencia al descargar un IME sin firmar de la Web. Para obtener un certificado y firmar los archivos:

-   **Usar una firma Authenticode para firmar programas digitalmente**
    -   Obtener un certificado de firma de código Authenticode válido de una de las muchas entidades de certificación compatibles con Windows
    -   Usar herramientas de desarrollo (como [signtool.exe](../seccrypto/signtool.md)) para firmar las aplicaciones antes de la distribución
    -   Para obtener más información y una descripción paso a paso del proceso de firma de código, vea la entrada de blog [todo lo que necesita saber sobre la firma de código de Authenticode](/archive/blogs/ieinternals/everything-you-need-to-know-about-authenticode-code-signing) .
-   **Asegúrese de que las descargas no se detectan como malware**
    -   Los programas descargados detectados y confirmados como malware afectan tanto a la reputación de la descarga como a la reputación del certificado digital que se usa para firmar el archivo.
-   **Solicitar certificación de Windows**
    -   Visite la página de certificación de aplicaciones de Windows en MSDN

Para obtener más información, consulte estos artículos sobre firmas digitales y firma de código:

-   [Información general sobre Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Garantizar la integridad y la autenticidad](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Procedimientos recomendados para la firma de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [¿Qué son los certificados digitales?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

Si un IME **no está** firmado, el usuario recibe este mensaje de advertencia cuando intenta descargar el IME:

![mensaje de advertencia de IME no firmado](images/downloadwarning02-fhu-ivu.png)

Si un IME está firmado, los usuarios verán este mensaje en su lugar:

![mensaje firmado de IME](images/downloadwarning01-fhu-vcu.png)

En función de estas notificaciones, los usuarios pueden elegir si desea eliminar el archivo o pasar por alto la advertencia y ejecutar el programa descargado.

**Revocación de IME**

Los IME que son malintencionados o que no siguen las directrices del IME de Windows 8 se pueden quitar del sistema mediante Windows Defender. Para obtener más información acerca de los IME malintencionados, consulte el artículo sobre los [IME de terceros en Windows 8](/previous-versions/windows/apps/hh967426(v=win.10)).

## <a name="resources"></a>Recursos

-   [ITfThreadMgrEx:: get Active Flags (método)](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags)
-   [SignTool](../seccrypto/signtool.md)
-   [Todo lo que necesita saber sobre la firma de código de Authenticode](https://blogs.msdn.com/b/ieinternals/archive/2011/03/22/authenticode-code-signing-for-developers-for-file-downloads-building-smartscreen-application-reputation.aspx)
-   [Contratos y extensiones de aplicaciones de Windows](/previous-versions/windows/apps/hh464906(v=win.10))
-   [Requisitos de certificación para aplicaciones de escritorio de Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [Requisitos de certificación para aplicaciones de Windows](https://msdn.microsoft.com/library/windows/apps/51A7C609-94AB-49ab-B8E0-F26FF776DDB4.aspx)
-   [Uso del Kit para la certificación de aplicaciones en Windows](../win_cert/using-the-windows-app-certification-kit.md)
-   [Información general sobre Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Garantizar la integridad y la autenticidad](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)#Ensuring_Integrity_a)
-   [Procedimientos recomendados para la firma de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [¿Qué son los certificados digitales?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

 

 