---
title: 'Requisitos técnicos de Games for Windows: procedimientos recomendados para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8'
description: En este artículo se proporcionan requisitos técnicos y procedimientos recomendados para juegos que se ejecutan en Windows.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a5c1480f8ef5ef67a2bd2b998e0dcbe28ed397
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482121"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Requisitos técnicos de Games for Windows: Procedimientos recomendados para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8

En este artículo se proporcionan requisitos técnicos y procedimientos recomendados para juegos que se ejecutan en Windows. Hemos escrito estos requisitos técnicos y procedimientos recomendados principalmente para abarcar Windows Vista y Windows 7, así como el sistema operativo Windows XP heredado. Estos procedimientos recomendados también se aplican generalmente a los juegos Win32 de escritorio Windows 8.

Este artículo contiene estas secciones:

-   [Diferencias entre Windows 8](#differences-for-windows-8)
    -   [Información adicional](#additional-information)
-   [Juegos para Windows](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [1.1 Integración de Games Explorer](#11-games-explorer-integration)
    -   [1.2 Compatibilidad con la seguridad familiar y los controles parentales](/windows)
    -   [1.3 Compatibilidad con juegos guardados enriquecidos](#13-support-rich-saved-games)
    -   [1.4 Compatibilidad con el controlador Xbox 360 común para Windows \[ condicional\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)
    -   [1.5 Compatibilidad con varias relaciones de aspecto y resoluciones](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [1.6 Inicio de soporte técnico desde Windows Media Center](#16-support-launch-from-windows-media-center)
    -   [1.7 Compatibilidad con Direct3D](#17-direct3d-support)
    -   [1.8 Habilitar alta reconocimiento de PPP](#18-enable-high-dpi-aware)
-   [Seguridad y compatibilidad](#security-and-compatibility)
    -   [2.1 Siga las instrucciones de control de cuentas de usuario](#21-follow-user-account-control-guidelines)
    -   [2.2 Compatibilidad Windows versiones x64](#22-support-windows-x64-versions)
    -   [2.3 Archivos de firma](#23-sign-files)
    -   [2.4 Controladores de firma](#24-sign-drivers)
    -   [2.5 Realización de la comprobación de la versión correcta](#25-perform-proper-version-checking)
    -   [2.6 Compatibilidad con sesiones de usuario simultáneas](#26-support-concurrent-user-sessions)
    -   [2.7 Compatibilidad con nombres largos](#27-support-long-names)
-   [Instalación](#32-support-user-account-control-for-installation)
    -   [3.1 Compatibilidad con una instalación sencilla](#31-support-easy-installation)
    -   [3.2 Compatibilidad con el control de cuentas de usuario para la instalación](#32-support-user-account-control-for-installation)
    -   [3.3 Instalar en carpetas correctas](#33-install-to-correct-folders)
    -   [3.4 Instalación Windows recursos correctamente](#34-install-windows-resources-properly)
    -   [3.5 Evitar reinicios durante la instalación](#35-avoid-reboots-during-installation)
    -   [3.6 Usar el control de versiones de archivos correctamente](#36-use-file-versioning-correctly)
    -   [3.7 Compatibilidad con el requisito condicional de ejecución \[ automática\]](#37-support-autorun-conditional-requirement)
-   [Confiabilidad](#reliability)
    -   [4.1 Eliminar reinicios innecesarios](#41-eliminate-unnecessary-reboots)
    -   [4.2 Eliminar Application Verifier errores](#42-eliminate-application-verifier-failures)
    -   [4.3 Compatibilidad con Informe de errores de Windows información de versión de archivo](#43-support-windows-error-reporting-and-file-version-information)
-   [Xbox 360 Common Controller for Windows Terminology](#xbox-360-common-controller-for-windows-terminology)
-   [Directrices para productos de middleware de juegos](#guidelines-for-game-middleware-products)
    -   [Introducción](#introduction)
    -   [Otros Recomendaciones](#additional-recommendations)
    -   [Juegos para Windows presentación](#games-for-windows-showcases)
-   [Recursos](#resources)

## <a name="differences-for-windows-8"></a>Diferencias entre Windows 8

Este es un resumen de las principales diferencias al aplicar estos requisitos técnicos y procedimientos recomendados a Windows 8.

<dl> <dt>

<span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**La interfaz de usuario del Explorador de juegos no está visible**
</dt> <dd>

Todos los juegos que se registran en [El Explorador](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) de juegos se abren como iconos en la nueva interfaz de usuario de Windows, pero muchos de los metadatos asociados al título ya no están visibles. Sigue utilizando la herramienta Creador de archivos de definición de juegos (GDFMAKER.EXE), que ahora está disponible en el Kit de desarrollo de software (SDK) de Windows, para crear los metadatos. También se usan los mecanismos existentes para implementar los metadatos. Siga comprobando el registro de Games Explorer mediante Windows 7 y compruebe que el nuevo icono de la interfaz de usuario de Windows aparece al instalarlo en Windows 8 (consulte [1.1 Games Explorer Integration](#11-games-explorer-integration)).

Para descargar el SDK Windows 8, consulte [Descargas para desarrollar aplicaciones de escritorio.](https://msdn.microsoft.com/windows/desktop/aa904949)

</dd> <dt>

<span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**El registro con las API de Game Explorer sigue siendo el mecanismo para registrar el juego con Windows parentales**
</dt> <dd>

Se recomienda ejecutar la versión del SDK de Windows de GDFMAKER en la versión publicada de Windows 8 para asegurarse de que puede rellenar todos los sistemas de clasificación admitidos actualmente.

> [!Note]  
> Esta versión de GDFMAKER requiere .NET 4.0.

 

Consulte [1.2 Support Family Safety / Parental Controls (Compatibilidad con la seguridad de las familias y los controles parentales).](/windows)

</dd> <dt>

<span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**Ahora hay tres opciones para usar la API XINPUT en función de sus requisitos.**
</dt> <dd>

XINPUT 1.4 está integrado en Windows 8. Tanto Windows store como las aplicaciones win32 de escritorio pueden usar XINPUT 1.4. Todas las versiones de Windows pueden usar XINPUT 9.1.0 para controladores comunes simplificados, pero no hay ningún paquete de redistribución con XINPUT 9.1.0. Todas las versiones Windows también pueden usar la versión XINPUT 1.3 del SDK de DirectX existente, que requiere que DirectSetup se implemente.

Vea [1.4 Support the Xbox 360 Common Controller for Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).

</dd> <dt>

<span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Solo se admite un conjunto limitado de aplicaciones Win32 de escritorio en Windows RT**
</dt> <dd>

Los juegos que se ejecutan Windows 7 pueden y deben ejecutarse correctamente en Windows 8 plataformas x86 y x64.

Consulte [Compatibilidad con la versión 2.2 Windows versiones x64](#22-support-windows-x64-versions).

</dd> <dt>

<span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Asegúrese de que las comprobaciones del sistema operativo se realizan correctamente.**
</dt> <dd>

La Windows 8 del sistema operativo es la 6.2. Windows 8 supera las pruebas de barra mínimas actuales que se recomiendan para la implementación de juegos.

</dd> <dt>

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**El paquete directX End-User Redistribution se ejecuta correctamente en Windows 8, como en Windows 7, para implementar D3DX9, D3DX10, D3DX11, XINPUT 1.3, XAUDIO 2.7, XACTEngine, entre otros.**
</dt> <dd>

Pero existe un problema conocido con DirectSetup en sistemas con solo .NET 4.0 instalado debido al control de implementación de los ensamblados heredados de DirectX 1.1 administrados. Este problema se aplica tanto a Windows 8, que se incluye con .NET 4.5 de forma predeterminada, como a los equipos de Windows XP nuevos con el entorno de ejecución de .NET 4.0 instalado. Pero este problema no se aplica a ninguna versión de .NET anterior a .NET 4.0. Aunque Windows 8 tiene un comportamiento de compatibilidad de aplicaciones para resolver este problema automáticamente (que requiere acceso a la red), se recomienda que los juegos que siguen implementando la actualización de DirectSetup en el SDK de DirectX (junio de 2010) actualicen la versión de los archivos REDIST. Como siempre, si usa DirectSetup para el título, recorte el título hasta el conjunto mínimo necesario de CAB.

Vea [3.4 Instalar Windows recursos correctamente.](#34-install-windows-resources-properly)

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Los juegos que requieren el entorno de ejecución compatible con .NET 2.0 (2.0, 3.0, 3.5) siguen usando los mecanismos de implementación existentes**
</dt> <dd>

Estos juegos desencadenan un comportamiento de compatibilidad de aplicaciones Windows 8 habilitar el entorno de ejecución de .NET 3.5 automáticamente (lo que requiere acceso a la red). Sin embargo, se recomienda que los desarrolladores de .NET pasen al entorno de ejecución de .NET 4.0.

> [!Note]  
> Los ensamblados heredados de DirectX 1.1 administrado no son compatibles con el entorno de ejecución de .NET 4.x.

 

Vea [3.4 Instalar Windows recursos correctamente.](#34-install-windows-resources-properly)

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**No se recomienda el uso de una corrección automática u otra tecnología previa a la instalación que se basa en .NET.**
</dt> <dd>

Puede suponer que solo los entornos de ejecución compatibles con .NET 2.0 (2.0, 3.0, 3.5) están presentes en Windows Vista y Windows 7. Solo el entorno de ejecución compatible con .NET 4.0 está presente en Windows 8 de forma predeterminada.

Vea [3.7 Support Autorun (Compatibilidad con la ejecución automática).](#37-support-autorun-conditional-requirement)

</dd> <dt>

<span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Hay una actualización de Application Verifier para Windows 8**
</dt> <dd>

El SDK Windows 8 incluye esta versión Application Verifier.

Vea [4.2 Eliminar Application Verifier errores.](#42-eliminate-application-verifier-failures)

</dd> </dl>

### <a name="additional-information"></a>Información adicional

<dl>

[Windows 8 y Windows Server 2012 de compatibilidad](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[¿Dónde está el SDK de DirectX?](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a>Juegos para Windows

**Resumen de los requisitos de juegos**

**Ventajas del cliente**

Los juegos informáticos son una experiencia de entretenimiento clave en Windows, pero las preocupaciones de facilidad de uso han provocado la frustración de los clientes a lo largo de los años. Tradicionalmente, los juegos se instalan como aplicaciones, pero se usan más como medios de entretenimiento (películas o canciones, por ejemplo). Las innovaciones, como Games Explorer, exponen los juegos de una manera coherente que es diferente de las aplicaciones estándar. Estas innovaciones también dan a los juegos un estado ciudadano de primera Windows, junto con Música e Imágenes. Los siguientes requisitos ayudan a garantizar que Windows Vista y Windows 7 proporcionan una experiencia de juego mejorada, más accesible y unificada. Al mismo tiempo, garantizan la compatibilidad con Windows XP.

### <a name="11-games-explorer-integration"></a>1.1 Integración de Games Explorer

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

El juego debe estar visible en El Explorador de juegos (la **carpeta Juegos)** en Windows Vista y Windows 7. Cuando se selecciona, el juego también debe mostrar metadatos correctos, que incluyen publicador, desarrollador, fecha de lanzamiento, versión, puntuaciones de índice de experiencia de Windows, clasificación (si procede) e hipervínculos asociados.

Si el juego se distribuye digitalmente a través de un servicio de juegos en línea, el proveedor de servicios también debe aparecer en El Explorador de juegos. Para garantizar el control adecuado del proveedor y habilitar el uso de fuentes RSS, se debe usar la versión 2 del esquema para los archivos de definición de juegos (GDF). (Para obtener más información sobre los GDF, vea Información adicional).

Además, los instaladores de juegos deben observar las siguientes reglas cuando se ejecutan en Windows Vista y Windows 7:

-   La instalación no debe crear un acceso directo para iniciar el juego en el escritorio, en el menú Inicio o en cualquier otra ubicación.
-   No se deben crear tareas ni métodos abreviados para la eliminación.
-   Los usuarios deben poder quitar el juego mediante programas y características en Panel de control en Windows Vista y Windows 7, o agregar o quitar programas en Panel de control en Windows XP.

En Windows XP y en versiones anteriores de Windows, el instalador de juegos puede crear grupos de programas, iconos de escritorio o accesos directos según sea necesario.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Windows El Explorador de juegos es similar en concepto a las carpetas Windows XP **Mis documentos** o **Mis imágenes.** La idea es centralizar contenido similar en un solo lugar y permitir actividades de organización y contextuales más sencillas. Games Explorer amplía el concepto **Mis documentos** **o Mis imágenes,** ya que permite una organización y un control más completos sobre los juegos. El Explorador de juegos permite a los jugadores ver, organizar e interactuar con todos los juegos instalados en sus sistemas. También permite a los editores de juegos comunicar información importante del juego de forma más eficaz. El sistema está controlado por datos, lo que facilita a un editor de juegos actualizar la información del juego a lo largo de la vida del producto.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

La integración con El Explorador de juegos requiere que cree un archivo de definición de juegos (GDF), que es un archivo de texto XML que se inserta dentro de un archivo binario (un archivo ejecutable o un archivo DLL) como un recurso, junto con un icono de Windows. A continuación, el juego debe registrarse en el Explorador de juegos. El GDF también permite la exposición de la información proporcionada, como el título del juego, el publicador, el desarrollador, los vínculos a sitios web y las tareas opcionales. Tenga en cuenta que las tareas de soporte técnico solo pueden ser vínculos a sitios web, pero también se pueden usar tareas de reproducción para tareas de soporte técnico opcionales.

Games Explorer puede usar una imagen de mapa de bits en miniatura, pero se recomienda que, en su lugar, proporcione un recurso de icono de Windows con iconos grandes (256 256). El recurso de icono debe incluir tamaños de imagen de 256 256 48 48, 32 32 y 16 16 en profundidades de color de 24 bits (Color verdadero) y de 8 bits (256). El editor de iconos proporcionado en Visual Studio 2008 y 2010 admite estos formatos de iconos grandes, al igual que IconWorkshop Lite.

Los detalles sobre la **integración Windows Games Explorer** se proporcionan en el SDK de DirectX. El SDK de DirectX incluye un editor de archivos de definición de juegos (GDF), así como un GDF de ejemplo que se incluye en GDFExampleBinary, un ejemplo. Otro ejemplo, GameUxInstallHelper, proporciona rutinas para integrar la funcionalidad necesaria en los sistemas de instalación existentes. El validador de archivos de definición de juegos (gdftrace.exe) proporciona compatibilidad con la depuración para evaluar un GDF. Consulte también "Windows Games Explorer Integration" en la documentación del SDK de DirectX para C++.

Windows 7 presenta compatibilidad con la segunda versión de un esquema para archivos GDF. La nueva versión incluye un método simplificado para crear tareas de juego y compatibilidad con notificaciones de actualización, proveedores de servicios de juegos, estadísticas de juegos y fuentes RSS para proveedores de servicios de juegos. La versión más reciente de GameUxInstallHelper controla todo el registro y la compatibilidad heredada necesarias para usar un archivo GDF de la versión 2 con Windows Vista. Use las herramientas y el código de ejemplo del SDK de DirectX de agosto de 2009 o posterior. Se recomienda usar un archivo GDF de la versión 2 para habilitar la compatibilidad con fuentes RSS, estadísticas de juegos y notificaciones de actualización. Consulte también los ejemplos ProviderGDFExampleBinary y GameStatisticsExample.

En Windows Vista Business Edition, Windows 7 Professional Edition y Enterprise Edition de Windows Vista y Windows 7, el vínculo Juegos de la menú Inicio está oculto. El Explorador de juegos sigue estando disponible en la menú Inicio clic en **Todos** los programas y, a continuación, en **Juegos.**

Para las aplicaciones asociadas que se instalan con el juego, pero no con ellos mismos, puede crear grupos de programas, accesos directos e iconos de escritorio de menú Inicio en todas las versiones de Windows, incluidos Windows Vista y Windows 7. Estas aplicaciones asociadas deben pasar los juegos aplicables para Windows requisitos; Para obtener más información, vea [Directrices para productos de middleware de juegos.](#guidelines-for-game-middleware-products) Se recomienda que los servicios de juegos se registren en Games Explorer como proveedor de juegos Windows 7. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1.2 Compatibilidad con la seguridad de la familia y los controles parentales

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Los juegos deben admitir completamente Windows seguridad de familia mediante el cumplimiento de las reglas siguientes:

-   Los juegos no deben requerir que el usuario tenga credenciales administrativas para jugar. La instalación, aplicación de revisiones y eliminación puede requerir credenciales administrativas, según los requisitos de la sección 3. (Relacionado con esto es el requisito 2.1, Seguir las directrices de control de cuentas de usuario).
-   Los juegos clasificados por Windows de clasificación admitidos por el usuario, como ESRB y PEGI, deben incluir la información de clasificaciones asignada en su archivo de definición de juegos (GDF). Todos los datos de clasificaciones disponibles deben incluirse en todas las versiones localizadas de GDF, así como en la versión neutra del idioma.
-   Los juegos deben enumerar sus archivos ejecutables en GDF para proporcionar una buena experiencia de usuario para las restricciones generales de aplicaciones, a menos que el juego use una tecnología antiseduría que crea ejecutables con nombre aleatorio en tiempo de ejecución.
-   Los juegos deben llamar al **método VerifyAccess** de la interfaz de Games Explorer durante el inicio, si está disponible, y salir si devuelve \* pfHasAccess como FALSE.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Todos los juegos deben ejecutarse en el contexto de una cuenta de usuario estándar para permitir que las cuentas controladas por Windows Parental Controls puedan jugar al juego. Los padres quieren la capacidad de supervisar y controlar el acceso de sus hijos a los juegos. Además, numerosos grupos del sector, el gobierno y la defensa desean mejores formas de permitir que los padres supervisen y controlen los juegos a los que se exponen sus hijos. Junto con la arquitectura que ofrece Games Explorer, Microsoft proporciona a los padres esta capacidad a través Windows controles parentales.

Incluso para los juegos que no participan en un programa de la tabla de clasificaciones, requerir privilegios elevados crea una experiencia de juego deficiente para la mayoría de las cuentas de usuario. Este es especialmente el caso si están habilitados los controles parentales, lo que requeriría que el elemento primario escriba la contraseña de administrador cada vez que se inicia el juego.

El Windows control parental permite a los padres seleccionar las clasificaciones que creen adecuadas para sus hijos. Los controles parentales admiten muchos de los sistemas de clasificación en todo el mundo. Los controles parentales también permiten a los padres restringir el acceso a juegos basados en descriptores de contenido (si el sistema de clasificación aplicable los admite) y permitir o no el acceso a juegos individuales.

La opción predeterminada del sistema de clasificación para los controles parentales de Windows se basa en  la configuración regional del sistema, pero el usuario puede modificarla en Opciones regionales y de idioma **en Panel de control**. Por lo tanto, todos los idiomas admitidos deben proporcionar todos los datos de clasificaciones disponibles para que el usuario tenga la libertad de seleccionar el tablero de clasificaciones que desee.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Los juegos sin una clasificación todavía deben cumplir los requisitos para admitir el juego como usuario estándar y para llamar a **VerifyAccess**. Estos juegos tienen como valor predeterminado la categoría Sin clasificación, muestran el texto "No se proporciona clasificación" en el Explorador de juegos y están sujetos a la configuración **Restricciones** de juegos en Controles **parentales** para juegos no clasificados. El valor **predeterminado de Restricciones** es Permitir.

La información de clasificación en GDF se omitirá si el binario que contiene no está firmado correctamente Authenticode. Consulte el requisito 2.3.

El Editor de archivos de definición de juegos del SDK de DirectX incluye todos los sistemas de clasificaciones admitidos y replicará correctamente esta información en todas las versiones localizadas de GDF, así como en una versión neutra del lenguaje. La herramienta GDFTrace descodificará y comprobará toda la información de clasificaciones presente. Use la versión de agosto de 2009 o posterior de estas herramientas.

El GDF de un proveedor de juegos normalmente no contiene información de clasificación y está sujeto a la configuración del contenido no clasificado.




| Sistema operativo | Sistemas de clasificación admitidos | 
|------------------|--------------------------|
| Windows Vista | <ul><li>CERO (Japón)</li><li>ESRB (EE. UU.)</li><li>OFLC (Australia)</li><li>PEGI (Europa)</li><li>PEGI De Noruega (en desuso)</li><li>PEGI Portugal</li><li>PEGI/BBFC (Reino Unido)</li><li>USK (Alemania)</li></ul> | 
| Windows Vista con un Service Pack | Los Service Pack para Windows Vista agregan compatibilidad con lo siguiente:<br /><ul><li>GRB (Corea del Sur)</li><li>Descriptores de contenido variantes de esrb</li></ul> | 
| Windows 7 | Windows 7 admite los sistemas de clasificación admitidos por Windows Vista y agrega compatibilidad con lo siguiente: <br /><ul><li>CSRR (Taiwán)</li></ul> | 
| Windows 8 | Windows 8 admite los sistemas de clasificaciones anteriores y agrega compatibilidad con lo siguiente:<br /><ul><li>HAE-AU (Australia)</li><li>DJCTQ (Brasil)</li><li>PFB (Sudáfrica)</li><li>OFLC-NZ (Nueva Zelanda)</li></ul>Windows 8 soporte técnico para los siguientes sistemas ahora en desuso:<br /><ul><li>PEGI-FI (Finlandia)</li><li>OFLC (Australia)</li></ul> | 




 

> [!Note]  
> Cualquier título que incluya nuevos descriptores de contenido de ESRB Windows Vista Service Pack 1 (SP1) se mostrará como No clasificado en Windows Vista sin service pack.

 

Los datos de clasificaciones más recientes se omiten en las versiones de los sistemas operativos sin compatibilidad con ellos. La variante PEGI (Finlandia) está ahora en desuso en favor del sistema de clasificación ESTÁNDAR DE PEGI (Europa). El sistema OFLC está ahora en desuso en favor de LA HAA para Australia.

Para obtener más información sobre cómo hacer que un juego sea compatible con privilegios de usuario estándar, consulte el artículo de DirectX Control de cuentas de [usuario para desarrolladores de juegos.](/windows/desktop/DxTechArts/user-account-control-for-game-developers)

Consulte el requisito 1.1 para obtener más detalles sobre el archivo de definición de juego (GDF).

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1.3 Compatibilidad con juegos guardados enriquecidos

\[Este requisito se ha retirado\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1.4 Compatibilidad con el Xbox 360 common controller for Windows \[ conditional requirement\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Los juegos que admiten controladores de controlador de controlador de juegos deben admitir Mando Xbox 360 para Windows mediante la API [XInput.](/windows/desktop/xinput/xinput-game-controller-apis-portal) Si también se admiten periféricos DirectInput, también se puede usar DirectInput. Sin embargo, XInput debe ser la API predeterminada si se usa Xbox 360 dispositivo compatible.

Todas las referencias a los botones y desencadenadores de controlador comunes deben usar Xbox 360 nombres. Consulte la [Xbox 360 Common Controller for Windows Terminology list](#xbox-360-common-controller-for-windows-terminology) (Terminología de common controller for Windows para obtener más información).

La vibración del controlador debe desactivarse cuando el juego está en estado pausado o suspendido.

El control mouse/teclado no se puede deshabilitar completamente en ningún momento. Como mínimo, debe estar disponible una opción para volver a los menús del juego.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Este requisito proporciona a los jugadores libertad de elección para usar el controlador Xbox 360 o el teclado y el mouse, en función del método de entrada que sea más natural e intuitivo.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Este requisito no se aplica a los juegos que usan solo el mouse o el teclado.

Se recomienda implementar la navegación por menús para usar los botones de controlador estándar ampliamente aceptados:

-   A: Aceptar
-   B- Cancelar
-   Inicio: aceptar o pausar
-   Copia de seguridad: cancelar, hacer una copia de seguridad de una pantalla o subir un nivel de menú

Para obtener más información, vea [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal).

En el tema [XInput y DirectInput](/windows/desktop/xinput/xinput-and-directinput) se describen los problemas con el uso de ambas API al mismo tiempo.

Se recomienda no usar DirectInput para implementar controles de teclado o mouse. Los controles de teclado y mouse solo deben implementarse mediante Windows y las API de Win32. Para obtener más información sobre cómo obtener información sobre el movimiento del mouse de alta resolución sin usar DirectInput, consulte Aprovechar las [ventajas High-Definition movimiento del mouse.](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement)

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1.5 Compatibilidad con varias relaciones de aspecto y resoluciones

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

El juego debe admitir al menos las siguientes relaciones de aspecto y resoluciones de pantalla asociadas:

-   4:3 normal (800 600 o 1024 768)
-   16:9 widescreen (1280 720)
-   16:10 widescreen (1152 720, 1680 1050 o 800 480)

Para la configuración y detección de la resolución de pantalla, el juego debe cumplir las reglas siguientes:

-   El juego usa la resolución de escritorio del dispositivo de pantalla de forma predeterminada si es una resolución compatible. La relación de aspecto del escritorio debe usarse como criterio de búsqueda si el juego elige una resolución predeterminada diferente.
-   El juego debe pedir al usuario que confirme la nueva configuración de pantalla cuando se realiza un cambio. Si el usuario no acepta en 15 segundos, la pantalla debe revertir a la configuración anterior.
-   El juego no debe extender píxeles ni centrar una ventana de representación 4:3 para admitir relaciones de aspecto de pantalla ancha. Sin embargo, el uso de letterboxing es aceptable.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Con el Windows 3D, no se puede suponer una relación de aspecto o resolución determinadas, debido a los siguientes factores:

-   Compatibilidad con pantallas de alto detalle.
-   Mayor cuota de mercado de los monitores widescreen.
-   Implementaciones DE LAN para Windows Media Center.
-   Requisitos de accesibilidad.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Idealmente, el juego tiene como valor predeterminado la relación de aspecto nativo de la pantalla. Sin embargo, obtener esta información de forma confiable puede ser un desafío, por lo que como solución más general, el juego puede suponer que el escritorio se ejecuta en la relación de aspecto nativa. La resolución de escritorio se puede obtener llamando [**a EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) con ENUM \_ REGISTRY \_ SETTINGS.

Para obtener más información, vea las secciones Relación de aspecto y Widescreen del artículo de DirectX Introducción a la experiencia de [10](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers)pies para Windows game developers .

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>1.6 Inicio de soporte técnico desde Windows Media Center

\[Este requisito se ha retirado.\]

### <a name="17-direct3d-support"></a>1.7 Compatibilidad con Direct3D

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Si el juego usa Direct3D, la versión mínima admitida debe ser Direct3D 9 y Direct3D debe ser el representador predeterminado seleccionado.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

La Windows vista y Windows de gráficos de 7 núcleos está diseñada en torno a Direct3D. Direct3D 8 y versiones anteriores se admiten mediante la reapping de interfaces heredadas.

Se recomienda encarecidamente usar versiones de Direct3D más recientes que Direct3D 9. Consulte Games for Windows Showcase S.1. Requerir Direct3D 10 o Direct3D 11 es totalmente compatible con el requisito 1.7.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1.8 Habilitar alta reconocimiento de PPP

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Los juegos y sus instaladores deben ejecutarse correctamente sin problemas visuales cuando el escalado de puntos por pulgada (PPP) está habilitado (probado con 144 PPP para un escalado del 150 % con una resolución de pantalla de 1600 1200) en Windows Vista y Windows 7.

Esto normalmente requiere que el ejecutable del juego declare que es compatible con PPP. Esto se logra mediante la inserción de un elemento de manifiesto: <dpiAware> true <dpiAware> .

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Los monitores DE ALTA calidad DE LA SON comunes como pantallas de equipos y se ven mejor cuando se impulsan en sus resoluciones nativas (normalmente 1280 1024, 1600 1200, y así sucesivamente). Los clientes que tienen dificultades para leer texto y ver imágenes con esta resolución a menudo establecen los escritorios de sus equipos en una resolución más baja y sufren artefactos visuales del escalado de PPP. En su lugar, los clientes pueden dejar la resolución en el tamaño nativo y cambiar el valor de PPP de la pantalla Windows, lo que hace que la apariencia del elemento y el texto sea mayor sin sacrificar la calidad de la imagen.

Aunque esta característica ha estado disponible de algún modo desde Windows XP, rara vez lo habilitan los clientes o los OEM. Más de la mitad de todas las pantallas de equipo actuales están establecidas en una resolución inferior a la resolución nativa del monitor, en función de los comentarios de los clientes. Windows 7 hace que esta característica sea mucho más visible para los clientes durante la configuración inicial y al cambiar la configuración de pantalla, lo que les anima a usar el escalado de PPP en lugar de cambiar la resolución del escritorio.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

En su lugar, se puede usar la función [**SetProcessDPIAware,**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) si se llama al principio del código de inicio del proceso. Se prefiere agregar al manifiesto para asegurarse de que no hay condiciones de carrera con elementos de software (como archivos DLL) que se puedan inicializar antes de llamar al punto de entrada principal. Tenga en **cuenta que SetProcessDPIAware** solo está presente en Windows Vista y Windows 7.

Agregar el elemento manifest es fácil de hacer con Visual Studio 2005 y 2008; cree un archivo denominado dpiaware.manifest que contenga el texto siguiente:

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

A continuación, Visual Studio, agregue pppware.manifest al proyecto. Asegúrese de **que Insertar manifiesto** está establecido en Sí **en** las propiedades del proyecto. Tenga en cuenta que las versiones anteriores de la herramienta manifiesto (Mt.exe) generarán una advertencia falso con los elementos de manifiesto compatibles con PPP. Para resolver este problema, actualice Mt.exe a la versión más reciente desde el SDK de Windows.

Visual Studio 2010 incluye una configuración en las propiedades del proyecto, denominada Habilitar reconocimiento de **PPP,** que elimina la necesidad de un archivo como pppaware.manifest. Para **buscar Habilitar reconocimiento de PPP,** expanda **Propiedades** de configuración y Herramienta **manifiesto** y, a continuación, seleccione Entrada **& salida**.

En Windows, el modo de presentación tradicional tiene como valor predeterminado 96 PPP, que era común para los monitores de CRT.

Aunque las aplicaciones de pantalla completa cambian la resolución de pantalla, a menudo usan métricas y mensajes de ventana al configurar búferes y mostrar rectángulos. La virtualización de PPP hace que estos modos de presentación a pantalla completa aparezcan recortados y declarar la compatibilidad con PPP evitará estos problemas. Para obtener más información, vea [Escribir DPI-Aware aplicaciones Win32](../hidpi/high-dpi-desktop-application-development-on-windows.md).

</dd> </dl>

## <a name="security-and-compatibility"></a>Seguridad y compatibilidad

**Resumen de los requisitos de seguridad y compatibilidad**

**Ventajas del cliente**

Los siguientes requisitos mejoran la seguridad general de los juegos y ayudan a garantizar que funcionan con Windows en arquitecturas diferentes, en configuraciones diferentes y en modos diferentes.

### <a name="21-follow-user-account-control-guidelines"></a>2.1 Seguir las directrices de control de cuentas de usuario

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Todos los archivos ejecutables (es decir, todos los archivos que tienen una extensión .exe) deben contener un manifiesto incrustado que defina su nivel de ejecución mediante la inclusión de la etiqueta siguiente:

``` syntax
            <requestedExecutionLevel>
```

Según el requisito 1.2, el juego principal y el ejecutable de ejecución automática deben tener el nivel de ejecución de asInvoker para admitir contextos de usuario estándar.

Los archivos de datos de usuario que tienen asociaciones de archivo registradas con **Explorador de archivos** deben colocarse en una subcarpeta de la carpeta especificada por CSIDL PERSONAL (también denominada \_ **Documentos** **o Mis documentos**). Todos los demás archivos de datos de usuario deben almacenarse en una subcarpeta de las carpetas especificadas por CSIDL \_ LOCAL \_ APPDATA o CSIDL \_ COMMON \_ APPDATA. (Estos directorios están ocultos de forma predeterminada para usuarios individuales y para todos los usuarios).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

La experiencia de Windows usuario es más segura si las aplicaciones se ejecutan solo con los permisos necesarios.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Si solo algunas características de una aplicación requieren privilegios administrativos (por ejemplo, una aplicación que necesita configurar un firewall), el proceso principal de la aplicación todavía debe ejecutarse con privilegios de usuario estándar. Las características que requieren privilegios administrativos deben moverse a un proceso independiente, como un instalador o una utilidad de configuración.

Si no se requieren privilegios administrativos, el XML del manifiesto incrustado debe incluir lo siguiente:

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

Si se requieren privilegios administrativos, el XML del manifiesto incrustado debe incluir lo siguiente:

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

Con Visual Studio 2005, esto se inserta fácilmente simplemente agregando un archivo de manifiesto (.manifest) que contiene uno de los bloques anteriores al proyecto y asegurándose de que **Insertar** manifiesto está establecido en **Sí** en las propiedades del proyecto para la herramienta Manifiesto. Para Visual Studio 2008 y 2010, las propiedades de UAC se pueden establecer directamente en las propiedades del proyecto para el vinculador en la página **Archivo de** manifiesto. Tenga en cuenta que las versiones anteriores de la herramienta manifiesto (Mt.exe) generan una advertencia falso con los elementos de manifiesto de UAC. Para resolver este problema, actualice Mt.exe a la versión más reciente desde el SDK Windows.

Consulte el requisito 3.1 para obtener más información sobre los casos especiales de instalación, aplicación de revisiones y eliminación.

Las bibliotecas de vínculos dinámicos (DLL) no requieren estos manifiestos.

Para obtener más información sobre el control de cuentas de usuario, vea [Control de cuentas de usuario para desarrolladores de juegos.](/windows/desktop/DxTechArts/user-account-control-for-game-developers)

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>2.2 Compatibilidad Windows versiones x64

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Para mantener la compatibilidad con las ediciones de 64 bits de Windows, los juegos deben cumplir los siguientes requisitos.

-   Los títulos y los instaladores de títulos no deben contener ningún código de 16 bits ni depender de ningún componente de 16 bits.
-   Si el juego depende de los controladores en modo kernel para el funcionamiento, las versiones x64 de estos controladores deben estar disponibles. La configuración del juego debe detectar e instalar los controladores y componentes adecuados para las ediciones de 64 bits de Windows.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Muchos Windows Vista y Windows 7 usuarios ejecutarán ediciones de 64 bits del sistema operativo a lo largo de la vida del producto, por lo que es fundamental que las aplicaciones sean compatibles con este sistema operativo.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Windows en Windows 64 (WOW64) permite que el código de 32 bits se ejecute en ediciones de 64 bits de Windows, por lo que no es necesario que la aplicación sea código nativo de 64 bits en ediciones de 64 bits de Windows. El código de 66 bits no se ejecuta en ediciones de 64 bits de Windows.

No es necesario mantener Windows xp Professional x64 Edition, pero se recomienda encarecidamente.

Para más información, consulte [Programación de 64 bits para desarrolladores de juegos.](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers)

</dd> </dl>

### <a name="23-sign-files"></a>2.3 Archivos de firma

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Todos los archivos de código ejecutable (normalmente, los archivos con la extensión .exe o .dll) deben estar firmados con un certificado Authenticode válido públicamente y deben tener una dirección URL de servidor de marca de tiempo válida para la firma de producción.

Si el juego usa Windows Installer, los archivos de paquete del instalador (.msi archivos) deben estar firmados.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Firmar un archivo ayuda a los usuarios a decidir si confiar en una aplicación y garantiza a los usuarios que los archivos no se han alterado. También permite que las aplicaciones se ejecuten correctamente en entornos bloqueados.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para más información, consulte [Authenticode Signing for Game Developers ( Firma de Authenticode para desarrolladores de juegos).](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

Si el juego usa Windows Installer, se recomienda habilitar la aplicación de revisiones UAC/LUA, mediante la inclusión de una tabla MsiPatchCertificate. Para obtener más información, consulte Aplicación de revisiones de Control de cuentas [de usuario (UAC).](/windows/desktop/Msi/user-account-control--uac--patching)

No se recomienda firmar archivos de gabinete (.cab), a menos que sean relativamente pequeños (menos de 100 MB).

</dd> </dl>

### <a name="24-sign-drivers"></a>2.4 Controladores de firma

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Cualquier controlador en modo kernel instalado por el juego debe estar firmado con un certificado Authenticode válido públicamente.

Cualquier controlador de dispositivo de hardware en modo kernel instalado por el juego debe tener una firma de Microsoft, que se puede obtener de Windows Hardware Quality Labs (WHQL) o del programa Driver Reliability Signature (DRS).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Los controladores de malware o mal escritos pueden afectar gravemente a la estabilidad y seguridad de un sistema. En las ediciones de 64 bits de Windows Vista y Windows 7, los controladores sin signo no se cargan. Esta directiva también se puede habilitar para las ediciones de 32 bits de Windows Vista y Windows 7.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Se necesitan versiones nativas de 32 y 64 bits de todos los controladores en modo kernel según el requisito 2.2.

Puede encontrar más información sobre los programas de firma de controladores de Microsoft en el [portal Windows Hardware Developer .](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx)

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2.5 Realizar la comprobación de versiones correcta

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Los juegos no deben dejar de ejecutarse en sistemas operativos futuros como se indica en los cambios en el número de versión de Windows, a menos que el Contrato de licencia del usuario final prohíba el uso en sistemas operativos futuros. Si se supone que se debe producir un error en el juego, debe hacerlo correctamente mostrando un mensaje adecuado al usuario.

Si Windows se realizan comprobaciones de versión, las API de comprobación de versiones [**(GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) o [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) deben usarse para comprobar la versión del sistema operativo. Las claves del Registro no se deben leer para determinar la versión.

Las comprobaciones de versión explícitas para el tiempo de ejecución de DirectX no deben estar presentes en el juego. Estas comprobaciones de versión no deben estar presentes en la instalación que inicia la instalación en tiempo de ejecución de DirectX (DirectSetup).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Cuando Windows los usuarios actualicen sus sistemas operativos, no deben bloquearse para que no puedan jugar a los juegos actuales simplemente porque Windows número de versión ha aumentado. Los comprobación de versiones mal escritos siguen generando problemas de software que, de lo contrario, funciona bien en las versiones más recientes de Windows o simplemente con la adición de un service pack Windows.

La lógica de comparación de comprobación de versiones frágiles para el entorno de ejecución de DirectX ha creado numerosas instalaciones con errores cuando se ejecuta en diferentes versiones de Windows. El número de versión de DirectX solo se aplica a los componentes principales del sistema operativo. No se aplica a los componentes del SDK de DirectX en paralelo que usan muchos juegos.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Es bastante habitual ver que los instaladores comprueban una versión mínima del sistema operativo. Sin embargo, esta comprobación debe realizarse con cuidado para asegurarse de que comprueba si es mayor o igual que, en lugar de una igualdad simple, bloqueando así una versión específica del sistema operativo. El Application Verifier prueba **HighVersionLie** de Application Verifier es una manera rápida y fácil de determinar cómo reaccionará el instalador a un cambio significativo en el número de versión del sistema operativo.

El uso adecuado del paquete de redistribución en tiempo de ejecución de DirectX (instalación de DirectX) implica iniciarlo siempre durante la instalación, preferiblemente en modo silencioso. Esto permite que el código proporcionado por Microsoft realice las actualizaciones de versión necesarias. También permite la instalación de cualquier componente opcional del SDK de DirectX en paralelo, como D3DX, XACT, MDX o XInput.

Para obtener procedimientos recomendados para implementar el entorno de ejecución de DirectX, consulte [Instalación de DirectX para desarrolladores de juegos.](/windows/desktop/DxTechArts/directx-setup-for-game-developers)

Se recomienda que los juegos que admiten Windows XP comprueben un nivel de Service Pack de 2 o superior, ya que Service Pack 2 (SP2) y Service Pack 3 (SP3) proporcionan mejoras de seguridad significativas, un requisito simplificado de redistribución en tiempo de ejecución de DirectX e implementación muy amplia. La mayoría de las tecnologías modernas de Microsoft que admiten Windows XP requieren SP2 o SP3 (XAudio2, Games for Windows - LIVE, y así sucesivamente).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2.6 Compatibilidad con sesiones de usuario simultáneas

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Los juegos que se basan en gráficos 3D no son necesarios para funcionar a través de una conexión a Escritorio remoto, pero el usuario debe ser alertado cuando se produce un error en el juego.

Los juegos deben admitir Windows escenarios de multitarea siguiendo las reglas siguientes:

-   Los juegos no deben bloquear el uso de sesiones de usuario simultáneas.
-   Un juego debe ejecutarse en una nueva sesión de usuario cuando ya se está ejecutando en otra sesión.
-   No se debe escuchar el sonido del juego en una sesión de usuario cuando otro usuario está activo en una sesión diferente.
-   Los juegos deben admitir la conmutación rápida de usuarios.
-   Los juegos no deben intentar deshabilitar el cambio de tarea estándar. Los juegos no deben deshabilitar el método abreviado de teclado ALT+TAB. Los juegos pueden deshabilitar los métodos abreviados de teclado de accesibilidad, como se describe [en Deshabilitar teclas de método abreviado en juegos.](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games)

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Windows usuarios deben poder ejecutar sesiones simultáneas sin conflictos ni interrupciones. Se trata de un escenario común para un Windows compartido por una familia, familiares u otros.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para probar si el juego se inicia en una sesión remota, llame a [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ REMOTESESSION). Un valor distinto de cero indica que la sesión es remota.

Para obtener más información, vea [Fast User Switching](/windows-hardware/drivers/display/fast-user-switching). Tenga en cuenta que la conmutación rápida de usuarios se produce si las restricciones de tiempo de los controles parentales están habilitadas cuando el tiempo del usuario está en espera. Consulte el requisito 1.2 para obtener más detalles.

</dd> </dl>

### <a name="27-support-long-names"></a>2.7 Compatibilidad con nombres largos

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Si un juego admite guardar archivos, debe ser capaz de guardar archivos que tengan nombres y rutas de acceso largos. El juego debe controlar correctamente los caracteres especiales del sistema de archivos, como \\ / : \* ? " < >, en los campos de entrada del usuario que se usan para crear rutas de acceso o nombres de archivo.

Los juegos deben funcionar correctamente cuando un usuario tiene un nombre de usuario largo.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Los reproductores están acostumbrados a usar nombres largos en rutas de acceso profundas compatibles con el sistema operativo subyacente.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Los nombres largos se definen como aquellos que contienen los valores máximos definidos en el SDK de Windows.

</dd> </dl>

## <a name="installation"></a>Instalación

**Resumen de los requisitos de seguridad y compatibilidad**

**Ventajas del cliente**

Los clientes pueden estar seguros de que las aplicaciones se instalarán en Windows sin degradar el sistema operativo u otras aplicaciones si las aplicaciones usan métodos oficiales de distribución de componentes del sistema. Una experiencia de instalación simplificada proporciona una experiencia más accesible y sin problemas para juegos.

### <a name="31-support-easy-installation"></a>3.1 Compatibilidad con una instalación sencilla

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Los juegos deben proporcionar una ruta de acceso simplificada en la interfaz de usuario de configuración mediante la implementación de lo siguiente:

-   Muestra un máximo de un aviso de CLUF.
-   La ruta de instalación predeterminada debe omitir todas las selecciones para la instalación (como las selecciones de componentes o carpetas de instalación), asumir las selecciones predeterminadas y, a continuación, ejecutar el juego o el iniciador tras una instalación correcta, sin avisos adicionales. Si lo desea, se puede proporcionar una opción de instalación personalizada para opciones de configuración avanzadas.
-   Instale los componentes necesarios del sistema operativo (como los entornos de ejecución de DirectX y Visual C) mediante los paquetes de redistribución de Microsoft correctos. La instalación debe realizarse en modo silencioso, sin preguntar y sin que las comprobaciones de versión del componente lo resguardan.
-   Proporcione la **eliminación a través de programas** y características **Panel de control** para la aplicación de juego y los archivos de trabajo generados. Se recomienda una opción para eliminar los archivos de datos creados por el usuario. El proceso de eliminación debe asegurarse de que se quitan todos los archivos instalados y de que se borran todas las configuraciones (por ejemplo, las entradas de la lista de excepciones del firewall y las claves del Registro). No se deben quitar los componentes redistribuidos del sistema operativo.
-   Si el juego requiere que se agregan excepciones al firewall de Windows, el proceso de configuración puede solicitar a los usuarios que informen de que este cambio es necesario. Este mensaje debe aparecer antes de que comience la instalación.

La instalación y eliminación pueden requerir derechos administrativos. La aplicación de revisiones puede requerir la solicitud de credenciales administrativas, en función de la frecuencia de actualización. El juego normal del juego no debe requerir derechos administrativos, según el requisito 2.1 Siga las instrucciones de control de cuentas de usuario.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

La instalación sencilla es una filosofía de desarrollo de juegos centrada en Windows que está diseñada para simplificar y simplificar el proceso a veces tedioso y confuso de instalar juegos en equipos que ejecutan Windows sistemas operativos. La instalación sencilla se habilita mediante un conjunto de tecnologías y procedimientos recomendados que reducen la complejidad innecesaria y el riesgo percibido de instalar juegos en Windows equipos.

Los objetivos clave son:

-   Reduzca la cantidad de tiempo para entrar en el juego y empezar a jugar.
-   Reduzca el número de cuadros de diálogo y opciones a muy pocos, o ninguno, para simplificar la experiencia de instalación del juego.

Algunas instalaciones tradicionales tienen avisos que permiten instalaciones no funcionales, aunque parezca que la aplicación se ha instalado correctamente. Por ejemplo, un juego puede requerir que un usuario acepte un CLUF. A continuación, se instala el juego y, a continuación, aparece el CLUF de DirectX. Este CLUF permite a los usuarios rechazar y, por tanto, omitir la instalación del entorno de ejecución de DirectX. Este escenario puede dar lugar a un juego que no se puede ejecutar debido a la falta de componentes.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para más información sobre la instalación de juegos, las técnicas de instalación de juegos no tradicionales, las soluciones de aplicación de revisiones compatibles con UAC y el control de revisiones frecuentes, consulte los siguientes artículos de DirectX:

-   [Simplificar la instalación de juegos](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [Instalación a petición de juegos](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [Aplicación de revisiones a Game Software Windows XP, Windows Vista y Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Procedimientos recomendados de instalación para juegos en línea multijugador masivos](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> La eliminación de archivos de datos generados específicos del usuario debe realizarse solo para el usuario actual y para las ubicaciones de usuario compartidas comunes. No hay ninguna manera sólida de examinar el sistema para quitar archivos específicos del usuario para otros usuarios, incluso si la eliminación requiere credenciales administrativas.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3.2 Compatibilidad con el control de cuentas de usuario para la instalación

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

El instalador del juego no debe asumir que se ejecuta en el mismo contexto que el usuario. Las ubicaciones específicas del usuario serán diferentes del instalador y del reproductor, incluso para los sistemas de usuario único debido a la elevación de credenciales de administrador. Por lo tanto, cuando un juego se ejecuta por primera vez, debe realizar tareas específicas del usuario, independientemente del proceso de instalación.

El Windows de excepción del firewall no debe aparecer cuando un usuario hospeda o se une a un juego multijugador. Cualquier configuración necesaria debe realizarse en el momento de la instalación. Las instrucciones de instalación deben informar al usuario de que esta operación se producirá como parte de la instalación.

El instalador del juego debe proporcionar un manifiesto insertado que designe el nivel de ejecución necesario, según el requisito 2.1, Seguir las instrucciones de control de cuentas de usuario.

Si el instalador inicia el juego una vez completada la instalación, debe iniciarse en el contexto del usuario original.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Uno de los cambios más grandes en el sistema operativo Windows en Windows Vista es la adición del Control de cuentas de usuario (UAC), que ejecuta aplicaciones con privilegios reducidos de forma predeterminada. Como resultado, los instaladores deben administrar los niveles de privilegios en consecuencia. Windows 7 también hace un uso amplio de UAC. Aunque Windows 7 mejora la experiencia del usuario de UAC, los instaladores deben cumplir los mismos requisitos que en Windows Vista para funcionar correctamente, sin depender de un comportamiento de virtualización potencialmente confuso.

UAC está activo de forma predeterminada en Windows Vista y Windows 7, y la gran mayoría de los clientes (88 % o más, en función de los comentarios) dejan esta característica habilitada.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para obtener más información sobre cómo configurar Windows Firewall, consulte el artículo de DirectX [Windows Firewall para](/windows/desktop/DxTechArts/games-and-firewalls) desarrolladores de juegos y el ejemplo FirewallInstallHelper.

El lanzamiento estándar del juego al final del proceso de instalación no cumple el último aspecto de este requisito si un usuario estándar inicia la instalación y si el proceso de instalación requiere privilegios administrativos (es decir, solicita las credenciales de administrador). También hereda privilegios administrativos, lo que es un riesgo de seguridad potencial. En su lugar, un cargador de arranque de configuración debe iniciar el juego después de volver de una invocación correcta del instalador. Para obtener más información, vea el artículo de MSDN Magazine [Teach Your Apps to Play Nicely with Windows Vista User Account Control](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3.3 Instalar en carpetas correctas

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Los juegos que están instalados para todos los usuarios deben instalarse en la carpeta Archivos de programa de forma predeterminada. Los datos de usuario se deben escribir cuando el juego se ejecuta por primera vez, no durante la instalación.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Los usuarios deben tener la flexibilidad de instalar aplicaciones donde las necesiten. También deben tener una experiencia coherente y segura con la ubicación predeterminada de los archivos.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Los juegos pueden hacer uso de las distintas ubicaciones de carpeta conocidas (como las especificadas por CSIDL LOCAL APPDATA y \_ \_ CSIDL \_ COMMON APPDATA) para almacenar grandes cantidades de datos de juegos y archivos ejecutables compatibles para implementar escenarios avanzados de instalación a petición y aplicación de \_ revisiones.

Dado que la instalación puede requerir elevación a una cuenta de usuario diferente durante el proceso de instalación de todos los usuarios, no hay ninguna ubicación de usuario correcta en la que almacenar los datos en el momento de la instalación. Además, si el cifrado de archivos está habilitado, solo la cuenta de usuario que los creó puede acceder a los archivos cifrados.

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3.4 Instalación Windows recursos correctamente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Las aplicaciones no deben intentar instalar archivos o claves del Registro protegidos por Windows Resource Protection (WRP). Si la aplicación requiere versiones más recientes de los componentes del sistema, debe actualizar estos componentes mediante un Microsoft Service Pack o un paquete de instalación aprobado por Microsoft que contenga el componente del sistema. Los componentes del sistema nunca se deben volver a empaquetar.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Windows La protección de recursos (WRP) está diseñada para garantizar que los recursos del sistema protegidos solo se actualizan mediante mecanismos de instalación o actualización aprobados por Microsoft. WRP mejora la confiabilidad del sistema al garantizar que los resultados de una instalación son predecibles.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

WRP es el sucesor de Windows File Protection, que protege la mayoría de los componentes del sistema que están instalados en la carpeta Windows archivos. WRP protege la mayoría de las claves del Registro que almacenan la configuración para la creación de objetos COM. También reserva determinadas carpetas para que las use exclusivamente el sistema operativo. Los intentos de acceso a los recursos protegidos suelen producir un error de denegación de acceso.

Para más información sobre los procedimientos recomendados cuando el entorno de ejecución de DirectX se implementa con un juego, consulte el artículo de DirectX Instalación de [DirectX para desarrolladores de juegos.](/windows/desktop/DxTechArts/directx-setup-for-game-developers)

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3.5 Evitar reinicios durante la instalación

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

El instalador del juego no debe suponer que la instalación de componentes de Windows desde paquetes de redistribución requiere un reinicio, a menos que el reinicio se indique mediante un resultado devuelto o por la documentación de Microsoft.

Si el instalador del juego siempre fuerza un reinicio, Microsoft debe aprobarlo.

Los cuadros de diálogo Archivos en uso que se incluyen en los paquetes del instalador de Windows deben contener una opción para cerrar automáticamente las aplicaciones e intentar reiniciarlas una vez completada la instalación.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Reiniciar el sistema después de una instalación es una interrupción inconveniente para los usuarios y normalmente no es necesario.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para obtener más información, vea [Using Windows Installer with Restart Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager).

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3.6 Usar el control de versiones de archivos correctamente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

El programa de instalación del juego debe comprobar correctamente para asegurarse de que están instaladas las versiones de archivo más recientes. La instalación de un juego nunca debe volver a los archivos que no se producen o que comparten las aplicaciones que no se producen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Los componentes compartidos y los componentes del sistema a menudo se actualizan para correcciones de seguridad y funcionalidad ampliada. Una instalación que incluya una versión anterior de los componentes actualizados no debería dar lugar a la pérdida de actualizaciones y correcciones que ya se han aplicado.

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3.7 Compatibilidad con el requisito condicional de ejecución \[ automática\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

En el caso de los juegos distribuidos en CD, DVD u otros medios extraíbles que admiten La ejecución automática, cuando el disco se inserta por primera vez, la aplicación debe ejecutar automáticamente o pedir al usuario que instale el juego, a menos que el usuario haya deshabilitado la característica Ejecución automática.

Una vez que la aplicación se haya instalado correctamente, volver a insertar el disco en la unidad no debe hacer que la instalación se vuelva a iniciar automáticamente. Es aceptable preguntar a los usuarios si quieren actualizar o cambiar sus opciones de instalación.

La aplicación de ejecución automática no debe solicitar elevación (es decir, debe tener asInvoker en el manifiesto, según el requisito 2.1, aunque puede iniciar el programa de instalación u otra utilidad que requiera derechos administrativos. La elevación solo debe producirse si el juego no está instalado o si el usuario lo selecciona específicamente.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

La ejecución automática simplifica la experiencia de uso de aplicaciones distribuidas por medios, como juegos que normalmente requieren que el disco esté presente en la unidad para poder jugar al juego.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

No es aceptable exigir al usuario que vaya a Explorador de archivos para iniciar la instalación desde el CD o DVD.

En el caso de los juegos que se distribuyen en varios discos, lo ideal es que los discos posteriores usen la característica Ejecución automática o continúen con la instalación sin pedir al usuario que presione una tecla o que haga otra acción.

Al crear un programa de ejecución automática, asegúrese de que todos los componentes necesarios están presentes en las nuevas instalaciones de Windows. Las aplicaciones típicas se basan en tecnologías instaladas por la instalación, pero la ejecución automática se ejecuta antes de que se produzca dicha instalación. Un ejemplo común es el error de los programas de ejecución automática porque los archivos DLL del entorno de ejecución de Visual C no se incluyeron como parte de la Windows configuración. Por lo tanto, el programa Autorun debe usar la implementación de CRT local de la aplicación o debe vincular estáticamente CRT.

Los programas de ejecución automática escritos para su uso en versiones de Windows antes de Windows Vista no deben usar el entorno de ejecución de .NET porque esta tecnología no se incluye con Windows XP o versiones anteriores de Windows. Windows Server 2003 y Windows Vista son las primeras versiones de Windows que incluyen el entorno de ejecución de .NET como parte de su sistema operativo.

Por motivos similares, los programas de ejecución automática no pueden requerir la presencia de componentes opcionales en paralelo del SDK de DirectX, como D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, XACT, XINPUT y MDX 1.1.

Para obtener un ejemplo del uso de Autorun, consulte AutoRun Sample (Ejemplo de ejecución automática).

</dd> </dl>

## <a name="reliability"></a>Confiabilidad

**Resumen de los requisitos de seguridad y compatibilidad**

**Ventajas del cliente**

Estos requisitos hacen que una aplicación sea más confiable al minimizar el número de bloqueos, bloqueos y reinicios. Los requisitos de confiabilidad pueden ayudar a garantizar que el software sea más predecible, fácil de mantener, resistente y recuperable.

### <a name="41-eliminate-unnecessary-reboots"></a>4.1 Eliminar reinicios innecesarios

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Todos los instaladores de aplicaciones deben aprovechar las API del administrador de reinicio para evitar reinicios del sistema (consulte el requisito 3.5).

Los juegos no deben bloquear el apagado.

Todas las aplicaciones deben responder al administrador de reinicio escuchando y respondiendo a los siguientes mensajes de apagado:

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ QUERYENDSESSION con LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Las aplicaciones guia deben responder (TRUE) inmediatamente como preparación para un reinicio.

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ ENDSESSION con LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Las aplicaciones deben devolver un valor 0 en 5 segundos y, a continuación, cerrar.

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL+C 
</dt> <dd>

Las aplicaciones de consola que reciben este mensaje deben cerrarse inmediatamente.

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Los reinicios del sistema son una interrupción importante. Conduce a una mala experiencia del usuario y debe minimizarse. Algunas operaciones, como las actualizaciones críticas del sistema, pueden requerir reinicios. Al escuchar los mensajes de apagado, el juego y otras aplicaciones pueden reaccionar rápidamente a las solicitudes del administrador de reinicio. De esta manera, pueden evitar retrasos innecesarios en solicitudes de reinicio válidas.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Si un instalador de juegos usa la tecnología Windows Installer (MSI) sin ninguna acción personalizada, esta funcionalidad se proporciona automáticamente. Los paquetes de redistribución de Microsoft también admiten el Administrador de reinicio.

Para obtener más información sobre el Administrador de reinicio, vea el artículo de MSDN [Acerca del Administrador de reinicio.](/windows/desktop/RstMgr/about-restart-manager)

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4.2 Eliminar Application Verifier errores

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

El juego no debe generar errores en ejecución en Microsoft Application Verifier (AppVerifier), versión 4.0 o posterior, en las siguientes pruebas:

-   Aspectos básicos: identificadores, montones, bloqueos, memoria, TLS
-   Varios: DangerousAPIs, DirtyStacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

AppVerifier comprueba muchos problemas conocidos que provocan bloqueos y bloqueos en Windows aplicaciones, así como vulnerabilidades de seguridad conocidas.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Para obtener más información sobre Application Verifier, vea [Application Verifier](/previous-versions/ms220948(v=vs.80)) y Uso de Application Verifier dentro del ciclo de vida de desarrollo [de software](/previous-versions/aa480483(v=msdn.10)) en MSDN. Puede descargar el Application Verifier desde [Detalles de descarga: Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) en el Centro de descarga de Microsoft.

Este requisito no se aplica a las aplicaciones administradas puras sin interoperabilidad nativa.

Estas pruebas deben ejecutarse en una compilación de versión. Las compilaciones de depuración pueden generar errores falsos. Algunas tecnologías antisecuencia y antisecuencia pueden interferir con la ejecución de AppVerifier. Por lo tanto, estas pruebas deben realizarse sin tecnologías antiseñería y anti-cheat habilitadas.

Puede que sea necesario establecer la propiedad Full de la prueba Basics:Heaps en FALSE, ya que el PageHeap completo aumenta considerablemente la presión de memoria de la aplicación en ejecución. Se seguirán detectando errores, pero pueden ser más difíciles de rastrear si solo se usa PageHeap parcial.

Si usa las pruebas relacionadas con UAC/LUA en Application Verifier para cumplir los requisitos de control de cuentas [](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) de usuario 2.1 y 3.2, debe usar el Analizador de usuarios estándar para revisar los resultados. También hay muchas otras pruebas útiles proporcionadas por Application Verifier que se recomienda encarecidamente usar en el desarrollo y las pruebas para garantizar un alto nivel de compatibilidad con las versiones actuales y futuras de Windows. La **prueba HighVersionLie** se usa para comprobar el cumplimiento del requisito 2.5.

Visual Studio Team System incluye un subconjunto de la funcionalidad AppVerifier que se integra en el entorno de depuración. Esto puede resultar útil para realizar un seguimiento y resolver problemas con los aspectos básicos: montones, identificadores y pruebas de bloqueo.

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4.3 Compatibilidad con Informe de errores de Windows información de versión de archivo

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Para habilitar la compatibilidad con Informe de errores de Windows, los juegos deben cumplir los siguientes requisitos:

-   Los juegos solo deben controlar las excepciones conocidas y esperadas. Informe de errores de Windows debe deshabilitarse. Si aparece un error como una infracción de acceso en un juego, debe permitir que Informe de errores de Windows informe del bloqueo.
-   Todos los archivos ejecutables (por ejemplo, archivos .exe archivos DLL) deben contener un nombre de producto, un nombre de empresa y una versión de archivo precisos.
-   La salida normal del juego no debe dar lugar a un error de excepción desconocido.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Las API Informe de errores de Windows proporcionan comentarios fundamentales a Microsoft para detectar bloqueos y bloqueos generalizados en las aplicaciones. Esto permite que Microsoft y sus asociados detecten y resuelvan rápidamente los problemas del sistema y del controlador que conducen a errores de la aplicación rápidamente.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Los juegos pueden incluir controladores de excepciones no controladas personalizados para realizar la compatibilidad personalizada y la funcionalidad de informes, pero deben pasar cualquier error a las funciones **ReportFault** o **WerReportSubmit.**

Puede comprobar la información adecuada de la versión del archivo consultando las propiedades del archivo en la interfaz de usuario de Windows escritorio y comprobando la página de propiedades Versión.

Para obtener más información sobre Informe de errores de Windows API y cómo analizar los volcados de memoria que se generan al usar este servicio, vea el artículo de DirectX Análisis de volcado de [memoria](/windows/desktop/DxTechArts/crash-dump-analysis).

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>Xbox 360 Common Controller for Windows Terminology



| Nombre                                          | Descripción                                                                                                 |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| Un                                        | Botón A.                                                                                     |
| B                                        | Botón B.                                                                                     |
| ATRÁS                                     | El botón Atrás.                                                                                  |
| (derecha/izquierda) topes                      | Botón situado en el borde superior derecho e izquierdo del controlador. Equivalente a un botón de botón de botones.    |
| panel direccional                          | Panel direccional del controlador.                                                                   |
| Panel D                                    | Abreviatura aceptada del panel direccional.                                                         |
| DP                                       | Abreviatura del panel direccional y etiqueta del controlador.                                                |
| RB, LB                                   | Abreviaturas de los topes derecho e izquierdo y etiquetas del controlador.                                        |
| RS, LS                                   | Abreviaturas de stick derecha e izquierda y etiquetas de controlador.                                         |
| RT, LT                                   | Abreviaturas de desencadenador derecha e izquierda y etiquetas de controlador.                                       |
| RSB, LSB                                 | Abreviaturas de stick derecha e izquierda y etiquetas de controlador.                                         |
| START                                    | El botón Inicio.                                                                                 |
| (derecha/izquierda) stick                       | El stick del controlador. Anteriormente, la chincheta.                                                       |
| Botón de stick (derecha/izquierda)                | Botón de stick del controlador. Anteriormente, el botón de la chincheta.                                         |
| Desencadenador (derecha/izquierda)                     | Desencadenador del controlador.                                                                          |
| Vibración                                | Comentarios sobre el juego generados por el motor del controlador. No use el alabado.                           |
| X                                        | Botón X.                                                                                     |
| Y                                        | Botón Y.                                                                                     |
| Mando Xbox 360 para Windows          | El controlador Xbox 360 se vende como SKU de hardware de PC, incluido un disco Windows controlador de dispositivo.          |
| Mando inalámbrico Xbox 360 para Windows | El Xbox 360 de juegos inalámbrico se vende como una SKU de hardware de PC, incluido un disco Windows controlador de dispositivo. |



 

## <a name="guidelines-for-game-middleware-products"></a>Directrices para productos de middleware de juegos

### <a name="introduction"></a>Introducción

Para que los juegos cumplan los requisitos para Windows programa, deben cumplir una lista de requisitos técnicos. Los componentes de terceros que se incluyen con un título (archivos ejecutables, archivos DLL, controladores, etc.) también deben cumplir estos requisitos para que el juego pueda calificar. En este documento se resaltan los requisitos más comunes que también deben cumplir los componentes de terceros para que el juego pase las pruebas de cumplimiento. Los instaladores y los paquetes de producción completos del motor de juegos deben revisar el documento completo de requisitos técnicos de Games for Windows, ya que muchos de estos requisitos se ven afectados por estas herramientas.

### <a name="additional-recommendations"></a>Recomendaciones adicionales

Además de asegurarse de que el componente admite la creación de títulos que cumplen los requisitos de Juegos para Windows, hay una serie de consideraciones que debe tener en cuenta al diseñar e implementar una biblioteca o utilidad de soporte técnico para un juego de Windows.

-   Para admitir a los desarrolladores que trabajan en aplicaciones x64 nativas de 64 bits, proporcione versiones nativas de 32 y 64 bits de las bibliotecas. La versión de 32 bits debe ser compatible con 64 bits por 2.2. Las bibliotecas para aplicaciones de 32 bits no deben suponer que el bit alto de cualquier dirección de 32 bits no se usa para admitir el uso en aplicaciones LARGEADDRESSAWARE x86.
-   Si proporciona encabezados de código nativo (C/C++), use la sintaxis de atributos del Lenguaje de anotación estándar (SAL) para decorar las rutinas de API públicas. Esto permitirá a los usuarios de la biblioteca obtener la máxima ventaja de usar Static Code Analysis (/analyze), que forma parte de Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium y Visual Studio 2010 Ultimate, así como las herramientas del compilador del SDK de Windows disponibles públicamente.
-   Si el producto crea subprocesos dentro del proceso del usuario, asegúrese de nombrar cada subproceso para que las herramientas de depuración puedan anotar correctamente los subprocesos en ejecución.
-   Si escribe rutinas que están diseñadas para llamarse dentro del bucle principal de un juego, use las rutinas D3DPERF \_ BeginEvent/EndEvent y D3DPERF SetMarker para anotar operaciones de alto nivel para facilitar la identificación de cuellos de botella mediante LAN para \_ Windows.
    > [!Note]  
    > Para la Visual Studio de diagnóstico de gráficos de 2012, estas rutinas D3DX y HISTOGRAM se reemplazan por la interfaz [**ID3DUserDefinedAnnotation.**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)

     

-   En el caso de las bibliotecas de redes, proporcione implementaciones neutras de IP y evite rutinas IPv4 en desuso para admitir las tecnologías IPv6 y Teredo en Windows XP con Service Pack 2, Windows Vista y Windows 7.
-   Los proveedores de servicios de juegos deben registrarse en Games Explorer mediante la versión 2 del esquema de GDF y usar la característica RSS para proporcionar noticias relacionadas con el servicio.

### <a name="games-for-windows-showcases"></a>Juegos para Windows presentación

### <a name="introduction"></a>Introducción

Juegos para Windows presentaciones van más allá de proporcionar una experiencia de juego sólida en Windows equipos. Al implementar estas características, los juegos pueden agregar más emociones a la experiencia del usuario en las plataformas de Windows más recientes.

Los juegos Windows títulos deben cumplir todos los requisitos técnicos enumerados en este artículo, pero presentar características son opcionales. Estos títulos son gratuitos para implementar algunos, ninguno o todos estos escaparates.

### <a name="s1-exploit-direct3d-11"></a>S.1 Exploit Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Direct3D 11 es la API de representación de próxima generación para Windows Vista y Windows 7. Los juegos que aprovechan Direct3D 11 usan contenido optimizado, técnicas de representación avanzadas y nuevas características de hardware para crear una experiencia atractiva en hardware compatible con 10, 10.1 y 11.

Si el juego también implementa Direct3D 9, una comparación en paralelo debe mostrar una mejora perceptible en la calidad del contenido, la fidelidad visual, el rendimiento, la complejidad de la escena y otras áreas de fidelidad de gráficos para Direct3D 11. Esta compatibilidad está sujeta al requisito técnico 1.7 Windows Games for Windows.

La tecnología Direct3D 10level9 se puede usar para admitir el hardware de vídeo de clase 9 de Direct3D 2.0/3.0 de Shader Model 2.0/3.0 en Windows Vista y Windows 7, en lugar de usar una implementación de Direct3D 9 en paralelo para una amplia compatibilidad con hardware. Sin embargo, esto no es suficiente para mostrar esta presentación.

En los equipos Windows Vista o Windows 7 con Direct3D 11 instalado, el juego debe usar Direct3D 11 de forma predeterminada.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

La API de Direct3D 11 se basa en la infraestructura Windows Display Driver Model (WDDM) y Direct3D 10.1 para admitir nuevas funcionalidades: teselación de hardware, sombreadores de proceso, representación multiproceso y creación de recursos, nuevos formatos de compresión de textura y un lenguaje de sombreador más flexible. Direct3D 11 proporciona compatibilidad unificada con hardware para tarjetas de vídeo modernas, incluidas las últimas partes de Direct3D 11, todas las tarjetas de vídeo Direct3D 10 y 10.1, y muchas tarjetas de vídeo de Direct3D 9 del modelo de sombreador 2.0/3.0, que es el hardware de vídeo mínimo necesario para el escritorio de Aero 3D.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Migrar un motor de representación de Direct3D 9 para usar la nueva interfaz de Direct3D 11 es una tarea bien definida:

-   Elimine todas las operaciones de función fija en favor de sombreadores programables.
-   Actualice todos los sombreadores existentes a la nueva sintaxis de Shader Model 4.x/5.
-   Actualice la administración de recursos para admitir el nuevo modelo de vista.
-   Convierta todos los recursos para usar una nueva lista de formatos disponibles.
-   Actualice el control de estado de representación para usar bloques de estado inmutables y vuelva a trabajar las constantes del sombreador en búferes constantes.

Esta conversión es esencial para habilitar la presentación de Direct3D 11, aunque el resultado no cumple el requisito de presentación de aprovechar la nueva API.

La nueva API y el modelo de programación HLSL asociado ofrecen muchas oportunidades para mejorar el contenido:

-   Aprovechar las características de hardware existentes de Direct3D 10, como El sombreador de geometría, Stream Out, matrices de texturas y los formatos de textura comprimidos BC4/BC5.
-   Aprovechamiento de las características de hardware existentes de Direct3D 10.1, como los modos de combinación independientes por representación y destino, la lectura de profundidad de MSAA, el acceso al sombreador por ejemplo de MSAA, las matrices de mapas de cubo y la representación en formatos comprimidos en bloques (BC).
-   Implementación de algoritmos avanzados de GPU mediante el sombreador de proceso con CS4.x en tarjetas de vídeo direct3D 10/10.1 existentes (habilitadas por controladores de vídeo actualizados) o CS 5.0 en tarjetas de vídeo direct3D 11 de próxima generación.
-   Representación en varios subprocesos mediante la creación de recursos de subproceso libre y varios contextos de dispositivo para mejorar el rendimiento en sistemas de varios núcleos (con controladores de vídeo actualizados). Para obtener más información, vea Games for Windows Showcase S.3.
-   El uso de nuevas características del hardware de vídeo de clase 11 de Direct3D, como la teselación de hardware con sombreadores de casco y dominio, el hardware de sombreador HLSL modelo 5.0 hlsl incluye formatos de textura comprimidos BC6HBC7 y vinculación dinámica del sombreador.

Las técnicas que se pueden implementar con Direct3D 9 (en gran medida a través de un alto costo de CPU) se pueden descargar en la GPU de una manera eficaz, lo que libera recursos de CPU para admitir otras demandas de juego.

Las API de Direct3D 11, las herramientas de soporte técnico y los ejemplos están disponibles en el SDK de DirectX. Consulte también API de gráficos en Windows.

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S.2 Exploit x64 Native

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

El juego incluye un ejecutable nativo de 64 bits que ofrece una nueva experiencia atractiva habilitada por las ediciones x64 de Windows que se ejecutan en hardware compatible con x64. Una comparación en paralelo con la versión de 32 bits del juego debe mostrar una mejora perceptible en la complejidad del contenido, tiempos de carga generales reducidos y rendimiento.

En las ediciones de 64 bits de Windows, la instalación siempre debe configurar la versión nativa de 64 bits del juego como valor predeterminado para los accesos directos en Games Explorer y Windows XP Professional x64 Edition. Si se desea una instalación dual, se puede especificar una tarea de reproducción adicional para Games Explorer en Windows Vista y Windows 7 que apunta a la versión de 32 bits, pero el valor predeterminado debe seguir siendo la versión nativa de 64 bits.

Tenga en cuenta que el juego debe admitir las ediciones de 64 bits de Windows Vista y Windows 7 para cumplir esta recomendación de presentación. Se recomienda Windows xp Professional x64 Edition, pero no es necesario.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

La tecnología x64 proporciona funcionalidades de direccionamiento de 64 bits para los mercados de consumidores y servidores que incluye compatibilidad con versiones anteriores de 32 bits de velocidad completa para las aplicaciones existentes. x64 es una parte clave de la hoja de ruta para AMD (AMD64) e Intel (EMT64) y, a excepción de las CPU ultra móviles, admite la tecnología para todos los procesadores de generación actuales y futuros.

Windows XP Professional x64 Edition fue el primer sistema operativo (SO) de Windows orientado al consumidor que admite la tecnología x64 y Windows Vista y Windows 7 expanden en gran manera la disponibilidad de la habilitación del sistema operativo para la informática de consumidor de 64 bits. Con 2 GB de RAM como estándar en muchos equipos nuevos, las mejoras adicionales en el escalado de memoria no beneficiarán a las aplicaciones individuales de 32 bits que no pueden abordar más de 2 GB de RAM física. En la actualidad, muchos juegos se enfrentan a desafíos que encajan todo el contenido disponible en las restricciones de 2 GB de espacio de direcciones virtuales, especialmente cuando se combinan con las memorias de vídeo grandes disponibles en GPU de gama alta, y el traslado a la tecnología x64 aumenta considerablemente los niveles de detalle compatibles.

La compatibilidad de x64 con juegos de 32 bits es un requisito técnico de Games for Windows (2.2), pero aprovechar al máximo las nuevas tecnologías requiere una implementación nativa de 64 bits.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

La principal ventaja del direccionamiento de 64 bits es la capacidad de acceder directamente a más de 2 GB de memoria física y virtual. El espacio de direcciones de memoria virtual grande permite un uso amplio de E/S asignadas a memoria sin preocuparse por los problemas de agotamiento del espacio de direcciones de máquina virtual que son frecuentes en la programación de 32 bits. Los juegos pueden aprovechar el nuevo espacio para mejorar en gran medida los tiempos de carga o, en algunos casos, eliminar las pausas para cargar contenido.

Las aplicaciones de 32 bits existentes pueden beneficiarse de las ediciones x64 al tener la capacidad de procesar direcciones con datos completos de 32 bits cuando se han creado con la opción del vinculador Habilitar direcciones grandes **(/LARGEADDRESSAWARE).** En las versiones de 32 bits de Windows XP, los modos de arranque especiales permitían a estas aplicaciones abordar hasta 3 GB de RAM, y las ediciones x64 proporcionan acceso a hasta 4 GB de RAM para aplicaciones compatibles con direcciones grandes (LAA). Aunque el uso de LAA en una aplicación de 32 bits no cumple este requisito de presentación, esta tecnología de puente es una manera muy útil de proporcionar ventajas de escalado adicionales en las versiones x64 de Windows para aquellos que no implementan completamente este requisito de presentación.

Para obtener más información, vea Programación de [64](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) bits para desarrolladores de juegos y [RAM, VRAM](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) y Más RAM: Juegos de 64 bits está aquí en Gamasutra.

> [!Note]  
> Un desafío clave para esta presentación es asegurarse de que las bibliotecas o componentes de terceros en los que se basa el juego están disponibles para el desarrollo nativo de 64 bits. Muchas API heredadas de Microsoft también se han eliminado del entorno nativo de 64 bits, lo que puede resultar un desafío para las bases de código del motor que contienen implementaciones anteriores de sistemas clave.

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>S.3 Exploit Many-Core Processors

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

El juego implementa características que aprovechan los procesadores de varios núcleos, escalando a 3, 4 o más núcleos, cuando están disponibles.

Si el juego admite sistemas de un solo procesador o de doble núcleo, una comparación en paralelo con un sistema de cuatro núcleos debe mostrar nuevas características perceptibles, efectos atractivos adicionales, mejoras en la calidad del contenido o un rendimiento mejorado.

Dado que el escalado de doble núcleo ya es ampliamente compatible con los juegos, así como el uso automático de varias mejoras de controladores de Direct3D, el escalado de doble núcleo no es suficiente para mostrar esta presentación.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

El crecimiento continuo del rendimiento de las CPU ha pasado de las mejoras de velocidad de reloj a la adición de núcleos computacionales. Las hojas de ruta de AMD e Intel se basan en diseños escalables y de varios núcleos. Todas las plataformas de juegos de próxima generación tienen CPU de varios núcleos debido a este cambio fundamental en la evolución de los procesadores. Las aplicaciones de un solo subproceso ya no verán mejoras significativas en las CPU de próxima generación. El multithreading simple tampoco se escalará a medida que el número de núcleos de CPU en uso común crezca a tres o más.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Tenga en cuenta que los recuentos de núcleos no necesitan ser una potencia de dos, por lo que los juegos deben escalarse linealmente y controlar los recuentos de núcleos de 3, 4, 5, 6, 7, 8, y así sucesivamente.

El escalado aumentando el número de subprocesos de una aplicación solo proporciona una devolución si el costo de la comunicación y la sincronización de subprocesos se mantienen en la comprobación. El escalado basado en características puede resultar una solución más sencilla a corto plazo, lo que permite que el juego funcione con normalidad sin los subprocesos adicionales en sistemas de un solo núcleo y habilitarlos cuando la potencia de CPU adicional esté disponible.

Para obtener más información, vea [Coding For Multiple Cores on Xbox 360 and Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) and [Lockless Programming Considerations for Xbox 360 and Microsoft Windows](/windows/desktop/DxTechArts/lockless-programming) en los artículos de DirectX, así como la utilidad DXUTLockFreePipe y el ejemplo CoreDetection.

El uso de los contextos de dispositivo y creación de recursos sin subprocesos de Direct3D 11 resulta útil para lograr la escalabilidad de muchos núcleos en la representación y carga de recursos gráficos. Consulte Games for Windows Showcase S.1.

Tenga en cuenta que el uso directo de la instrucción de CPU rdtsc, en lugar de usar las API de Windows para calcular el tiempo en sistemas de varios núcleos, puede provocar problemas en algunas configuraciones de hardware y sistema operativo. Consulte [Game Timing and Multicore Processors (Control de tiempo de](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) juego y procesadores de varios núcleos) en los artículos de DirectX.

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>S.4 Support Games for Windows - LIVE

Games for Windows - LIVE ya no es compatible con Microsoft.

### <a name="s5-support-windows-touch"></a>Compatibilidad con S.5 Windows Touch

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Windows juegos táctiles se pueden reproducir mediante gestos táctiles o en equipos que ejecutan Windows 7 con una pantalla táctil. También se puede usar la entrada de teclado, pero la interfaz de reproducción principal debe estar basada en la función táctil.

La habilitación de la función táctil no debe impedir el uso del mouse o del controlador común, sujeto al requisito técnico 1.4.

No se espera que el instalador del juego admita Windows touch.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Las pantallas compatibles con múltiples funciones táctiles para equipos están disponibles para equipos portátiles y escritorios, y representan una característica de hardware clave que se promueve con el lanzamiento de Windows 7. Windows 7 admite Windows Touch en todas las interfaces de escritorio y controles comunes.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Las aplicaciones de código nativo pueden tener acceso multitáctil a través de los mensajes WM TOUCH, en \_ combinación con la función [**RegisterTouchWindow.**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) Consulte también Manipulations and Inertia API (Manipulaciones e API de inercia).

Windows Presentation Foundation (WPF) 4.0 proporciona una solución administrada para interfaces multi-touch.

Para más información, consulte el sdk Windows Touch.

</dd> </dl>

### <a name="s6-support-high-color"></a>S.6 admite color alto

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Los juegos que admiten color alto usan un 10:10:10:2 (DXGI \_ FORMAT \_ R10G10B10A2, D3DFMT \_ A2B10G10R10) o un formato 16:16:16:16 (DXGI \_ FORMAT \_ R16G16B16A16, D3DFMT \_ A16B16G16R16) para el modo de presentación en búfer y pantalla completa.

Mediante el uso de un destino de representación de color alto, el contenido de rango de High-Dynamic (HDR) se puede representar con una gama extendida o amplia al realizar la asignación de tono a un intervalo de 10 o 16 bits.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Fundamento**
</dt> <dd>

Los monitores han sido capaces de mostrar más de 256 niveles de color por canal durante muchos años, incluso cuando las pantallas de CRT eran frecuentes. El hardware de detección en tarjetas de vídeo ha sido el factor limitador. Las GPU modernas, que incluyen la mayoría del hardware de 9 clases de Direct3D y todo direct3D de 10 clases y hardware mejor, tienen hardware de análisis capaz de al menos 10 bits por canal y la funcionalidad de hardware está configurada para crecer a 16 bits por canal de color en el futuro. Los sistemas de interconexión de HD TV (HDMI, DisplayPort) se han diseñado para controlar más de 8 bits por canal, y VGA análogo ya llevará dichas señales.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Información adicional**
</dt> <dd>

Tenga en cuenta que El color alto, o Hi Color, hace referencia históricamente al cambio de pantallas de color de 256 (8 bits) a pantallas de color de 15 o 16 bits. La mayoría de los sistemas de visualización han pasado desde hace mucho tiempo a Color verdadero, que es color de 24 bits o 8 bits por canal de color para rojo, verde y azul. Por color alto aquí nos refieremos a una nueva generación de sistemas de pantallas que pueden funcionar con más de 8 bits por canal de color individual. También se conoce como Color profundo.

</dd> </dl>

### <a name="recommended-best-practices"></a>Procedimientos recomendados

### <a name="introduction"></a>Introducción

Además de cumplir los requisitos técnicos y adoptar una o varias presentaciones en el título, hay una serie de procedimientos recomendados que se deben seguir para todos los Windows juegos. Aunque estas recomendaciones quedan fuera del ámbito de los requisitos técnicos básicos, se recomienda encarecidamente emplearlas para todos los juegos Windows títulos.

### <a name="additional-recommendations"></a>Recomendaciones adicionales

-   Use el compilador y el runtime Visual Studio más recientes. Las versiones más recientes del compilador implementan mejoras significativas para la calidad del código generado y para los problemas de seguridad, y emplean estrategias modernas de optimización del procesador. Actualizar el compilador y usar la versión más reciente de C Runtime es una manera fácil de migrar a prácticas de codificación modernas.
-   Use la versión de la biblioteca de vínculos dinámicos (DLL) del entorno de ejecución de C, en lugar de la vinculación estática, y use CRT seguro. (Se pueden realizar excepciones en casos especiales de preinstalación, como para un programa de ejecución automática o para el propio instalador).
-   Para el audio del juego, use XAudio2, X3DAudio o XACT, en lugar de Direct Sound. Para los motores de audio que hacen todas las mezclas y la conversión de velocidad de origen y solo necesitan una solución de baja latencia para la salida de audio, use Direct Sound en Windows XP (solo) y WASAPI en Windows Vista y Windows 7.
-   Evite el uso de API heredadas y en desuso: DirectDraw, Direct Sound, DirectPlay, la capa de rendimiento de DirectPlay, DirectPlay Voice y el modo retenido de Direct3D. Tenga en cuenta que DirectPlay Voice y Direct3D Retained Mode no están disponibles en Windows Vista o Windows 7. La capa de rendimiento de DirectPlay y DirectPlay no está disponible para las aplicaciones nativas x64.
-   Optimice mediante conjuntos de instrucciones SIMD de SSE/SSE2. Consulte [directXMath](/windows/desktop/dxmath/directxmath-portal) API en Windows SDK como una solución multiplataforma para operaciones matemáticas optimizadas para SIMD.
-   Use procedimientos recomendados modernos para la seguridad de Windows (incluidas las opciones del compilador y del vinculador, como **/NXCOMPAT,** **/GS,** **/SAFESEH,** **/DYNAMICBASE,** **/SDL,** y así sucesivamente). Para más información, consulte [Procedimientos recomendados de seguridad en el desarrollo de juegos.](/windows/desktop/DxTechArts/best-security-practices-in-game-development)
-   Use las bibliotecas y componentes Windows SDK más recientes. Quite las dependencias de los componentes heredados de DirectSetup implementados fuera de banda, como D3DX9, D3DX10 y D3DX11. Considere la [posibilidad de usar DirectXTex,](https://github.com/Microsoft/DirectXTex) [DirectXTK](https://github.com/Microsoft/DirectXTK) o ambos.
-   Evite usar el compilador HLSL anterior y, en su lugar, use el compilador HLSL moderno. Si la aplicación requiere compatibilidad con el sombreador de píxeles 1.x, use el ensamblado de sombreador en lugar de HLSL o limite el uso del compilador anterior a solo esos escenarios.

## <a name="resources"></a>Recursos



| Término                                                                                                                                                                                                                         | Descripción                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Juegos para Windows: casos de prueba <br/>                              | Procedimientos recomendados para juegos Windows XP, Windows Vista y Windows 7<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK <br/>                                                                                                      | [Windows Sdk](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Directrices de control de cuentas de usuario <br/>                      | [Windows Requisitos de desarrollo de aplicaciones de Vista para la compatibilidad con el control de cuentas de usuario](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Portal para desarrolladores <br/>                                                  | [Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>DirectX Portal para desarrolladores <br/>                                                  | [Centro para desarrolladores de Directx](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog de Games for Windows SDK y DirectX<br/> | [Juegos para Windows y el SDK de DirectX](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artículos adicionales de DirectX<br/>                                             | [Artículos técnicos de DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

