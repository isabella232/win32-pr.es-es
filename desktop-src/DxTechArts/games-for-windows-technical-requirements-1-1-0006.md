---
title: 'Requisitos técnicos de Games for Windows: procedimientos recomendados para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8'
description: En este artículo se proporcionan los requisitos técnicos y los procedimientos recomendados para los juegos que se ejecutan en Windows.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e38b9476a4ab2aad5edc6210f55bc4d2b85845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793684"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Juegos para requisitos técnicos de Windows: prácticas recomendadas para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8

En este artículo se proporcionan los requisitos técnicos y los procedimientos recomendados para los juegos que se ejecutan en Windows. Hemos escrito estos requisitos técnicos y prácticas recomendadas principalmente para tratar Windows Vista y Windows 7, así como el sistema operativo Windows XP heredado. Estos procedimientos recomendados también se aplican generalmente a juegos de Win32 de escritorio en Windows 8.

Este artículo contiene estas secciones:

-   [Diferencias para Windows 8](#differences-for-windows-8)
    -   [Información adicional](#additional-information)
-   [Juegos para Windows](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [Integración del explorador de juegos de 1,1](#11-games-explorer-integration)
    -   [1,2 compatibilidad con la familia de seguridad y control parental](/windows)
    -   [1,3 admitir juegos guardados enriquecidos](#13-support-rich-saved-games)
    -   [1,4 compatibilidad con el requisito condicional de la consola Xbox 360 Common Controller for Windows \[\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)
    -   [1,5 compatibilidad con varias soluciones y relaciones de aspecto](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [1,6 Inicio de soporte técnico de Windows Media Center](#16-support-launch-from-windows-media-center)
    -   [Compatibilidad con Direct3D 1,7](#17-direct3d-support)
    -   [1,8 habilitar reconocimiento de PPP alto](#18-enable-high-dpi-aware)
-   [Seguridad y compatibilidad](#security-and-compatibility)
    -   [2,1 Siga las directrices de control de cuentas de usuario](#21-follow-user-account-control-guidelines)
    -   [2,2 compatibilidad con versiones x64 de Windows](#22-support-windows-x64-versions)
    -   [Archivos de firma de 2,3](#23-sign-files)
    -   [Controladores de firma de 2,4](#24-sign-drivers)
    -   [2,5 realizar la comprobación de la versión correcta](#25-perform-proper-version-checking)
    -   [2,6 compatibilidad con sesiones de usuario simultáneas](#26-support-concurrent-user-sessions)
    -   [2,7 compatibilidad con nombres largos](#27-support-long-names)
-   [Instalación](#32-support-user-account-control-for-installation)
    -   [3,1 compatibilidad con la instalación sencilla](#31-support-easy-installation)
    -   [3,2 compatibilidad con el control de cuentas de usuario para la instalación](#32-support-user-account-control-for-installation)
    -   [3,3 instalar en carpetas correctas](#33-install-to-correct-folders)
    -   [3,4 instalar los recursos de Windows correctamente](#34-install-windows-resources-properly)
    -   [3,5 evitar reinicios durante la instalación](#35-avoid-reboots-during-installation)
    -   [3,6 usar el control de versiones de archivos correctamente](#36-use-file-versioning-correctly)
    -   [3,7 compatibilidad con el requisito condicional de ejecución automática \[\]](#37-support-autorun-conditional-requirement)
-   [Confiabilidad](#reliability)
    -   [4,1 eliminación de los reinicios innecesarios](#41-eliminate-unnecessary-reboots)
    -   [4,2 eliminación de errores de comprobador de aplicaciones](#42-eliminate-application-verifier-failures)
    -   [4,3 compatibilidad con Informe de errores de Windows e información de versión de archivo](#43-support-windows-error-reporting-and-file-version-information)
-   [Terminología del controlador común de Xbox 360 para Windows](#xbox-360-common-controller-for-windows-terminology)
-   [Directrices para productos de middleware de juegos](#guidelines-for-game-middleware-products)
    -   [Introducción](#introduction)
    -   [Recomendaciones adicionales](#additional-recommendations)
    -   [Juegos para Windows Showcase](#games-for-windows-showcases)
-   [Recursos](#resources)

## <a name="differences-for-windows-8"></a>Diferencias para Windows 8

A continuación se muestra un resumen de las diferencias clave a la hora de aplicar estos requisitos técnicos y prácticas recomendadas a Windows 8.

<dl> <dt>

<span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**La interfaz de usuario del explorador de juegos no es visible**
</dt> <dd>

Todos los juegos que se registran en el [Explorador de juegos](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) aparecen como iconos en la nueva interfaz de usuario de Windows, pero muchos de los metadatos asociados al título ya no están visibles. Todavía usa la herramienta Game Definition File Maker (GDFMAKER.EXE), que ahora está disponible en el kit de desarrollo de software (SDK) de Windows, para crear los metadatos. También se usan los mecanismos existentes para implementar los metadatos. Siga usando Windows 7 para probar el registro del explorador de juegos y compruebe que aparece el icono nueva interfaz de usuario de Windows al instalarlo en Windows 8 (consulte [integración del explorador de juegos de 1,1](#11-games-explorer-integration)).

Para descargar el SDK de Windows 8, consulte [descargas para desarrollar aplicaciones de escritorio](https://msdn.microsoft.com/windows/desktop/aa904949).

</dd> <dt>

<span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**El registro con las API del explorador de juegos sigue siendo el mecanismo para registrar el juego con controles parentales de Windows**
</dt> <dd>

Se recomienda ejecutar la Windows SDK versión de GDFMAKER en la versión de lanzamiento de Windows 8 para asegurarse de que puede rellenar todos los sistemas de clasificación admitidos actualmente.

> [!Note]  
> Esta versión de GDFMAKER requiere .NET 4,0.

 

Consulte [protección de la familia de soporte técnico de 1,2](/windows).

</dd> <dt>

<span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**Ahora hay tres opciones para usar la API de XINPUT en función de sus requisitos.**
</dt> <dd>

XINPUT 1,4 está integrado en Windows 8. Las aplicaciones de la tienda Windows y las aplicaciones Win32 de escritorio pueden usar XINPUT 1,4. Todas las versiones de Windows pueden usar XINPUT 9.1.0 para los controladores comunes simplificados, pero no hay ningún paquete de redistribución con XINPUT 9.1.0. Todas las versiones de Windows también pueden usar la versión del SDK de DirectX existente XINPUT 1,3, que requiere que se implemente DirectSetup.

Consulte [1,4 compatibilidad con el controlador común de Xbox 360 para Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).

</dd> <dt>

<span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**En Windows RT solo se admite un conjunto limitado de aplicaciones de escritorio de Win32.**
</dt> <dd>

Los juegos que se ejecutan en Windows 7 se pueden ejecutar correctamente en plataformas Windows 8 x86 y x64.

Consulte [compatibilidad con versiones de Windows x64 de 2,2](#22-support-windows-x64-versions).

</dd> <dt>

<span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Asegurarse de que las comprobaciones del sistema operativo se realicen correctamente**
</dt> <dd>

La versión del sistema operativo Windows 8 es 6,2. Windows 8 pasa las pruebas de la barra mínima actual que se recomiendan para la implementación de juegos.

</dd> <dt>

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**El paquete de redistribución de End-User de DirectX se ejecuta correctamente en Windows 8, como en Windows 7, para implementar D3DX9, D3DX10, D3DX11, XINPUT 1,3, XAUDIO 2,7, XACTEngine, etc.**
</dt> <dd>

Sin embargo, existe un problema conocido con DirectSetup en sistemas que solo tienen instalado .NET 4,0 debido al control de la implementación de los ensamblados de DirectX 1,1 administrados heredados. Este problema se aplica a Windows 8, que se incluye de forma predeterminada en .NET 4,5, y equipos con Windows XP actualizados con el tiempo de ejecución de .NET 4,0 instalado. Sin embargo, este problema no se aplica a ninguna versión de .NET anterior a .NET 4,0. Aunque Windows 8 tiene un comportamiento de compatibilidad de aplicaciones para resolver este problema automáticamente (lo que requiere acceso a la red), se recomienda que los juegos que continúan implementando DirectSetup se actualicen a la versión actualizada del SDK de DirectX (2010 de junio) de los archivos de redistribución. Como siempre, si usa DirectSetup para su título, recorte el título hasta el conjunto mínimo necesario de Cab.

Consulte [3,4 instalar los recursos de Windows correctamente](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Los juegos que requieren el tiempo de ejecución compatible con .NET 2,0 (2,0, 3,0, 3,5) siguen usando los mecanismos de implementación existentes**
</dt> <dd>

Estos juegos desencadenan un comportamiento de compatibilidad de aplicaciones en Windows 8 para habilitar el tiempo de ejecución de .NET 3,5 automáticamente (que requiere acceso a la red). Sin embargo, se recomienda que los desarrolladores de .NET se muevan al tiempo de ejecución de .NET 4,0.

> [!Note]  
> Los ensamblados de DirectX 1,1 administrados heredados no son compatibles con el tiempo de ejecución de .NET 4. x.

 

Consulte [3,4 instalar los recursos de Windows correctamente](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**No se recomienda el uso de un ejecutor u otra tecnología de preinstalación que se base en .NET**
</dt> <dd>

Puede suponer que solo los tiempos de ejecución compatibles con .NET 2,0 (2,0, 3,0, 3,5) están presentes en Windows Vista y Windows 7. De forma predeterminada, solo el entorno de ejecución compatible con .NET 4,0 está presente en Windows 8.

Consulte [compatibilidad con la ejecución automática de 3,7](#37-support-autorun-conditional-requirement).

</dd> <dt>

<span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Hay una comprobador de aplicaciones actualizada para Windows 8**
</dt> <dd>

El SDK de Windows 8 incluye esta comprobador de aplicaciones actualizada.

Consulte [4,2 eliminación de errores de Comprobador de aplicaciones](#42-eliminate-application-verifier-failures).

</dd> </dl>

### <a name="additional-information"></a>Información adicional

<dl>

[Guía de compatibilidad de Windows 8 y Windows Server 2012](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[¿Dónde está el SDK de DirectX?](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a>Juegos para Windows

**Resumen de los requisitos de juegos**

**Ventajas para los clientes**

Los juegos de equipos son una experiencia clave de entretenimiento en Windows, pero los problemas de facilidad de uso han causado la frustración del cliente durante los años. Tradicionalmente, los juegos se instalan como aplicaciones, pero se usan más como medios de entretenimiento (películas o canciones, por ejemplo). Las innovaciones, como el explorador de juegos, exponen juegos de una manera coherente que es diferente de las aplicaciones estándar. Estas innovaciones también proporcionan a los juegos el estado de los ciudadanos de primera clase en Windows, junto con música e imágenes. Los siguientes requisitos ayudan a garantizar que Windows Vista y Windows 7 proporcionan una experiencia de juego mejorada, más accesible y unificada. Al mismo tiempo, garantizan la compatibilidad con Windows XP.

### <a name="11-games-explorer-integration"></a>Integración del explorador de juegos de 1,1

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

El juego debe estar visible en el explorador de juegos (la carpeta **juegos** ) en Windows Vista y Windows 7. Cuando se selecciona, el juego también debe mostrar los metadatos correctos, entre los que se incluyen el publicador, el desarrollador, la fecha de lanzamiento, la versión, las puntuaciones de los índices de experiencia de Windows, la clasificación (si es aplicable) y los hipervínculos asociados.

Si el juego se distribuye digitalmente a través de un servicio de juegos en línea, el proveedor de servicios también debe aparecer en el explorador de juegos. Para garantizar el control correcto del proveedor y para habilitar el uso de fuentes RSS, se debe usar la versión 2 del esquema para los archivos de definición de juego (GDFs). (Para obtener más información sobre GDFs, consulte información adicional).

Además, los instaladores de juegos deben observar las reglas siguientes cuando se ejecutan en Windows Vista y Windows 7:

-   La instalación no debe crear un acceso directo para iniciar el juego en el escritorio, en el menú Inicio o en cualquier otra ubicación.
-   No se deben crear tareas ni accesos directos para quitarlos.
-   Los usuarios deben poder quitar el juego mediante programas y características en el panel de control de Windows Vista y Windows 7, o agregar o quitar programas en el panel de control de Windows XP.

En Windows XP y en versiones anteriores de Windows, el instalador de juegos es gratuito para crear grupos de programas, iconos de escritorio o accesos directos según sea necesario.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

El explorador de juegos de Windows es un concepto similar al de las carpetas de Windows XP **Mis documentos** o **Mis imágenes**. La idea es centralizar contenido similar en un lugar y permitir actividades de organización y contextuales más fáciles. El explorador de juegos amplía el concepto **Mis documentos** o **Mis imágenes** al permitir una organización y un control más completos de los juegos. El explorador de juegos permite a los jugadores ver, organizar e interactuar con todos los juegos instalados en sus sistemas. También permite a los editores de juegos comunicar información de juegos importante de forma más eficaz. El sistema está controlado por datos, lo que facilita que un editor del juego actualice la información del juego durante la vida del producto.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

La integración con el explorador de juegos requiere la creación de un archivo de definición de juego (GDF), que es un archivo de texto XML que se inserta en un archivo binario (un archivo ejecutable o una DLL) como un recurso, junto con un icono de Windows. El juego debe registrarse en el explorador de juegos. El GDF también permite la exposición de la información proporcionada, como el título del juego, el publicador, el desarrollador, los vínculos a los sitios web y las tareas opcionales. Tenga en cuenta que las tareas de soporte solo pueden ser vínculos a sitios web, pero las tareas de reproducción también se pueden usar para tareas de soporte opcionales.

El explorador de juegos puede hacer uso de una imagen de mapa de bits en miniatura, pero se recomienda que, en su lugar, proporcione un recurso de icono de Windows con iconos grandes (256 256). El recurso Icon debe incluir tamaños de imagen de 256 256 48 48, 32 32 y 16 16 en profundidades de color de 24 bits (color verdadero) y 8 bits (256). El editor de iconos proporcionado en Visual Studio 2008 y 2010 admite estos formatos de iconos grandes, como hace IconWorkshop Lite.

En el SDK de DirectX se proporcionan detalles sobre la integración con el **Explorador de juegos de Windows** . El SDK de DirectX incluye un editor de archivos de definición de juego (GDF), así como un GDF de ejemplo que se incluye en GDFExampleBinary, un ejemplo. Otro ejemplo, GameUxInstallHelper, proporciona rutinas para integrar la funcionalidad necesaria en los sistemas de instalación existentes. El validador de archivos de definición de juego (gdftrace.exe) proporciona compatibilidad de depuración para evaluar un GDF. Vea también "integración del explorador de juegos de Windows" en la documentación del SDK de DirectX para C++.

Windows 7 incluye compatibilidad con la segunda versión de un esquema para los archivos GDF. La nueva versión incluye un método simplificado para crear tareas de reproducción y compatibilidad con notificaciones de actualización, proveedores de servicios de juegos, estadísticas de juegos y fuentes RSS para proveedores de servicios de juegos. La versión más reciente de GameUxInstallHelper controla todo el registro y la compatibilidad heredada necesaria para usar un archivo GDF de la versión 2 con Windows Vista. Use las herramientas y el código de ejemplo del SDK de DirectX de agosto 2009 o posterior. Se recomienda usar un archivo GDF de la versión 2 para habilitar la compatibilidad con fuentes RSS, estadísticas de juegos y notificaciones de actualización. Consulte también los ejemplos ProviderGDFExampleBinary y GameStatisticsExample.

En Windows Vista Business Edition, Windows 7 Professional Edition y Enterprise Edition de Windows Vista y Windows 7, el vínculo juegos del menú Inicio está oculto. El explorador de juegos sigue estando disponible en el menú Inicio; para ello, haga clic en **todos los programas** y, a continuación, haga clic en **juegos**.

En el caso de las aplicaciones asociadas que se instalan con el juego, pero no con los juegos, puede crear grupos de programas de menú Inicio, accesos directos e iconos de escritorio en todas las versiones de Windows, incluidas Windows Vista y Windows 7. Tales aplicaciones asociadas deben pasar los juegos aplicables para los requisitos de Windows; para obtener más información, consulte [directrices para productos de middleware de juegos](#guidelines-for-game-middleware-products). Se recomienda que los servicios de juegos se registren en el explorador de juegos como proveedor de juegos para Windows 7. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1,2 compatibilidad con la familia de seguridad y control parental

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Los juegos deben ser totalmente compatibles con la seguridad de la familia de Windows, respetando las siguientes reglas:

-   Los juegos no deben requerir que el usuario tenga credenciales administrativas para jugar. La instalación, la revisión y la eliminación pueden requerir credenciales administrativas, según los requisitos de la sección 3. (Relacionado con esto es el requisito 2,1, siga las directrices de control de cuentas de usuario).
-   Los juegos calificados por las placas de clasificación compatibles con Windows, como ESRB y PEGI, deben incluir la información de clasificación asignada en el archivo de definición de juego (GDF). Todos los datos de clasificación disponibles deben incluirse en cada versión localizada de GDF, así como en la versión independiente del lenguaje.
-   Los juegos deben enumerar sus ejecutables en el GDF para proporcionar una buena experiencia del usuario para las restricciones de aplicaciones generales, a menos que el juego use una tecnología antipiratería que cree archivos ejecutables con nombre aleatorio en tiempo de ejecución.
-   Los juegos deben llamar al método **VerifyAccess** de la interfaz del explorador de juegos durante el inicio, si está disponible, y salir si devuelve \* pfHasAccess como false.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Todos los juegos deben ejecutarse en el contexto de una cuenta de usuario estándar para permitir que las cuentas controladas por el control parental de Windows jueguen al juego. Los padres quieren poder supervisar y controlar el acceso de sus hijos a los juegos. Además, muchos grupos de industria, gubernamentales y de apoyo desean mejores formas de permitir que los padres supervisen y controlen los juegos a los que se exponen sus hijos. Junto con la arquitectura que ofrece el explorador de juegos, Microsoft ofrece a los padres esta capacidad a través de los controles parentales de Windows.

Incluso en el caso de juegos que no participan en un programa de la placa de clasificación, la exigencia de privilegios elevados crea una experiencia de reproducción deficiente para la mayoría de las cuentas de usuario. Esto es especialmente útil si está habilitado el control parental, lo que requeriría que el elemento primario escriba la contraseña de administrador cada vez que se inicie el juego.

El sistema de controles parentales de Windows permite a los padres seleccionar las clasificaciones que piensan que son adecuadas para sus hijos. Los controles parentales admiten muchos de los sistemas de clasificación mundiales. Los controles parentales también permiten que los padres restrinjan el acceso a los juegos basándose en los descriptores de contenido (si el sistema de clasificación aplicable los admite) y para permitir o denegar el acceso a los juegos individuales.

La elección predeterminada del sistema de clasificación para el control parental de Windows se basa en la configuración regional del sistema, pero puede ser modificada por el usuario en la opción **configuración regional y de idioma** del **Panel de control**. Por lo tanto, cada idioma admitido debe proporcionar todos los datos de clasificación disponibles para que el usuario tenga la libertad de seleccionar la placa de clasificación que deseen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Los juegos sin clasificación deben cumplir los requisitos para admitir Play como usuario estándar y llamar a **VerifyAccess**. Estos juegos tienen como valor predeterminado la categoría sin clasificación, muestran el texto "no se proporcionó una clasificación" en el explorador de juegos y están sujetos a la configuración de **restricciones de juego** en el **control parental** para juegos sin clasificación. La configuración de **restricciones** predeterminada es permitir.

La información de clasificación en el GDF se omitirá si el binario que lo contiene no se firmó correctamente con Authenticode. Consulte el requisito 2,3.

El editor de archivos de definición de juego del SDK de DirectX incluye todos los sistemas de clasificación admitidos y replicará correctamente esta información en todas las versiones localizadas de GDF, así como una versión independiente del idioma. La herramienta GDFTrace descodificará y comprobará toda la información de clasificación presente. Use la versión de agosto de 2009 o posterior de estas herramientas.

El GDF de un proveedor de juegos normalmente no contiene información de clasificación y está sujeto a la configuración del contenido sin clasificación.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sistema operativo</th>
<th>Sistemas de clasificación admitidos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><ul>
<li>CERO (Japón)</li>
<li>ESRB (EE. UU.)</li>
<li>OFLC (Australia)</li>
<li>PEGI (Europa)</li>
<li>PEGI Finlandia (desusado)</li>
<li>PEGI Portugal</li>
<li>PEGI/BBFC (Reino Unido)</li>
<li>USK (Alemania)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista con un Service Pack</td>
<td>Los Service Packs para Windows Vista agregan compatibilidad para lo siguiente:<br/>
<ul>
<li>GRB (Corea del Sur)</li>
<li>ESRB &quot; &quot; descriptores de contenido variante leves</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows 7</td>
<td>Windows 7 es compatible con los sistemas de clasificación compatibles con Windows Vista y agrega compatibilidad para lo siguiente: <br/>
<ul>
<li>CSRR (Taiwán)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 8</td>
<td>Windows 8 es compatible con los sistemas de clasificación anteriores y agrega compatibilidad para lo siguiente:<br/>
<ul>
<li>COB-AU (Australia)</li>
<li>DJCTQ (Brasil)</li>
<li>PFB (Sudáfrica)</li>
<li>OFLC-NZ (Nueva Zelanda)</li>
</ul>
Windows 8 retirará la compatibilidad con los siguientes sistemas en desuso:<br/>
<ul>
<li>PEGI-FI (Finlandia)</li>
<li>OFLC (Australia)</li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Cualquier título que incluya nuevos descriptores de contenido de ESRB de Windows Vista Service Pack 1 (SP1) se mostrará como sin clasificación en Windows Vista sin un Service Pack.

 

Los datos de clasificación más recientes se omiten en las versiones de sistemas operativos que no son compatibles con ellos. La variante PEGI (Finlandia) ahora está en desuso en favor del sistema de clasificación PEGI (Europa) estándar. El sistema OFLC está ahora en desuso en favor de COB-AU para Australia.

Para obtener más información sobre cómo crear un juego compatible con los privilegios de usuario estándar, consulte el artículo de DirectX [control de cuentas de usuario para desarrolladores de juegos](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

Consulte el requisito 1,1 para obtener más detalles sobre el archivo de definición de juego (GDF).

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1,3 admitir juegos guardados enriquecidos

\[Este requisito se ha retirado\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 compatibilidad con el requisito condicional de la consola Xbox 360 Common Controller for Windows \[\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Los juegos que admiten controladores de controlador para juegos deben admitir la controladora Xbox 360 para Windows mediante la API de [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) . Si también se admiten periféricos de DirectInput, también se puede usar DirectInput. Sin embargo, XInput debe ser la API predeterminada si se usa un dispositivo compatible con Xbox 360.

Todas las referencias a los botones y desencadenadores de controlador comunes deben usar los nombres de Xbox 360. Para obtener más información, consulte la lista de [terminología de Xbox 360 Common Controller para Windows](#xbox-360-common-controller-for-windows-terminology) .

La vibración del controlador debe estar desactivada cuando el juego está en estado pausado o suspendido.

No se puede deshabilitar completamente el control de mouse/teclado en ningún momento. Como mínimo, debe haber disponible una opción para volver a los menús del juego.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Este requisito permite a los jugadores optar por usar la controladora Xbox 360 o el teclado y el mouse, en función del método de entrada que sea una interfaz más natural e intuitiva.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Este requisito no se aplica a los juegos que solo usan el mouse o el teclado.

Se recomienda implementar la navegación de menú para usar los botones de controlador estándar ampliamente aceptados:

-   A-aceptar
-   B-cancelar
-   Inicio: aceptar o pausar
-   Volver a cancelar, volver a una pantalla o subir un nivel de menú

Para obtener más información, consulte [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal).

En el tema [XInput y DirectInput](/windows/desktop/xinput/xinput-and-directinput) se describen los problemas relacionados con el uso de ambas API al mismo tiempo.

Se recomienda no usar DirectInput para implementar controles de teclado o del mouse. Los controles de teclado y mouse solo deben implementarse mediante mensajes de Windows y las API de Win32. Para más información sobre cómo obtener información de movimiento del mouse de alta resolución sin usar DirectInput, vea [aprovechar High-Definition movimiento del mouse](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement).

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1,5 compatibilidad con varias soluciones y relaciones de aspecto

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

El juego debe admitir al menos las siguientes proporciones de aspecto y las resoluciones de pantalla asociadas:

-   4:3 normal (800 600 o 1024 768)
-   pantalla panorámica 16:9 (1280 720)
-   pantalla panorámica 16:10 (1152 720 o 1680 1050 o 800 480)

En cuanto a la configuración y la detección de la resolución de pantalla, el juego debe cumplir las siguientes reglas:

-   El juego usa la resolución de escritorio del dispositivo de pantalla de forma predeterminada si se trata de una solución compatible. La relación de aspecto del escritorio debe usarse como criterio de búsqueda si el juego elige una resolución predeterminada diferente.
-   El juego debe pedir al usuario que confirme la nueva configuración de pantalla cuando se realice un cambio. Si el usuario no acepta en 15 segundos, la pantalla debe volver a la configuración anterior.
-   El juego no debe ajustar los píxeles ni centrar una ventana de representación 4:3 para admitir las proporciones de aspecto de pantalla panorámica. Sin embargo, la panorámica es aceptable.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Con el escritorio de Windows 3D, no se puede asumir una relación de aspecto o resolución determinada debido a los siguientes factores:

-   Compatibilidad con pantallas de alto detalle.
-   Aumento de la cuota de mercado de monitores de pantalla panorámica.
-   Implementaciones de HDTV para Windows Media Center.
-   Requisitos de accesibilidad.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Idealmente, el juego tiene como valor predeterminado la relación de aspecto nativa de la pantalla. Sin embargo, la obtención confiable de esta información puede ser un reto, por lo que, como una solución más general, el juego puede suponer que el escritorio se está ejecutando con la relación de aspecto nativa. La resolución del escritorio se puede obtener llamando a [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) con la \_ configuración del registro enum \_ .

Para obtener más información, consulte las secciones sobre la relación de aspecto y la pantalla panorámica del artículo de DirectX [Introducción a la experiencia de 10 pies para los desarrolladores de juegos de Windows](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>1,6 Inicio de soporte técnico de Windows Media Center

\[Este requisito se ha retirado.\]

### <a name="17-direct3d-support"></a>Compatibilidad con Direct3D 1,7

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Si el juego usa Direct3D, la versión mínima admitida debe ser Direct3D 9 y Direct3D debe ser el representador predeterminado seleccionado.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

La arquitectura de gráficos principales de Windows Vista y Windows 7 está diseñada en torno a Direct3D. Direct3D 8 y versiones anteriores son compatibles con la reasignación de interfaces heredadas.

Se recomienda encarecidamente el uso de versiones de Direct3D más recientes que Direct3D 9. Vea los juegos para Windows Showcase S. 1. Requerir Direct3D 10 o Direct3D 11 es totalmente compatible con el requisito 1,7.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1,8 habilitar reconocimiento de PPP alto

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Los juegos y sus instaladores deben ejecutarse correctamente sin problemas visuales cuando se habilita el escalado de puntos por pulgada (PPP) (se prueba con 144 ppp para el ajuste de escala del 150% a la resolución de pantalla de 1600 1200) en Windows Vista y Windows 7.

Normalmente, esto requiere que el ejecutable del juego declare sea compatible con el PPP. Esto se logra mediante la inserción de un elemento de manifiesto: <dpiAware> true <dpiAware> .

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Los monitores LCD de alta calidad son habituales cuando se muestran los equipos y tienen el mejor aspecto cuando se controla con sus soluciones nativas (normalmente 1280 1024, 1600 1200, etc.). Los clientes que tienen dificultades para leer texto y ver imágenes en esta resolución a menudo establecen sus escritorios de equipo en una resolución más baja y sufren artefactos visuales a partir del escalado de LCD. En su lugar, los clientes pueden dejar la resolución en el tamaño nativo y cambiar el PPP de la pantalla de Windows, por lo que la apariencia de los elementos y del texto es mayor sin sacrificar la calidad de la imagen.

Aunque esta característica está disponible en algún formato desde Windows XP, rara vez la habilitan los clientes o los OEM. En la actualidad, más de la mitad de todos los equipos se establecen en una resolución más baja que la resolución nativa del monitor, en función de los comentarios de los clientes. Windows 7 hace que esta característica sea mucho más visible para los clientes durante la instalación inicial y al cambiar la configuración de pantalla, lo que anima a usar el escalado de PPP en lugar de cambiar la resolución del escritorio.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

En su lugar, se puede usar la función [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) , si se llama al principio del código de inicio del proceso. Se prefiere agregar al manifiesto para asegurarse de que no hay condiciones de carrera con elementos de software (como archivos dll) que puedan inicializarse antes de que se llame al punto de entrada principal. Tenga en cuenta que **SetProcessDPIAware** solo está presente en Windows Vista y Windows 7.

Agregar el elemento de manifiesto es fácil de hacer con Visual Studio 2005 y 2008; Cree un archivo denominado dpiaware. manifest que contenga el texto siguiente:

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

Después, en Visual Studio, agregue dpiware. manifest al proyecto. Asegúrese de que **incrustar manifiesto** está establecido en **sí** en las propiedades del proyecto. Tenga en cuenta que las versiones anteriores de la herramienta manifiesto (Mt.exe) generarán una advertencia falsa con los elementos de manifiesto con reconocimiento de PPP. Para resolverlo, actualice Mt.exe a la versión más reciente del Windows SDK.

Visual Studio 2010 incluye una configuración en las propiedades del proyecto, denominada **Habilitar reconocimiento de PPP**, que elimina la necesidad de un archivo como dpiaware. manifest. Busque **Habilitar reconocimiento de PPP** expandiendo **propiedades de configuración** y **herramienta de manifiesto** y, a continuación, seleccione **entrada & salida**.

En Windows, el modo de presentación tradicional tiene como valor predeterminado 96 PPP, que era común para los monitores de CRT.

Mientras que las aplicaciones de pantalla completa cambian la resolución de pantalla, suelen usar mensajes y métricas de ventana al configurar los búferes y mostrar los rectángulos. La virtualización de PPP hace que estos modos de presentación de pantalla completa aparezcan recortados y declarar el reconocimiento de PPP impedirá estos problemas. Para obtener más información, vea [Writing DPI-Aware Win32 Applications](../hidpi/high-dpi-desktop-application-development-on-windows.md).

</dd> </dl>

## <a name="security-and-compatibility"></a>Seguridad y compatibilidad

**Resumen de los requisitos de seguridad y compatibilidad**

**Ventajas para los clientes**

Los siguientes requisitos mejoran la seguridad general de los juegos y ayudan a asegurarse de que funcionan con Windows en arquitecturas diferentes, con diferentes configuraciones y en distintos modos.

### <a name="21-follow-user-account-control-guidelines"></a>2,1 Siga las directrices de control de cuentas de usuario

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Cada archivo ejecutable (es decir, cada archivo que tiene una extensión. exe) debe contener un manifiesto incrustado que defina su nivel de ejecución mediante la inclusión de la siguiente etiqueta:

``` syntax
            <requestedExecutionLevel>
```

Por requisito 1,2, el juego principal y el ejecutable de ejecución automática deben tener el nivel de ejecución de AsInvoker para admitir contextos de usuario estándar.

Los archivos de datos de usuario que tienen asociaciones de archivos registradas con el **Explorador de archivos** deben colocarse en una subcarpeta de la carpeta especificada por CSIDL \_ personal (también denominada **documentos** o **Mis documentos**). Todos los demás archivos de datos de usuario deben almacenarse en una subcarpeta de las carpetas especificadas por CSIDL \_ local \_ AppData o la \_ AppData común de CSIDL \_ . (Estos directorios están ocultos de forma predeterminada para usuarios individuales y para todos los usuarios).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

La experiencia de Windows de un usuario es más segura si las aplicaciones solo se ejecutan con los permisos necesarios.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Si solo algunas características de una aplicación requieren privilegios administrativos (por ejemplo, una aplicación que necesite configurar un firewall), el proceso principal de la aplicación se debe seguir ejecutando con privilegios de usuario estándar. Las características que requieren privilegios administrativos deben moverse a un proceso independiente, como un instalador o una utilidad de configuración.

Si no se necesitan privilegios administrativos, el XML de manifiesto incrustado debe incluir lo siguiente:

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

Si se requieren privilegios administrativos, el XML de manifiesto incrustado debe incluir lo siguiente:

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

Con Visual Studio 2005, esto se incrusta fácilmente agregando un archivo de manifiesto (. manifest) que contiene uno de los bloques anteriores al proyecto y asegurándose de que **incrustar manifiesto** está establecido en **sí** en las propiedades del proyecto para la herramienta manifiesto. En Visual Studio 2008 y 2010, las propiedades de UAC se pueden establecer directamente en las propiedades del proyecto para el vinculador en la página del **archivo de manifiesto** . Tenga en cuenta que las versiones anteriores de la herramienta manifiesto (Mt.exe) generan una advertencia falsa con los elementos de manifiesto de UAC. Para resolverlo, actualice Mt.exe a la versión más reciente del Windows SDK.

Consulte el requisito 3,1 para más información sobre los casos especiales de instalación, revisión y eliminación.

Las bibliotecas de vínculos dinámicos (dll) no requieren dichos manifiestos.

Para obtener más información acerca del control de cuentas de usuario, consulte [control de cuentas de usuario para desarrolladores de juegos](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>2,2 compatibilidad con versiones x64 de Windows

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Para mantener la compatibilidad con las ediciones de 64 bits de Windows, los juegos deben cumplir los siguientes requisitos.

-   Los instaladores de títulos y títulos no deben contener código de 16 bits ni confiar en ningún componente de 16 bits.
-   Si el juego depende de los controladores en modo kernel para su funcionamiento, las versiones x64 de estos controladores deben estar disponibles. La configuración del juego debe detectar e instalar los controladores y componentes adecuados para las ediciones de 64 bits de Windows.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Muchos usuarios de Windows Vista y Windows 7 ejecutarán las ediciones de 64 bits del sistema operativo a lo largo de la vida del producto, por lo que es fundamental que las aplicaciones sean compatibles con este sistema operativo.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Windows en Windows 64 (WOW64) permite que el código de 32 bits se ejecute en ediciones de 64 bits de Windows, por lo que no es necesario que la aplicación sea un código de 64 bits nativo en ediciones de 64 bits de Windows. El código de dieciséis bits no se ejecuta en las ediciones de 64 bits de Windows.

No es necesario mantener la compatibilidad con Windows XP Professional x64 Edition, pero se recomienda encarecidamente hacerlo.

Para obtener más información, consulte [programación de 64 bits para desarrolladores de juegos](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> </dl>

### <a name="23-sign-files"></a>Archivos de firma de 2,3

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Todos los archivos de código ejecutable (normalmente archivos con la extensión. exe o. dll) deben estar firmados con un certificado Authenticode válido públicamente y deben tener una dirección URL válida del servidor de marca de tiempo para la firma de producción.

Si el juego usa Windows Installer, los archivos de paquete del instalador (archivos. msi) deben estar firmados.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Firmar un archivo ayuda a los usuarios a decidir si confiar en una aplicación y garantiza que los usuarios no hayan sido alterados. También permite que las aplicaciones se ejecuten correctamente en entornos bloqueados.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para obtener más información, consulte [firma Authenticode para desarrolladores de juegos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

Si el juego usa Windows Installer, se recomienda que habilite la revisión de UAC/LUA incluyendo una tabla MsiPatchCertificate. Para obtener más información, consulte [Patching control de cuentas de usuario (UAC)](/windows/desktop/Msi/user-account-control--uac--patching).

No se recomienda firmar archivos CAB (. cab), a menos que sean relativamente pequeños (menos de 100 MB).

</dd> </dl>

### <a name="24-sign-drivers"></a>Controladores de firma de 2,4

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Cualquier controlador en modo kernel instalado por el juego debe estar firmado con un certificado Authenticode válido públicamente.

Cualquier controlador de dispositivo de hardware en modo de kernel instalado por el juego debe tener una firma de Microsoft, que se puede obtener de los laboratorios de calidad de hardware de Windows (WHQL) o del programa de firma de confiabilidad de controlador (DRS).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Los controladores mal escritos o de malware pueden afectar gravemente a la estabilidad y la seguridad de un sistema. En las ediciones de 64 bits de Windows Vista y Windows 7, no se cargan los controladores sin firmar. Esta Directiva también se puede habilitar para las ediciones de 32 bits de Windows Vista y Windows 7.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Las versiones nativas de 32 bits y de 64 bits de todos los controladores en modo kernel son necesarias por el requisito 2,2.

Puede encontrar más información sobre los programas de firma de controladores de Microsoft en el [portal para desarrolladores de hardware de Windows](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx).

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2,5 realizar la comprobación de la versión correcta

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Los juegos no deben ejecutarse en sistemas operativos futuros, tal como se indica en los cambios en el número de versión de Windows, a menos que el contrato de licencia para el usuario final prohíba su uso en sistemas operativos futuros. Si se supone que el juego genera un error, debe hacerlo correctamente mostrando un mensaje adecuado al usuario.

Si se realizan comprobaciones de la versión de Windows, se deben usar las API de comprobación de versiones ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) o [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) para comprobar la versión del sistema operativo. No se deben leer las claves del registro para determinar la versión.

Las comprobaciones de versión explícitas para el tiempo de ejecución de DirectX no deben estar presentes en el juego. Estas comprobaciones de versión no deben estar presentes en la instalación que inicia el programa de instalación de DirectX en tiempo de ejecución (DirectSetup).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Cuando los usuarios de Windows actualizan sus sistemas operativos, no se les debe bloquear la reproducción de juegos actuales simplemente porque ha aumentado el número de versión de Windows. Los comprobadores de versión mal escritos continúan creando problemas de software que, de lo contrario, funciona correctamente en las versiones más recientes de Windows o simplemente con la adición de un Service Pack de Windows.

La lógica de comparación de comprobación de versión frágil para el tiempo de ejecución de DirectX ha creado numerosas instalaciones erróneas cuando se ejecuta en versiones diferentes de Windows. El número de versión de DirectX solo se aplica a los componentes principales del sistema operativo. No se aplica a los componentes de DirectX SDK en paralelo que utilizan muchos juegos.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Es bastante común ver que los instaladores comprueban una versión mínima del sistema operativo. Sin embargo, esta comprobación debe realizarse con cuidado para asegurarse de que se prueba para que sea mayor o igual que, en lugar de una igualdad simple, con lo que se bloquea en una versión específica del sistema operativo. El uso de la prueba **HighVersionLie** de Comprobador de aplicaciones es una manera rápida y sencilla de determinar cómo reaccionará el instalador ante un cambio significativo en el número de versión del sistema operativo.

El uso correcto del paquete de redistribución de tiempo de ejecución de DirectX (instalación de DirectX) implica iniciarlo siempre durante la instalación, preferiblemente en modo silencioso. Esto permite que el código proporcionado por Microsoft realice las actualizaciones de versión necesarias. También permite instalar cualquier componente opcional de DirectX SDK en paralelo, como D3DX, XACT, MDX o XInput.

Para conocer los procedimientos recomendados para implementar el entorno de tiempo de ejecución de DirectX, consulte [instalación de DirectX para desarrolladores de juegos](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

Se recomienda que los juegos que admiten Windows XP busquen un nivel de Service Pack de 2 o superior, ya que Service Pack 2 (SP2) y Service Pack 3 (SP3) proporcionan importantes mejoras de seguridad, un requisito simplificado de redistribución en tiempo de ejecución de DirectX y una implementación muy amplia. La mayoría de las tecnologías modernas de Microsoft que admiten Windows XP requieren SP2 o SP3 (XAudio2, games for Windows-LIVE, etc.).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2,6 compatibilidad con sesiones de usuario simultáneas

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

No es necesario que los juegos basados en gráficos 3D funcionen a través de una conexión a escritorio remoto, pero el usuario debe recibir una alerta cuando se produzca un error en el juego.

Los juegos deben admitir escenarios estándar de multitarea de Windows, respetando las siguientes reglas:

-   Los juegos no deben bloquear el uso de sesiones de usuario simultáneas.
-   Un juego debe ejecutarse en una nueva sesión de usuario cuando ya se esté ejecutando en otra sesión.
-   El sonido de un juego en una sesión de usuario no debe escucharse cuando otro usuario está activo en otra sesión.
-   Los juegos deben admitir el cambio rápido de usuario.
-   Los juegos no deben intentar deshabilitar la conmutación de tareas estándar. Los juegos no deben deshabilitar el método abreviado de teclado ALT + TAB. Los juegos pueden deshabilitar los métodos abreviados de teclado de accesibilidad, como se describe en [deshabilitar teclas de método abreviado en juegos](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Los usuarios de Windows deben ser capaces de ejecutar sesiones simultáneas sin conflictos ni interrupciones. Se trata de un escenario común para un equipo Windows compartido por una familia, ROOMMATES u otros.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para probar si el juego se inicia en una sesión remota, llame a [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ REMOTESESSION). Un valor distinto de cero indica que la sesión es remota.

Para obtener más información, consulte [cambio rápido de usuario](/windows-hardware/drivers/display/fast-user-switching). Tenga en cuenta que el cambio rápido de usuario se produce si se habilitan las restricciones de tiempo de control parental cuando el tiempo del usuario está activo. Consulte el requisito 1,2 para obtener más detalles.

</dd> </dl>

### <a name="27-support-long-names"></a>2,7 compatibilidad con nombres largos

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Si un juego admite el guardado de archivos, debe poder guardar archivos que tengan nombres y rutas de acceso largos. El juego debe administrar correctamente caracteres especiales del sistema de archivos, como \\ /: \* ? " < >, en los campos de entrada de usuario que se usan para crear nombres de archivo o rutas de acceso.

Los juegos deben funcionar correctamente cuando un usuario tiene un nombre de usuario largo.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Los reproductores están acostumbrados a usar nombres largos en rutas de acceso profundas que son compatibles con el sistema operativo subyacente.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Los nombres largos se definen como los que contienen los valores máximos que se definen en el Windows SDK.

</dd> </dl>

## <a name="installation"></a>Instalación

**Resumen de los requisitos de seguridad y compatibilidad**

**Ventajas para los clientes**

Los clientes pueden estar seguros de que las aplicaciones se instalarán en Windows sin degradar el sistema operativo ni otras aplicaciones si las aplicaciones usan métodos de distribución de componentes del sistema oficiales. Una experiencia de instalación simplificada proporciona una experiencia de juegos más accesible y sin problemas.

### <a name="31-support-easy-installation"></a>3,1 compatibilidad con la instalación sencilla

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Los juegos deben proporcionar una ruta de acceso simplificada en la interfaz de usuario del programa de instalación mediante la implementación de lo siguiente:

-   Mostrar un mensaje de CLUF como máximo.
-   La ruta de instalación predeterminada debe omitir todas las selecciones de la instalación (por ejemplo, la carpeta de instalación o las selecciones de componentes), suponer las selecciones predeterminadas y, a continuación, ejecutar el juego o el iniciador tras una instalación correcta, sin preguntar más. Si lo desea, puede proporcionar una opción de instalación personalizada para opciones de configuración avanzadas.
-   Instale los componentes necesarios del sistema operativo (como los tiempos de ejecución de DirectX y Visual C) mediante los paquetes de redistribución de Microsoft correctos. La instalación se debe realizar de forma silenciosa, sin preguntar y sin que se protejan las comprobaciones de la versión del componente.
-   Proporcione la eliminación a través de **programas y características** en el **Panel de control** para la aplicación de juego y los archivos de trabajo generados. Se recomienda una opción para eliminar los archivos de datos creados por el usuario. El proceso de eliminación debe asegurarse de que se quitan todos los archivos instalados y se borran todas las configuraciones (por ejemplo, las entradas de la lista de excepciones de firewall y las claves del registro). Los componentes del sistema operativo redistribuidos no se deben quitar.
-   Si el juego requiere que se agreguen excepciones al firewall de Windows, el proceso de instalación puede solicitar informar a los usuarios de que este cambio es obligatorio. Este aviso debe aparecer antes de que se inicie la instalación.

La instalación y la eliminación pueden requerir derechos administrativos. La revisión puede requerir solicitar credenciales administrativas, en función de la frecuencia de actualización. La reproducción normal del juego no debe requerir derechos administrativos; por el requisito 2,1 Siga las directrices de control de cuentas de usuario.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

La instalación sencilla es una filosofía de desarrollo de juegos centrada en Windows que está diseñada para simplificar y simplificar el proceso a veces tedioso y confuso de instalar juegos en equipos que ejecutan sistemas operativos Windows. La instalación sencilla se habilita mediante el uso de un conjunto de tecnologías y prácticas recomendadas que reducen la complejidad innecesaria y el riesgo percibido de instalar juegos en equipos Windows.

Los principales objetivos son:

-   Reduzca la cantidad de tiempo que debe entrar en el juego y comenzar a jugar.
-   Reduzca el número de cuadros de diálogo y opciones a muy pocos o ninguno, con el fin de simplificar la experiencia de instalación del juego.

Algunas instalaciones tradicionales tienen avisos que permiten instalaciones no funcionales, aunque la aplicación parezca que se ha instalado correctamente. Por ejemplo, un juego puede requerir que un usuario acepte un CLUF. Después, se instala el juego y, a continuación, aparece el CLUF de DirectX. Este CLUF permite a los usuarios rechazar y, por tanto, omitir la instalación del tiempo de ejecución de DirectX. Este escenario puede provocar que un juego no se ejecute debido a que faltan componentes.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para obtener más información sobre la instalación de juegos, las técnicas de instalación de juegos no tradicionales, las soluciones de revisión compatibles con UAC y el control de revisiones frecuentes, consulte los siguientes artículos de DirectX:

-   [Simplificar la instalación de juegos](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [Instalación a petición de juegos](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [Aplicar revisiones al software de juegos en Windows XP, Windows Vista y Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Prácticas recomendadas de instalación para juegos en línea multijugador masivo](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> La eliminación de archivos de datos generados específicos del usuario solo se debe realizar para el usuario actual y para ubicaciones de usuario compartidas comunes. No hay ninguna manera robusta de examinar el sistema para quitar archivos específicos del usuario para otros usuarios, incluso si la eliminación requiere credenciales administrativas.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3,2 compatibilidad con el control de cuentas de usuario para la instalación

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

El instalador del juego no debe asumir que se está ejecutando en el mismo contexto que el usuario. Las ubicaciones específicas del usuario serán diferentes del instalador y del reproductor, incluso para sistemas de usuario único debido a la elevación de credenciales de administrador. Por lo tanto, cuando un juego se ejecuta por primera vez, debe realizar tareas específicas del usuario, independientemente del proceso de instalación.

El cuadro de diálogo excepción de Firewall de Windows no debe aparecer cuando un usuario hospede o se una a un juego multijugador. Cualquier configuración necesaria debe realizarse en el momento de la instalación. Las instrucciones de configuración deben informar al usuario de que esta operación se realizará como parte de la configuración.

El instalador de juegos debe proporcionar un manifiesto incrustado que designe el nivel de ejecución necesario, por requisito 2,1 Siga las directrices de control de cuentas de usuario.

Si el instalador inicia el juego una vez completada la instalación, debe iniciarse en el contexto del usuario original.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Uno de los cambios más importantes en el sistema operativo Windows en Windows Vista es la adición de control de cuentas de usuario (UAC), que ejecuta las aplicaciones con privilegios reducidos de forma predeterminada. Como resultado, los instaladores necesitan administrar los niveles de privilegios en consecuencia. Windows 7 también hace un uso extensivo de UAC. Aunque Windows 7 mejora la experiencia del usuario de UAC, los instaladores deben cumplir los mismos requisitos que en Windows Vista para funcionar correctamente, sin depender del comportamiento de virtualización potencialmente confuso.

UAC está activo de forma predeterminada en Windows Vista y Windows 7, y la inmensa mayoría de los clientes (del 88% o más, en función de los comentarios) dejan esta característica habilitada.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para obtener más información sobre la configuración del firewall de Windows, consulte el artículo de DirectX [firewall de Windows para desarrolladores de juegos](/windows/desktop/DxTechArts/games-and-firewalls) y el ejemplo FirewallInstallHelper.

El lanzamiento estándar del juego al final del proceso de instalación no cumple el último aspecto de este requisito si un usuario estándar inicia la instalación, y si el proceso de instalación requiere privilegios administrativos (es decir, solicita una credencial de administrador). También hereda los privilegios administrativos, lo que es un riesgo de seguridad potencial. En su lugar, un cargador de arranque de instalación debe iniciar el juego después de volver de una invocación correcta del instalador. Para obtener más información, vea el artículo de MSDN Magazine [para que las aplicaciones se reproduzcan perfectamente con el control de cuentas de usuario de Windows Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3,3 instalar en carpetas correctas

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

De forma predeterminada, los juegos que se instalan para todos los usuarios se deben instalar en la carpeta archivos de programa. Los datos de usuario se deben escribir cuando el juego se ejecuta por primera vez, no durante la instalación.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Los usuarios deben disponer de la flexibilidad necesaria para instalar aplicaciones donde las necesiten. También deben tener una experiencia coherente y segura con la ubicación predeterminada de los archivos.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Los juegos pueden hacer uso de las distintas ubicaciones de carpetas conocidas (como las especificadas por CSIDL \_ local \_ AppData y CSIDL \_ Common \_ AppData) para almacenar grandes cantidades de datos de juegos y archivos ejecutables para implementar escenarios avanzados de instalación a petición y de aplicación de revisiones.

Dado que la instalación puede requerir la elevación a una cuenta de usuario diferente durante el proceso de instalación de todos los usuarios, no hay una ubicación de usuario correcta en la que almacenar los datos en el momento de la instalación. Además, si está habilitado el cifrado de archivos, solo se puede tener acceso a los archivos cifrados mediante la cuenta de usuario que los creó.

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3,4 instalar los recursos de Windows correctamente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Las aplicaciones no deben intentar instalar archivos o claves del registro protegidas por Protección de recursos de Windows (WRP). Si la aplicación requiere versiones más recientes de los componentes del sistema, debe actualizar estos componentes mediante un Service Pack de Microsoft o un paquete de instalación aprobado por Microsoft que contenga el componente del sistema. Los componentes del sistema nunca se deben volver a empaquetar.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Protección de recursos de Windows (WRP) está diseñado para garantizar que los recursos del sistema protegido solo se actualizan mediante los mecanismos de instalación o actualización aprobados por Microsoft. WRP mejora la confiabilidad del sistema, ya que garantiza que los resultados de una instalación son predecibles.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

WRP es el sucesor de protección de archivos de Windows, que protege la mayoría de los componentes del sistema que se instalan en la carpeta Windows. WRP protege la mayoría de las claves del registro que almacenan la configuración para la creación de objetos COM. También reserva determinadas carpetas para su uso exclusivo por parte del sistema operativo. Los intentos de acceso a recursos protegidos normalmente producen un error de denegación de acceso.

Para más información sobre los procedimientos recomendados para implementar el entorno de tiempo de ejecución de DirectX con un juego, consulte el artículo de DirectX [instalación de DirectX para desarrolladores de juegos](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3,5 evitar reinicios durante la instalación

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

El instalador de juegos no debe suponer que la instalación de los componentes de Windows de los paquetes de redistribución requiere un reinicio, a menos que el reinicio se indique mediante un resultado devuelto o la documentación de Microsoft.

Si el instalador de juegos siempre fuerza un reinicio, debe aprobarlo Microsoft.

Los cuadros de diálogo de archivos en uso que se incluyen en los paquetes de Windows Installer deben contener una opción para cerrar las aplicaciones automáticamente e intentar reiniciarlas una vez completada la instalación.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Reiniciar el sistema después de una instalación es una interrupción inadecuada para los usuarios y normalmente no es necesario.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para obtener más información, consulte [uso de Windows Installer con el administrador de reinicio](/windows/desktop/Msi/using-windows-installer-with-restart-manager).

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3,6 usar el control de versiones de archivos correctamente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

El programa de instalación del juego debe comprobar correctamente para asegurarse de que las versiones más recientes del archivo estén instaladas. La instalación de un juego nunca debe retrasar los archivos que no genere o que compartan las aplicaciones que no genere.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Los componentes compartidos y los componentes del sistema suelen actualizarse para las correcciones de seguridad y la funcionalidad ampliada. Una instalación que incluya una versión anterior de los componentes actualizados no debe producir la pérdida de actualizaciones y correcciones que ya se hayan aplicado.

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3,7 compatibilidad con el requisito condicional de ejecución automática \[\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

En el caso de los juegos distribuidos en CD, DVD u otros medios extraíbles que admitan la ejecución automática, cuando se inserte el disco por primera vez, la aplicación debe ejecutarse automáticamente o preguntar al usuario si desea instalar el juego, a menos que el usuario haya deshabilitado la característica de ejecución automática.

Una vez que la aplicación se haya instalado correctamente, volver a insertar el disco en la unidad no debe hacer que la instalación se inicie automáticamente de nuevo. Es aceptable preguntar a los usuarios si desean actualizar o cambiar las opciones de instalación.

La aplicación Autorun no debe solicitar la elevación (es decir, debe tener un llamador en el manifiesto, por requisito 2,1, aunque puede iniciar el programa de instalación u otra utilidad que requiera derechos administrativos). La elevación solo debe producirse si el juego no está instalado o si el usuario lo selecciona específicamente.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

La ejecución automática simplifica la experiencia de uso de aplicaciones distribuidas por medios, como los juegos que normalmente requieren que el disco esté presente en la unidad para poder reproducir el juego.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

No es aceptable requerir que el usuario navegue por el explorador de archivos para iniciar la instalación desde el CD o DVD.

En el caso de los juegos que se distribuyen en varios discos, idealmente deben usar la característica de ejecución automática o continuar la instalación sin preguntar al usuario si desea presionar una tecla o realizar otra acción.

Al crear un programa de ejecución automática, asegúrese de que todos los componentes necesarios están presentes en las instalaciones nuevas de Windows. Las aplicaciones típicas se basan en tecnologías instaladas por el programa de instalación, pero la ejecución automática se ejecuta antes de que se produzca este tipo de configuración. Un ejemplo común es el error de los programas de ejecución automática porque las dll de tiempo de ejecución de Visual C no se incluyeron como parte del programa de instalación de Windows. Por lo tanto, el programa autorun debe usar la implementación de CRT local de la aplicación o debe vincular estáticamente CRT.

Los programas de ejecución automática escritos para su uso en versiones de Windows anteriores a Windows Vista no deben usar el tiempo de ejecución de .NET porque esta tecnología no se incluye con Windows XP o versiones anteriores de Windows. Windows Server 2003 y Windows Vista son las primeras versiones de Windows que incluyen el tiempo de ejecución de .NET como parte de su sistema operativo.

Por motivos similares, los programas de ejecución automática no pueden requerir la presencia de componentes en paralelo opcionales del SDK de DirectX, como D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, XACT, XINPUT y MDX 1,1.

Para obtener un ejemplo de uso de la ejecución automática, vea ejemplo de ejecución automática.

</dd> </dl>

## <a name="reliability"></a>Confiabilidad

**Resumen de los requisitos de seguridad y compatibilidad**

**Ventajas para los clientes**

Estos requisitos hacen que una aplicación sea más confiable al minimizar el número de bloqueos, bloqueos y reinicios. Los requisitos de confiabilidad pueden ayudar a garantizar que el software sea más predecible, mantenible, resistente y recuperable.

### <a name="41-eliminate-unnecessary-reboots"></a>4,1 eliminación de los reinicios innecesarios

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Todos los instaladores de aplicaciones deben aprovechar las API del administrador de reinicio para evitar reinicios del sistema (consulte el requisito 3,5).

Los juegos no deben bloquear el cierre.

Todas las aplicaciones deben responder al administrador de reinicios escuchando y respondiendo a los siguientes mensajes de apagado:

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ QUERYENDSESSION con lParam = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Las aplicaciones GUI deben responder (TRUE) inmediatamente como preparación para un reinicio.

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ ENDSESSION con lParam = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Las aplicaciones deben devolver un valor 0 en 5 segundos y, a continuación, cerrar.

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL + C 
</dt> <dd>

Las aplicaciones de consola que reciben este mensaje deben cerrarse inmediatamente.

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Los reinicios del sistema son una interrupción importante. Conducen a una experiencia de usuario incorrecta y deben minimizarse. Algunas operaciones, como las actualizaciones críticas del sistema, pueden requerir reinicios. Al escuchar mensajes de cierre, el juego y otras aplicaciones pueden responder rápidamente a las solicitudes del administrador de reinicio. De esta manera, pueden evitar retrasos innecesarios en solicitudes de reinicio válidas.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Si un instalador de juegos usa la tecnología de Windows Installer (MSI) sin ninguna acción personalizada, esta funcionalidad se proporciona automáticamente. Los paquetes de redistribución de Microsoft también admiten el administrador de reinicio.

Para obtener más información acerca del administrador de reinicio, consulte el artículo de MSDN [acerca del administrador de reinicio](/windows/desktop/RstMgr/about-restart-manager).

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4,2 eliminación de errores de comprobador de aplicaciones

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

El juego no debe generar ningún error que se ejecute en Microsoft comprobador de aplicaciones (AppVerifier), versión 4,0 o posterior, en las siguientes pruebas:

-   Aspectos básicos: identificadores, montones, bloqueos, memoria, TLS
-   Varios: DangerousAPIs, DirtyStacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

AppVerifier comprueba muchos problemas conocidos que causan bloqueos y bloqueos en aplicaciones Windows, así como vulnerabilidades de seguridad conocidas.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para obtener más información acerca de comprobador de aplicaciones, vea [Comprobador de aplicaciones](/previous-versions/ms220948(v=vs.80)) y [uso de Comprobador de aplicaciones dentro del ciclo de vida de desarrollo de software](/previous-versions/aa480483(v=msdn.10)) en MSDN. Puede descargar comprobador de aplicaciones de detalles de la [descarga: Comprobador de aplicaciones](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) en el centro de descarga de Microsoft.

Este requisito no se aplica a las aplicaciones administradas puras sin interoperabilidad nativa.

Estas pruebas se deben ejecutar en una compilación de versión. Las compilaciones de depuración pueden generar errores falsos. Algunas tecnologías antipiratería y antitrampa pueden interferir con la ejecución de AppVerifier. Por lo tanto, estas pruebas deben realizarse sin tecnologías antipiratería y antitrampas habilitadas.

Puede que sea necesario establecer la propiedad completa de los aspectos básicos: la prueba de montones en FALSE, ya que el PageHeap completo aumenta en gran medida la presión de memoria de la aplicación en ejecución. Los errores se seguirán detectando, pero es posible que resulte más difícil realizar un seguimiento de ellos si solo usa PageHeap parcial.

Si usa las pruebas relacionadas con UAC/LUA en comprobador de aplicaciones para cumplir los requisitos de control de cuentas de usuario 2,1 y 3,2, debe usar el [analizador de usuario estándar](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) para revisar los resultados. También hay muchas otras pruebas útiles que proporciona comprobador de aplicaciones que se recomienda usar en el desarrollo y las pruebas para garantizar un alto nivel de compatibilidad con las versiones actuales y futuras de Windows. La prueba **HighVersionLie** se usa para comprobar el cumplimiento del requisito 2,5.

Visual Studio Team System incluye un subconjunto de la funcionalidad de AppVerifier que se integra en el entorno de depuración. Esto puede resultar útil para el seguimiento y la resolución de problemas con aspectos básicos: montones, identificadores y pruebas de bloqueos.

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4,3 compatibilidad con Informe de errores de Windows e información de versión de archivo

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Para habilitar la compatibilidad de Informe de errores de Windows, los juegos deben cumplir los siguientes requisitos:

-   Los juegos deben controlar solo las excepciones que se conocen y se esperan. Informe de errores de Windows no debe estar deshabilitado. Si aparece un error como una infracción de acceso en un juego, debe permitir que Informe de errores de Windows informe del bloqueo.
-   Todos los archivos ejecutables (por ejemplo, archivos. exe o dll) deben contener un nombre de producto exacto, el nombre de la compañía y la versión del archivo.
-   La salida normal del juego no debe producir un error de excepción desconocido.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Las API de Informe de errores de Windows proporcionan comentarios vitales a Microsoft para detectar bloqueos generalizados y bloqueos en las aplicaciones. Esto permite a Microsoft y sus asociados detectar y resolver rápidamente problemas del sistema y del controlador que conducen a errores de la aplicación rápidamente.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Los juegos pueden incluir controladores de excepciones no controladas personalizados para realizar la funcionalidad de informes y soporte técnico personalizados, pero deben pasar cualquier error en las funciones **ReportFault** o **WerReportSubmit** .

Se puede comprobar la información de la versión de archivo adecuada viendo las propiedades del archivo en la interfaz de usuario del escritorio de Windows y comprobando la página de propiedades versión.

Para obtener más información acerca de las API de Informe de errores de Windows y cómo analizar los volcados de memoria que se generan al usar este servicio, consulte el artículo de DirectX [análisis de volcado](/windows/desktop/DxTechArts/crash-dump-analysis)de memoria.

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>Terminología del controlador común de Xbox 360 para Windows



|                                          |                                                                                                  |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| A                                        | Botón A                                                                                     |
| B                                        | El botón B                                                                                     |
| ATRÁS                                     | Botón atrás                                                                                  |
| reboteadores (derecha/izquierda)                      | Botón situado en la parte superior derecha y borde izquierdo del controlador. Equivalente a un botón de hombro.    |
| Panel direccional                          | Panel direccional del controlador                                                                   |
| PAD D                                    | Abreviatura aceptada de pad direccional                                                         |
| DP                                       | Abreviatura del controlador direccional y etiqueta del controlador                                                |
| RB, LB                                   | Abreviaturas de los reboteadores derecho y izquierdo y etiquetas del controlador                                        |
| RS, LS                                   | Abreviaturas izquierda y derecha y etiquetas del controlador                                         |
| RT, LT                                   | Abreviaturas de desencadenadores y etiquetas de controlador de derecha e izquierda                                       |
| RSB, LSB                                 | Abreviaturas izquierda y derecha y etiquetas del controlador                                         |
| START                                    | El botón Iniciar                                                                                 |
| Stick (derecha/izquierda)                       | El stick de controlador. Anteriormente, el stick analógico.                                                       |
| botón de adhesivo (derecha/izquierda)                | Botón de la palanca del controlador. Botón de stick analógico anteriormente.                                         |
| (derecha/izquierda) desencadenador                     | Desencadenador del controlador.                                                                          |
| Vibración                                | Comentarios del juego generados por el motor del controlador. No use Rumble.                           |
| X                                        | El botón X                                                                                     |
| Y                                        | El botón Y                                                                                     |
| Controladora Xbox 360 para Windows          | El controlador de juegos de Xbox 360 vendió como un SKU de hardware de equipo, incluido un disco de controlador de dispositivo de Windows.          |
| Controlador inalámbrico Xbox 360 para Windows | El controlador de juegos inalámbrico Xbox 360 vendió como un SKU de hardware de equipo, incluido un disco de controlador de dispositivo de Windows. |



 

## <a name="guidelines-for-game-middleware-products"></a>Directrices para productos de middleware de juegos

### <a name="introduction"></a>Introducción

Para que los juegos puedan optar al programa games for Windows, deben cumplir una lista de requisitos técnicos. Los componentes de terceros que se incluyen con un título (archivos ejecutables, dll, controladores, etc.) también deben cumplir estos requisitos para que el juego pueda calificarse. En este documento se resaltan los requisitos más comunes que también deben cumplir los componentes de terceros del juego para pasar las pruebas de cumplimiento. Los instaladores y los paquetes de producción y del motor de juego completos deben revisar el documento de requisitos técnicos de juegos completos para Windows, ya que muchos de estos requisitos se ven afectados por estas herramientas.

### <a name="additional-recommendations"></a>Recomendaciones adicionales

Además de asegurarse de que el componente admite la creación de títulos que son compatibles con los requisitos de juegos para Windows, hay algunas otras consideraciones que debe tener en cuenta al diseñar e implementar una biblioteca o una utilidad de soporte para un juego de Windows.

-   Para admitir desarrolladores que trabajan en aplicaciones x64 nativas de 64 bits, proporcione versiones nativas de 32 bits y de 64 bits de las bibliotecas. La versión de 32 bits debe ser compatible con 64 bits por 2,2. Las bibliotecas de aplicaciones de 32 bits no deben suponer que el bit alto de cualquier dirección de 32 bits no se utiliza para admitir el uso dentro de las aplicaciones x86 de LARGEADDRESSAWARE.
-   Si proporciona encabezados de código nativo (C/C++), use la sintaxis de atributo del lenguaje de anotación estándar (SAL) para decorar las rutinas de la API pública. Esto permitirá a los usuarios de la biblioteca obtener el máximo beneficio de usar el análisis de código estático (/Analyze), que forma parte de Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium y Visual Studio 2010 Ultimate, así como las herramientas de compilador de Windows SDK disponibles públicamente.
-   Si el producto crea subprocesos dentro del proceso del usuario, asegúrese de asignar un nombre a cada subproceso para que las herramientas de depuración puedan anotar correctamente los subprocesos en ejecución.
-   Si escribe rutinas que están diseñadas para ser llamadas dentro de un bucle principal del juego, use las rutinas de D3DX D3DPERF \_ BeginEvent/EndEvent y D3DPERF \_ SetMarker para anotar operaciones de alto nivel para facilitar la identificación de los cuellos de botella mediante PIX para Windows.
    > [!Note]  
    > Para la funcionalidad de diagnóstico de gráficos de Visual Studio 2012, estas rutinas de D3DX y PIX se sustituyen por la interfaz [**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) .

     

-   En el caso de las bibliotecas de red, proporcione implementaciones independientes de IP y evite rutinas solo en desuso de IPv4 para admitir las tecnologías IPv6 y Teredo en Windows XP con Service Pack 2, Windows Vista y Windows 7.
-   Los proveedores de servicios de juegos deben registrarse en el explorador de juegos mediante la versión 2 del esquema GDF y hacer uso de la característica RSS para proporcionar noticias relacionadas con el servicio.

### <a name="games-for-windows-showcases"></a>Juegos para Windows Showcase

### <a name="introduction"></a>Introducción

Los juegos para Windows exhibes van más allá de ofrecer una experiencia de juegos sólida en equipos Windows. Mediante la implementación de estas características, los juegos pueden agregar más entusiasmo a la experiencia del usuario en las plataformas Windows más recientes.

Los juegos para títulos de Windows deben cumplir todos los requisitos técnicos que se enumeran en este artículo, pero las características de presentación son opcionales. Estos títulos son gratuitos para implementar algunos, ninguno o todas estas presentaciones.

### <a name="s1-exploit-direct3d-11"></a>S. 1 aprovechar Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Direct3D 11 es la API de representación de próxima generación para Windows Vista y Windows 7. Los juegos que aprovechan Direct3D 11 usan contenido optimizado, técnicas de representación avanzadas y nuevas características de hardware para crear una experiencia atractiva en hardware que admita 10, 10,1 y 11.

Si el juego también implementa Direct3D 9, una comparación en paralelo debe demostrar una mejora perceptible en la calidad del contenido, la fidelidad visual, el rendimiento, la complejidad de la escena y otras áreas de fidelidad de los gráficos para Direct3D 11. Esta compatibilidad está sujeta al requisito técnico 1,7 de juegos para Windows.

La tecnología 10level9 de Direct3D se puede usar para admitir el hardware de vídeo de Direct3D 9/3.0 de modelo de sombreador 2.0/3.0 en Windows Vista y Windows 7, en lugar de usar una implementación de Direct3D 9 en paralelo para una amplia compatibilidad de hardware. Sin embargo, esto no es suficiente para demostrar este escaparate.

En los equipos que ejecutan Windows Vista o Windows 7 con Direct3D 11 instalado, el juego debería usar Direct3D 11 de forma predeterminada.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

La API de Direct3D 11 se basa en la infraestructura de Windows Display Driver Model (WDDM) y Direct3D 10,1 para admitir nuevas funcionalidades: teselación de hardware, sombreadores de cálculo, representación multiproceso y creación de recursos, nuevos formatos de compresión de textura y un lenguaje de sombreador más flexible. Direct3D 11 proporciona compatibilidad de hardware unificada para las tarjetas de vídeo modernas, incluidas la última generación de las partes de Direct3D 11, todas las tarjetas de vídeo de Direct3D 10 y 10,1 y muchas tarjetas de vídeo de Direct3D 9 de modelo de sombreador 2.0/3.0, que es el hardware de vídeo mínimo necesario para el escritorio de Aero 3D.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

La migración de un motor de representación de Direct3D 9 para usar la nueva interfaz de Direct3D 11 es una tarea bien definida:

-   Elimine todas las operaciones de función fija en favor de los sombreadores programables.
-   Actualice todos los sombreadores existentes a la nueva sintaxis del modelo de sombreador 4. x/5.
-   Actualice la administración de recursos para admitir el nuevo modelo de vista.
-   Convierta todos los recursos para usar una nueva lista de formatos disponibles.
-   Actualice el control del estado de representación para utilizar bloques de estado inmutables y retrabaje las constantes del sombreador en búferes de constantes.

Esta conversión es esencial para habilitar la presentación de Direct3D 11, aunque el resultado no cumple el requisito de presentación de la explotación de la nueva API.

La nueva API y el modelo de programación de HLSL asociado ofrecen muchas oportunidades para el contenido mejorado:

-   Aprovechar las características de hardware de Direct3D 10 existentes, como el sombreador de geometría, las secuencias de flujo, las matrices de texturas y los formatos de textura comprimidos de las texturas BC4/BC5.
-   Aprovechar las características de hardware existentes de Direct3D 10,1, como los modos de mezcla independientes por representación y destino, la lectura de profundidad de MSAA, el acceso al sombreador de ejemplo de MSAA, las matrices de mapa de cubos y la representación en los formatos comprimidos (BC).
-   Implementación de algoritmos de GPU avanzada con el sombreador de cálculo con CS4. x en tarjetas de vídeo de Direct3D 10/10.1 existentes (habilitadas por controladores de vídeo actualizados) o CS 5,0 en tarjetas de vídeo Direct3D 11 de próxima generación.
-   Representación en varios subprocesos mediante la creación de recursos de subprocesos libres y varios contextos de dispositivo para mejorar el rendimiento en los sistemas de varios núcleos (con controladores de vídeo actualizados). Para obtener más información, consulte juegos para Windows Showcase S. 3.
-   Usar nuevas características del hardware de vídeo de clase de Direct3D 11, como la teselación de hardware con sombreadores de casco y de dominio, las características de hardware del sombreador de modelo de sombreador 5,0 BC6HBC7 formatos de textura comprimidos y la vinculación dinámica del sombreador.

Las técnicas que se pueden implementar con Direct3D 9 (en gran medida a través de un alto costo de CPU) pueden estar descargadas en la GPU de un modo eficaz, lo que libera los recursos de CPU para admitir otras demandas de juego.

Las API de Direct3D 11, las herramientas de soporte y los ejemplos están disponibles en el SDK de DirectX. Vea también API de gráficos en Windows.

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S. 2 explotación de x64 nativo

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

El juego incluye un archivo ejecutable nativo de 64 bits que ofrece una nueva experiencia convincente habilitada por las ediciones x64 de Windows que se ejecutan en hardware compatible con x64. Una comparación en paralelo con la versión de 32 bits del juego debería mostrar una mejora perceptible en la complejidad del contenido, los tiempos de carga totales reducidos y el rendimiento.

En las ediciones de 64 bits de Windows, la instalación siempre debe configurar la versión nativa de 64 bits del juego como valor predeterminado para los accesos directos en el explorador de juegos y en Windows XP Professional x64 Edition. Si se desea la instalación dual, se puede especificar una tarea de reproducción adicional para el explorador de juegos en Windows Vista y Windows 7 que apunta a la versión de 32 bits, pero el valor predeterminado debe permanecer en la versión nativa de 64 bits.

Tenga en cuenta que el juego debe admitir las ediciones de 64 bits de Windows Vista y Windows 7 para cumplir esta recomendación de presentación. Se recomienda la compatibilidad con Windows XP Professional x64 Edition, pero no es necesario.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

la tecnología x64 proporciona capacidades de direccionamiento de 64 bits para los mercados de consumidor y de servidor que incluyen compatibilidad con versiones anteriores de 32 bits de velocidad completa para las aplicaciones existentes. x64 es una parte fundamental de la guía básica para AMD (AMD64) e Intel (EMT64), y, con la excepción de las CPU ultra móviles, admite la tecnología para todos los procesadores de generación actuales y futuros.

Windows XP Professional x64 Edition era el primer sistema operativo Windows (SO) orientado al consumidor para admitir la tecnología x64, y Windows Vista y Windows 7 amplían en gran medida la disponibilidad de la habilitación del sistema operativo para la informática de consumidores de 64 bits. Con 2 GB de RAM como estándar en muchos equipos nuevos, las mejoras adicionales en el escalado de memoria no beneficiarán a las aplicaciones individuales de 32 bits que no pueden abordar más de 2 GB de RAM física. Hoy en día, muchos juegos están enfrentando desafíos que encajan todo el contenido disponible en las restricciones de 2 GB de espacio de direcciones virtuales, especialmente cuando se combinan con los grandes recuerdos de vídeo disponibles en las GPU de alto nivel, y el cambio a la tecnología x64 aumenta en gran medida los niveles de detalle compatibles.

la compatibilidad con x64 para juegos de 32 bits es un juego de requisitos técnicos de Windows (2,2), pero aprovechar al máximo las nuevas tecnologías requiere una implementación nativa de 64 bits.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

La principal ventaja del direccionamiento de 64 bits es la capacidad de acceder directamente a más de 2 GB de memoria física y virtual. El espacio de direcciones de memoria virtual grande permite el uso extensivo de e/s asignada a memoria sin preocuparse por los problemas de agotamiento del espacio de direcciones de la máquina virtual que se usan con frecuencia en la programación de 32 bits. Los juegos pueden aprovechar el nuevo espacio para mejorar considerablemente los tiempos de carga o, en algunos casos, para eliminar las pausas para cargar el contenido.

Las aplicaciones de 32 bits existentes pueden beneficiarse de las ediciones x64, ya que tienen la capacidad de procesar direcciones con datos de 32 bits completos cuando se compilan con la opción de vinculador habilitar direcciones grandes (**/LARGEADDRESSAWARE**). En las versiones de 32 de 64 bits de Windows XP, los modos de arranque especiales permitían que estas aplicaciones abordaran hasta 3 GB de RAM, y las ediciones x64 proporcionan acceso de hasta 4 GB de RAM para aplicaciones de gran tamaño (LAA). Aunque el uso de LAA en una aplicación de 32 bits no cumple este requisito de presentación, esta tecnología de puente es una forma muy útil de proporcionar ventajas de escalado adicionales en versiones x64 de Windows para los que no implementan completamente este requisito de presentación.

Para obtener más información, consulte [programación de 64 bits para desarrolladores de juegos](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) y [RAM, VRAM y más RAM: el juego de 64 bits está aquí](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) en Gamasutra.

> [!Note]  
> Un desafío clave para este escaparate es garantizar que las bibliotecas de terceros o los componentes en los que se basa el juego estén disponibles para el desarrollo nativo de 64 bits. Muchas API heredadas de Microsoft también se han eliminado del entorno nativo de 64 bits, que puede demostrar un desafío para las bases de código de motor que contienen implementaciones de sistemas clave anteriores.

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>S. 3 procesadores de Many-Core de vulnerabilidades

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

El juego implementa características que aprovechan los procesadores de varios núcleos, escalando a 3, 4 o más núcleos, cuando estén disponibles.

Si el juego es compatible con sistemas de un solo procesador o de doble núcleo, una comparación en paralelo con un sistema de cuatro núcleos debe demostrar nuevas características perceptibles, efectos atractivos adicionales, mejora de la calidad del contenido o rendimiento mejorado.

Dado que los juegos ya admiten el ajuste de escala de doble núcleo, y se usan automáticamente en varias mejoras del controlador de Direct3D, el escalado de doble núcleo no es suficiente para demostrar este escaparate.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

El crecimiento continuo del rendimiento de las CPU ha cambiado de las mejoras de velocidad de reloj a la adición de núcleos de cálculo. Tanto el mapa de ruta de AMD como el de Intel se basan en diseños escalables y multinúcleo. Todas las plataformas de juegos de última generación tienen CPU de varios núcleos debido a este cambio fundamental en la evolución de los procesadores. Las aplicaciones de un solo subproceso ya no verán mejoras significativas en las CPU de próxima generación. El multithreading simple también producirá un error de escalado, ya que el número de núcleos de CPU en uso común crece hasta tres o más.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Tenga en cuenta que los recuentos de núcleos no deben ser una potencia de dos, por lo que los juegos deben escalarse linealmente y controlar los recuentos de núcleos de 3, 4, 5, 6, 7, 8, etc.

El escalado mediante el aumento del número de subprocesos de una aplicación solo proporciona un valor devuelto si el costo de la comunicación y la sincronización de subprocesos se mantienen en comprobación. El escalado basado en características puede demostrar una solución más sencilla a corto plazo, lo que permite que el juego funcione normalmente sin los subprocesos adicionales en los sistemas de un solo núcleo y que los habilite cuando esté disponible la potencia de CPU adicional.

Para obtener más información, consulte [codificación de varios núcleos en xbox 360 y Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) y [consideraciones sobre la programación con bloqueo para Xbox 360 y Microsoft Windows](/windows/desktop/DxTechArts/lockless-programming) en los artículos de DirectX, así como la utilidad DXUTLockFreePipe y el ejemplo CoreDetection.

El uso de los contextos de dispositivo y la creación de recursos de subprocesos libres de Direct3D 11 es útil para lograr una escalabilidad de varios núcleos en la representación y carga de recursos de gráficos. Consulte juegos para Windows Showcase S. 1.

Tenga en cuenta que el uso de la instrucción de CPU RDTSC directamente, en lugar de usar las API de Windows para calcular el tiempo en los sistemas de varios núcleos, puede provocar problemas en algunas configuraciones de hardware y del sistema operativo. consulte [procesadores de temporización y multinúcleo de juegos](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) en los artículos de DirectX.

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>S. 4 compatibilidad con juegos para Windows: LIVE

Microsoft ya no admite juegos para Windows LIVE.

### <a name="s5-support-windows-touch"></a>S. 5 compatibilidad con Windows Touch

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Los juegos con capacidad táctil de Windows se pueden reproducir mediante gestos táctiles y/o en equipos que ejecutan Windows 7 con una pantalla táctil. También se puede usar la entrada mediante teclado, pero la interfaz de reproducción principal debe estar basada en el toque.

La habilitación de la función táctil no debe evitar el uso del mouse o del controlador común, sujeto al requisito técnico 1,4.

No se espera que el instalador del juego admita la funcionalidad de Windows Touch.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Las pantallas multitáctiles para equipos están disponibles para portátiles y equipos de escritorio, y representan una característica de hardware clave que se está promocionando con la versión de Windows 7. Windows 7 es compatible con Windows Touch en las interfaces de escritorio y de controles comunes.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Las aplicaciones de código nativo pueden tener acceso a múltiples entradas a través de los \_ mensajes Touch de WM, en combinación con la función [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) . Vea también la API de manipulaciones e inercia.

Windows Presentation Foundation (WPF) 4,0 proporciona una solución administrada para interfaces multitáctiles.

Para obtener más información, consulte el SDK de Windows Touch.

</dd> </dl>

### <a name="s6-support-high-color"></a>S. 6 compatibilidad con color alto

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requerido**
</dt> <dd>

Los juegos que admiten el color de alta densidad usan un formato 10:10:10:2 ( \_ \_ R10G10B10A2 formato de DXGI, D3DFMT \_ A2B10G10R10) o 16:16:16:16 (formato de DXGI \_ \_ R16G16B16A16, D3DFMT \_ A16B16G16R16) para el modo de presentación en el búfer de reserva y de pantalla completa.

Mediante el uso de un destino de representación de alto color, el contenido del intervalo de High-Dynamic (HDR) se puede representar con una gama amplia o extendida al realizar la asignación de tono en un intervalo de 10 o 16 bits.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Razonamiento**
</dt> <dd>

Los monitores han sido capaces de mostrar más de 256 niveles de color por canal durante muchos años, incluso cuando las pantallas de CRT eran predominantes. La detección de hardware en tarjetas de vídeo ha sido el factor de limitación. Las GPU modernas, incluida la mayoría del hardware de nivel de Direct3D 9 y todo el hardware de clase de Direct3D 10 y mejor, tienen un hardware de análisis capaz de tener al menos 10 bits por canal, y la capacidad de hardware se establece para crecer hasta los 16 bits por canal de color en el futuro. Los sistemas de interconexión de HD TV (HDMI, DisplayPort) se han diseñado para administrar más de 8 bits por canal, y el VGA analógico ya realizará dichas señales.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Tenga en cuenta que color alto, o HI color, históricamente hace referencia a pasar de las pantallas de color 256 (8 bits) a las pantallas de color de 15 o 16 bits. La mayoría de los sistemas de pantalla tienen mucho tiempo, ya que se mueven a un color verdadero que es un color de 24 bits, u 8 bits por canal de color para rojo, verde y azul. En este caso, se trata de una nueva generación de sistemas de muestra que pueden funcionar con más de 8 bits por canal de color individual. También se conoce como color en profundidad.

</dd> </dl>

### <a name="recommended-best-practices"></a>Prácticas recomendadas

### <a name="introduction"></a>Introducción

Además de cumplir los requisitos técnicos y adoptar una o más presentaciones en su título, hay una serie de prácticas recomendadas que deben seguirse para todos los juegos de Windows. Aunque estas recomendaciones quedan fuera del ámbito de los principales requisitos técnicos, se recomienda su uso en todos los juegos de títulos de Windows.

### <a name="additional-recommendations"></a>Recomendaciones adicionales

-   Use el compilador y el tiempo de ejecución más recientes de Visual Studio. Las versiones más recientes del compilador implementan mejoras significativas en la calidad del código generado y en los problemas de seguridad, y emplean estrategias modernas de optimización del procesador. La actualización del compilador y el uso del tiempo de ejecución de C más reciente es una forma sencilla de migrar a las prácticas de codificación modernas.
-   Use la versión de biblioteca de vínculos dinámicos (DLL) del tiempo de ejecución de C, en lugar de la vinculación estática, y use CRT seguro. (Las excepciones se pueden realizar en casos especiales de preinstalación, como para un programa de ejecución automática o para el propio instalador).
-   Para juegos de audio, use XAudio2, X3DAudio y/o XACT, en lugar de DirectSound. En el caso de los motores de audio que realizan toda la combinación y la conversión de velocidad de origen y solo necesitan una solución de baja latencia para la salida de audio, use DirectSound en Windows XP (solo) y WASAPI en Windows Vista y Windows 7.
-   Evite usar las API heredadas y en desuso: DirectDraw, DirectSound, DirectPlay, nivel de rendimiento de DirectMusic, voz de DirectPlay y modo de retención de Direct3D. Tenga en cuenta que no está disponible en absoluto en Windows Vista o Windows 7 el modo retenido de DirectPlay Voice y Direct3D. La capa de rendimiento de DirectPlay y DirectMusic no está disponible para las aplicaciones nativas x64.
-   Optimice el uso de conjuntos de instrucciones SIMD SSE/SSE2. Vea la API de [DirectXMath](/windows/desktop/dxmath/directxmath-portal) en el Windows SDK como una solución multiplataforma para las operaciones matemáticas optimizadas para SIMD.
-   Use los procedimientos recomendados modernos para la seguridad de Windows (incluidas las opciones del compilador y del enlazador como **/NXCompat**, **/GS**, **/SAFESEH**, **/dynamicbase**, **/SDL**, etc.). Para obtener más información, vea [procedimientos de seguridad recomendados para el desarrollo de juegos](/windows/desktop/DxTechArts/best-security-practices-in-game-development).
-   Use las bibliotecas y los componentes de Windows SDK más recientes. Quite las dependencias de los componentes fuera de banda de DirectSetup heredados, como D3DX9, D3DX10 y D3DX11. Considere el uso de [DirectXTex](https://github.com/Microsoft/DirectXTex) o [DirectXTK](https://github.com/Microsoft/DirectXTK) o ambos.
-   Evite usar el anterior compilador de HLSL y, en su lugar, use el compilador de HLSL moderno. Si la aplicación requiere compatibilidad con el sombreador de píxeles 1. x, use el ensamblado de sombreador en lugar de HLSL o limite el uso del compilador anterior a solo esos escenarios.

## <a name="resources"></a>Recursos



| Término                                                                                                                                                                                                                         | Descripción                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Juegos para Windows: casos de prueba <br/>                              | Prácticas recomendadas para juegos en Windows XP, Windows Vista y Windows 7<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK <br/>                                                                                                      | [SDK de Windows](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Directrices de control de cuentas de usuario <br/>                      | [Requisitos de desarrollo de aplicaciones de Windows Vista para la compatibilidad de control de cuentas de usuario](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portal para desarrolladores de WinQual <br/>                                                  | [Servicios en línea de calidad de Windows (WinQual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>Portal para desarrolladores de DirectX <br/>                                                  | [Centro para desarrolladores de DirectX](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog de juegos para Windows y DirectX SDK<br/> | [Juegos para Windows y el SDK de DirectX](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artículos adicionales de DirectX<br/>                                             | [Artículos técnicos de DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

