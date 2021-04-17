---
title: Explorador de juegos de Windows para desarrolladores de juegos
description: En este artículo se describe el proceso de registro de un juego con el explorador de juegos y controles parentales en Windows Vista y Windows 7 mediante el nuevo esquema GDF.
ms.assetid: 628f14bf-2714-0d68-8267-4f7f48c2774a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f59b90a23f407be3990a6a4e24b92d39e66852
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665855"
---
# <a name="windows-games-explorer-for-game-developers"></a>Explorador de juegos de Windows para desarrolladores de juegos

Windows Vista mejora la experiencia del usuario de juegos en Windows, incluyendo el explorador de juegos. El explorador de juegos se expone en el menú Inicio de Windows Vista como carpeta juegos y proporciona una ubicación central para el acceso a los juegos.

A partir de la versión de marzo de 2009 del SDK de DirectX, se usa un nuevo esquema de archivo de definición de juego (GDF) para admitir características de Windows 7, proveedor de juegos y fuente RSS, y IGameExplorer2. IGameExplorer2 es una nueva interfaz de Windows 7 que simplifica el proceso de integración de un juego con el explorador de juegos.

En este artículo se describe el proceso de registro de un juego con el explorador de juegos y controles parentales en Windows Vista y Windows 7 mediante el nuevo esquema GDF.

Contenido:

-   [Requisitos previos](#prerequisites)
-   [Integración con un instalador](#integrating-with-an-installer)
-   [Proceso de integración](#integration-process)
-   [Tareas del explorador de juegos](#games-explorer-tasks)
-   [Integración en InstallScript](#integrating-into-installscript)
-   [Integración en un paquete MSI](#integrating-into-an-msi-package)
-   [Sugerencias de depuración](#debugging-tips)
    -   [Prueba con código de ejemplo](#test-with-sample-code)
    -   [Asegúrese de que el juego se ha quitado correctamente](#make-sure-that-your-game-was-removed-properly)
    -   [Asegúrese de firmar con Authenticode](#be-sure-to-sign-using-authenticode)
    -   [Asegúrese de que los controles parentales están disponibles](#be-sure-that-parental-controls-are-available)
    -   [Comprobar que las tareas son del tipo correcto](#verify-that-tasks-are-of-the-correct-type)
    -   [Comprobar los datos en el archivo binario GDF](#verify-the-data-in-gdf-binary)
-   [Resumen](#summary)

## <a name="prerequisites"></a>Requisitos previos

Para poder integrar un juego en el explorador de juegos, debe crear un archivo de definición de juego (GDF). Un GDF es un archivo XML que contiene metadatos que describen el juego. En la versión 2009 de marzo del SDK de DirectX, se ha agregado una sección para el proveedor de juegos, la fuente RSS y la tarea de juego al esquema GDF. Para usar las instrucciones de este artículo, debe usar este nuevo formato GDF para crear el archivo GDF.

Microsoft proporciona una herramienta para crear GDFs en el SDK de DirectX, el editor de archivos de definición de juego, para facilitar este proceso de creación. Esta herramienta también ayuda a crear versiones localizadas de un GDF.

Una vez que se ha creado y localizado un GDF, debe encapsularse en una sección de recursos de un archivo binario (ya sea un ejecutable o un archivo DLL), junto con la miniatura y el icono del juego. GDF contiene todos los metadatos asociados al juego, incluida la valoración del juego. El control parental de Windows usa la clasificación del juego para permitir que los padres controlen el acceso al juego. El archivo binario que contiene GDF debe estar firmado digitalmente con un certificado Authenticode válido; de lo contrario, el explorador de juegos y el sistema de control parental omiten la clasificación del juego, ya que la información de clasificación no puede ser de confianza sin certificación. Para obtener más información sobre cómo firmar código con Authenticode, vea [firma de Authenticode para desarrolladores de juegos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

## <a name="integrating-with-an-installer"></a>Integración con un instalador

Para simplificar la integración del explorador de juegos, el ejemplo GameUXInstallHelper proporciona una API común que se puede llamar en Windows XP, Windows Vista y Windows 7. Está diseñado para trabajar con scripts para el sistema de instalación de InstallShield y Wise, así como acciones personalizadas de MSI y herramientas de instalación personalizadas. La detección del sistema operativo se controla dentro de este archivo DLL de ejemplo, por lo que el autor de la llamada no necesita preocuparse de si el cliente está ejecutando Windows XP, Windows Vista o Windows 7.

Las funciones exportadas por este archivo DLL son las siguientes:

<dl> <dt>

<span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**GameExplorerInstallW**
</dt> <dd>

Registra un juego con el explorador de juegos, dada una ruta de acceso al archivo binario GDF, una ruta de acceso completa a la carpeta donde está instalado el juego y el ámbito de instalación.

</dd> <dt>

<span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**GameExplorerInstallA**
</dt> <dd>

Registra un juego con el explorador de juegos. Versión ANSI de **GameExplorerInstallW**.

</dd> <dt>

<span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**GameExplorerUninstallW**
</dt> <dd>

Quita un juego del registro con el explorador de juegos, dada una ruta de acceso al archivo binario GDF.

</dd> <dt>

<span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**GameExplorerUninstallA**
</dt> <dd>

Quita un juego del registro con el explorador de juegos. Versión ANSI de **GameExplorerUninstallW**.

</dd> <dt>

<span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**GameExplorerSetMSIProperties**
</dt> <dd>

Configura las propiedades de CustomActionData para las acciones de una instalación personalizada diferida de MSI. El uso de esta función se describe con más detalle más adelante en este artículo.

</dd> <dt>

<span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**GameExplorerInstallUsingMSI**
</dt> <dd>

Agrega un juego al explorador de juegos. para su uso durante la instalación de una acción personalizada MSI.

</dd> <dt>

<span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**GameExplorerUninstallUsingMSI**
</dt> <dd>

Quitar un juego del explorador de juegos; para su uso durante la instalación de una acción personalizada MSI.

</dd> </dl>

Estas funciones se explican con más detalle en el encabezado GameUXInstallHelper. h.

## <a name="integration-process"></a>Proceso de integración

Una vez que se han agregado el GDF y los archivos relacionados a un recurso binario, es posible integrar el juego con el explorador de juegos. El uso de **GameUXInstallHelper** simplificará el proceso de integración. Para registrar el juego con el explorador de juegos, llame a **GameExplorerInstall** con una ruta de acceso al archivo binario GDF, una ruta de acceso completa a la carpeta donde está instalado el juego y el ámbito de instalación. Para quitar el registro del juego, llame a **GameExplorerUninstall** con una ruta de acceso al archivo binario GDF.

Tenga en cuenta que el proceso de eliminación solo quita una instalación única. Si se ha instalado un juego varias veces, este proceso debe repetirse para cada instalación única.

## <a name="games-explorer-tasks"></a>Tareas del explorador de juegos

Las tareas del explorador de juegos aparecerán en el menú contextual de un elemento en el explorador de juegos. Las tareas se dividen en tareas de reproducción y tareas de soporte técnico. Las tareas de reproducción inician un juego en un modo determinado, mientras que las tareas de soporte técnico sirven para cualquier otro propósito, como la vinculación a sitios Web.

En Windows Vista, las tareas son simplemente accesos directos que se encuentran en carpetas específicas. Las tareas de reproducción y las tareas de soporte se almacenan en carpetas con los nombres correspondientes PlayTasks y SupportTasks. GameUXInstallHelper puede leer la información de las tareas del juego desde el archivo binario GDF y crear todos los accesos directos automáticamente.

En Windows 7, los accesos directos a las tareas no son necesarios, porque el explorador de juegos obtiene toda la información de la tarea directamente del archivo binario GDF.

## <a name="integrating-into-installscript"></a>Integración en InstallScript

La llamada a las API del explorador de juegos desde el InstallScript de InstallShield se facilita mediante el ejemplo GameUXInstallHelper. Los pasos necesarios para la integración con InstallShield son los siguientes:

1.  Abra un proyecto de InstallScript en el editor de InstallShield.
2.  Agregue GameUXInstallHelper.dll al proyecto que se va a instalar en el directorio de destino.

    **Para agregar GameUXInstallHelper.dll a un proyecto de InstallScript:**

    1.  En la pestaña **Diseñador de instalación** , haga clic en datos de la **aplicación** en el panel de navegación de la izquierda.
    2.  Haga clic en **archivos y carpetas** y busque en **las carpetas del equipo de origen** para buscar GameUXInstallerHelper.dll en **los archivos del equipo de origen**.

        La ubicación predeterminada para GameUXInstallerHelper.dll es DirectX SDK root \\ Samples \\ C++ \\ Misc \\ bin \\ x86.

    3.  En **carpetas del equipo de destino**, haga clic en **carpeta de destino** de la aplicación.
    4.  Arrastre GameUXInstallerHelper.dll desde **los archivos del equipo de origen** a **los archivos del equipo de destino**.

3.  En el explorador de InstallScript, haga clic en el archivo InstallScript (normalmente Setup. RUL) que llama a la función DLL.
4.  Pegue el siguiente InstallScript en el archivo:

    ``` syntax
    typedef GUID
    begin
    LONG  Data1;
    SHORT Data2;
    SHORT Data3;
    CHAR  Data4(8);
    end;

    prototype LONG GameUXInstallHelper.GameExplorerInstallW(WSTRING, WSTRING, NUMBER);
    prototype LONG GameUXInstallHelper.GameExplorerUninstallW(WSTRING);

    function OnMoved()

    WSTRING gdfbin[256];
    WSTRING path[256];
    NUMBER scope;

    begin

    if !MAINTENANCE then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    path = TARGETDIR;
    gdfbin = TARGETDIR ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    if ALLUSERS == 1 then
    scope = 3;
    else
    scope = 2;
    endif;

    GameUXInstallHelper.GameExplorerInstallW( gdfbin, path, scope);

    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;

    function OnMoving()

    WSTRING gdfbin[256];

    begin

    if MAINTENANCE && UNINST != "" then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    gdfbin = path ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    GameUXInstallHelper.GameExplorerUninstallW(gdfbin);
    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;
    ```

## <a name="integrating-into-an-msi-package"></a>Integración en un paquete MSI

La siguiente es una descripción de alto nivel de los pasos necesarios para llamar a las API del explorador de juegos mediante acciones personalizadas de MSI:

1.  Agregue una propiedad a la tabla de propiedades MSI denominada "RelativePathToGDF" que contenga la ruta de acceso relativa al archivo binario GDF.
2.  Después de la acción CostFinalize, llame a la función **SetMSIGameExplorerProperties** de GameUXInstallHelper dll en una acción personalizada inmediata para establecer las propiedades MSI adecuadas para las demás acciones personalizadas.
3.  Tras la instalación, desencadene una acción personalizada diferida después de la acción InstallFiles que llama a la función **AddToGameExplorerUsingMSI** de GameUXInstallHelper dll. Si la instalación es para todos los usuarios, la acción personalizada debe establecer la marca msidbCustomActionTypeNoImpersonate; de lo contrario, no debe establecer esta marca. Por lo tanto, se definen dos acciones personalizadas prácticamente idénticas: GameUXAddAsAdmin y GameUXAddAsCurUser.
4.  Tras quitar la instalación, desencadene una acción personalizada diferida antes de la acción RemoveFiles que llama a la función GameUXInstallHelper DLL **RemoveFromGameExplorerUsingMSI**. Si la instalación fue para todos los usuarios, la acción personalizada debe establecer la marca msidbCustomActionTypeNoImpersonate; de lo contrario, no debe establecer esta marca. Por lo tanto, se definen dos acciones personalizadas prácticamente idénticas: GameUXRemoveAsAdmin y GameUXRemoveAsCurUser.
5.  Defina las acciones personalizadas de reversión para controlar el caso en el que el usuario cancela la instalación o eliminación después de que ya se haya producido una de estas acciones personalizadas. Esto da como resultado cuatro acciones personalizadas adicionales: GameUXRollBackAddAsAdmin, GameUXRollBackAddAsCurUser, GameUXRollBackRemoveAsAdmin y GameUXRollBackRemoveAsCurUser.

Este procedimiento se describe en detalle en las siguientes instrucciones, que describen un proceso que se puede realizar mediante un editor MSI, como el editor orca que se encuentra en el SDK de la plataforma. Algunos editores de MSI tienen asistentes que simplifican algunos de estos pasos de configuración.

**Para configurar un paquete MSI para la integración con el explorador de juegos**

1.  Abra el paquete MSI en orca.
2.  Agregue la fila que se muestra en la tabla siguiente a la tabla **binaria** del paquete MSI. 

    | Nombre   | Datos                                          |
    |--------|-----------------------------------------------|
    | GAMEUX | Ruta de acceso al archivo DLL \\GameUXInstallHelper.dll |

    

     

    > [!Note]  
    > Este archivo se incrustará en el paquete MSI, por lo que debe realizar este paso cada vez que vuelva a compilar GameUXInstallHelper.dll.

     

3.  Agregue las filas que se muestran en la tabla siguiente a la tabla **CustomAction** en el paquete MSI.

    | Acción                        | Tipo                                                                                                                                                                                                   | Source | Destino                         |
    |-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------------------------------|
    | GameUXSetMSIProperties        | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | GAMEUX | SetMSIGameExplorerProperties   |
    | GameUXAddAsAdmin              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXAddAsCurUser            | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackAddAsAdmin      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackAddAsCurUser    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsAdmin           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsCurUser         | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackRemoveAsAdmin   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackRemoveAsCurUser | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | AddToGameExplorerUsingMSI      |

    

     

4.  Agregue los valores que se muestran para Action, condition y Sequence en la tabla siguiente a la tabla **InstallExecuteSequence** del paquete MSI.

    | Acción                        | Condición                      | Secuencia | Notas                                                                                                                                                                                            |
    |-------------------------------|--------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | GameUXSetMSIProperties        |                                | 1015     | El número de secuencia coloca la acción poco después de CostFinalize.                                                                                                                                   |
    | GameUXAddAsAdmin              | NO instalado y ALLUSERS     | 4003     | Esta acción personalizada solo se producirá durante una instalación nueva para todos los usuarios. El número de secuencia coloca la acción después de InstallFiles y después de la reversión.                                 |
    | GameUXAddAsCurUser            | NO está instalado y no es ALLUSERS | 4004     | Esta acción personalizada solo se producirá durante una instalación nueva para el usuario actual. El número de secuencia coloca la acción después de InstallFiles y después de la reversión.                     |
    | GameUXRollBackAddAsAdmin      | NO instalado y ALLUSERS     | 4001     | Esta acción personalizada solo se producirá cuando se cancele una instalación nueva para todos los usuarios. El número de secuencia coloca la acción después de InstallFiles y antes de agregar la acción personalizada.             |
    | GameUXRollBackAddAsCurUser    | NO está instalado y no es ALLUSERS | 4002     | Esta acción personalizada solo se producirá cuando se cancele una instalación nueva para el usuario actual. El número de secuencia coloca la acción después de InstallFiles y antes de agregar la acción personalizada. |
    | GameUXRemoveAsAdmin           | QUITAR ~ = "ALL" Y ALLUSERS     | 3452     | Esta acción personalizada solo se producirá durante la eliminación de todos los usuarios. El número de secuencia coloca la acción directamente antes de RemoveFiles y después de la reversión.                                     |
    | GameUXRemoveAsCurUser         | QUITAR ~ = "ALL" Y NO ALLUSERS | 3453     | Esta acción personalizada solo se producirá durante la eliminación del usuario actual. El número de secuencia coloca la acción directamente antes de RemoveFiles y después de la reversión.                              |
    | GameUXRollBackRemoveAsAdmin   | QUITAR ~ = "ALL" Y ALLUSERS     | 3450     | Esta acción personalizada solo se producirá cuando se cancele la eliminación de todos los usuarios. El número de secuencia coloca la acción directamente antes de RemoveFiles y antes de la acción personalizada quitar.              |
    | GameUXRollBackRemoveAsCurUser | QUITAR ~ = "ALL" Y NO ALLUSERS | 3451     | Esta acción personalizada solo se producirá cuando se cancele la eliminación del usuario actual. El número de secuencia coloca la acción directamente antes de RemoveFiles y antes de la acción personalizada quitar.       |

    

     

5.  Agregue la fila que se muestra en la tabla siguiente a la tabla de propiedades del paquete MSI.

    | Propiedad          | Value                                                         |
    |-------------------|---------------------------------------------------------------|
    | RelativePathToGDF | \\nombre relativo de la ruta de acceso del archivo binario que contiene GDF |

    

     

    > [!Note]  
    > La ubicación especificada por la ruta de acceso es relativa a la ubicación especificada por la ruta de instalación. Por ejemplo, bin \\GDF.dll.

     

6.  Guarde el paquete MSI.

Para obtener información más detallada sobre los paquetes MSI y Windows Installer, vea [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Sugerencias de depuración

A continuación se muestran algunas sugerencias para ayudar a depurar problemas al llamar a las API del explorador de juegos:

### <a name="test-with-sample-code"></a>Prueba con código de ejemplo

La compilación de la solución de ejemplo GameUXInstallHelper creará un GameUXInstallHelper.dll y un GDFInstall.exe. La GDFInstall.exe es una aplicación de ejemplo que usa GameUXInstallHelper.dll. Al ejecutar GDFInstall.exe se le preguntará si desea instalar o quitar un archivo binario de GDF del explorador de juegos. Puede probar el archivo binario de GDF pasándolo como el primer argumento de la línea de comandos para GDFInstall.exe.

Si no tiene un archivo binario de GDF o no se puede instalar el suyo, pruebe a usar el GDF de ejemplo en el SDK de DirectX. El ejemplo GDFExampleBinary se encuentra en el SDK de DirectX y es simplemente un archivo DLL que solo contiene un archivo GDF. También se incluye en el origen, su proyecto GDFMaker. Puede compilarlo y probarlo mediante GDFInstall.exe. También puede comparar su XML con el suyo para identificar exactamente dónde está el problema.

### <a name="make-sure-that-your-game-was-removed-properly"></a>Asegúrese de que el juego se ha quitado correctamente

Si el juego ya está instalado en el explorador de juegos, las siguientes llamadas a **IGameExplorer:: AddGame** devolverán E \_ producirá un error, por lo que debe asegurarse de que el juego no esté instalado antes de realizar las pruebas. Esto también se aplica si instala GDF solo para el usuario actual e intenta instalar GDF para todos los usuarios. Primero debe quitar el juego de los usuarios actuales antes de que **IGameExplorer:: AddGame** se realice correctamente.

Si ejecuta **GDFInstall.exe enumeración**, la aplicación de ejemplo entrará en un modo diferente que enumerará todos los juegos del explorador de juegos instalados y le pedirá que los quite. También puede examinar y buscar en el registro en HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ GameUX para asegurarse de que el juego no está instalado para otro usuario del sistema. Sin embargo, no modifique estos valores del registro para ningún otro propósito, ya que no se garantiza que sigan siendo compatibles en versiones futuras del sistema operativo.

### <a name="be-sure-to-sign-using-authenticode"></a>Asegúrese de firmar con Authenticode

Si ha proporcionado una clasificación, pero no la ve en el explorador de juegos, asegúrese de que ha usado Authenticode para firmar el archivo ejecutable o DLL que contiene la clasificación. El explorador de juegos omite la información de clasificación en archivos sin firmar. Para obtener más información sobre Authenticode, consulte [firma Authenticode para desarrolladores de juegos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

### <a name="be-sure-that-parental-controls-are-available"></a>Asegúrese de que los controles parentales están disponibles

Asegúrese de que está probando controles parentales en una edición de Windows Vista que proporciona controles parentales: Home Basic, Home Premium o Ultimate. Windows Vista Business y Windows Vista Enterprise no proporcionan controles parentales, sin embargo, si está probando en Windows Vista Ultimate y el equipo de pruebas está unido a un dominio, debe cambiar la configuración de una directiva de grupo para que el control parental sea visible. Para ello, consulte [Introducción con el explorador de juegos](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85)).

### <a name="verify-that-tasks-are-of-the-correct-type"></a>Comprobar que las tareas son del tipo correcto

Si ha especificado tareas de soporte técnico que no aparecen en el explorador de juegos, compruebe que son todos los vínculos Web. Cualquier otra tarea de acceso directo debe crearse como tareas de reproducción. Las tareas se describen anteriormente en este artículo en [tareas del explorador de juegos](#games-explorer-tasks).

### <a name="verify-the-data-in-gdf-binary"></a>Comprobar los datos en el archivo binario GDF

GDFTrace.exe es una herramienta que se encuentra en el SDK de DirectX. Puede ejecutar GDFTrace.exe en el archivo binario de GDF y generará todos los metadatos de GDF contenidos en el archivo binario para cada idioma admitido para la validación rápida. También se muestran las advertencias sobre información que falta o está obsoleta.

## <a name="summary"></a>Resumen

El explorador de juegos de Windows Vista proporciona una forma sencilla y personalizable de presentar su juego a los usuarios de Windows Vista, pero también requiere que registre el juego con el sistema durante el proceso de instalación. El ejemplo GameUXInstallHelper simplifica enormemente este proceso para los desarrolladores.

 

 