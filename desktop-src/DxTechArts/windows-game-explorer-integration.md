---
title: Windows Explorador de juegos para desarrolladores de juegos
description: En este artículo se describe el proceso de registro de un juego con Games Explorer y controles parentales en Windows Vista y Windows 7 mediante el nuevo esquema de GDF.
ms.assetid: 628f14bf-2714-0d68-8267-4f7f48c2774a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6420b4783cfad7afd82483d45448ccb219342b4a7b88aa54e36c2de15ca0f778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070425"
---
# <a name="windows-games-explorer-for-game-developers"></a>Windows Explorador de juegos para desarrolladores de juegos

Windows Vista mejora la experiencia del usuario de juegos en Windows mediante la inclusión de Games Explorer. El Explorador de juegos se expone en el Windows inicio de Vista como la carpeta Juegos y proporciona una ubicación central para acceder a los juegos.

A partir de la versión de marzo de 2009 del SDK de DirectX, se usa un nuevo esquema de archivo de definición de juegos (GDF) para admitir características de Windows 7, game provider y fuente RSS e IGameExplorer2. IGameExplorer2 es una nueva interfaz de Windows 7 que simplifica el proceso de integración de un juego con Games Explorer.

En este artículo se describe el proceso de registro de un juego con Games Explorer y controles parentales en Windows Vista y Windows 7 mediante el nuevo esquema de GDF.

Contenido:

-   [Requisitos previos](#prerequisites)
-   [Integración con un instalador](#integrating-with-an-installer)
-   [Proceso de integración](#integration-process)
-   [Tareas del Explorador de juegos](#games-explorer-tasks)
-   [Integración en InstallScript](#integrating-into-installscript)
-   [Integración en un paquete MSI](#integrating-into-an-msi-package)
-   [Depuración Sugerencias](#debugging-tips)
    -   [Prueba con código de ejemplo](#test-with-sample-code)
    -   [Asegúrese de que el juego se quitó correctamente.](#make-sure-that-your-game-was-removed-properly)
    -   [Asegúrese de firmar con Authenticode.](#be-sure-to-sign-using-authenticode)
    -   [Asegúrese de que los controles parentales están disponibles.](#be-sure-that-parental-controls-are-available)
    -   [Comprobar que las tareas son del tipo correcto](#verify-that-tasks-are-of-the-correct-type)
    -   [Comprobación de los datos en el binario de GDF](#verify-the-data-in-gdf-binary)
-   [Resumen](#summary)

## <a name="prerequisites"></a>Requisitos previos

Para poder integrar un juego en Games Explorer, debe crear un archivo de definición de juego (GDF). Un GDF es un archivo XML que contiene metadatos que describen el juego. En la versión de marzo de 2009 del SDK de DirectX, se ha agregado una sección para el proveedor de juegos, la fuente RSS y la tarea de juego al esquema de GDF. Para usar las instrucciones de este artículo, debe usar este nuevo formato GDF para crear el archivo GDF.

Microsoft proporciona una herramienta para crear GDF en el SDK de DirectX, Editor de archivos de definición de juegos, para facilitar este proceso de creación. Esta herramienta también le ayuda a crear versiones localizadas de un GDF.

Una vez que se ha autorizado y localizado un GDF, se debe encapsular dentro de una sección de recursos de un archivo binario (ya sea un archivo ejecutable o DLL), junto con la miniatura y el icono del juego. El GDF contiene todos los metadatos asociados al juego, incluida la clasificación del juego. Windows Los controles parentales usan la clasificación del juego para permitir que los padres controlen el acceso al juego. El archivo binario que contiene el GDF debe estar firmado digitalmente con un certificado Authenticode válido; De lo contrario, Games Explorer y el sistema de control parental omiten la clasificación del juego, ya que la información de clasificación no puede ser de confianza sin certificación. Para más información sobre cómo firmar código con Authenticode, consulte [Firma de Authenticode para desarrolladores de juegos.](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

## <a name="integrating-with-an-installer"></a>Integración con un instalador

Para simplificar la integración de Games Explorer, el ejemplo GameUXInstallHelper proporciona una API común a la que se puede llamar en Windows XP, Windows Vista y Windows 7. Está diseñado para trabajar con scripts para InstallShield y Wise Installation System, así como con acciones personalizadas de MSI y herramientas de instalación personalizadas. La detección del sistema operativo se controla dentro de este archivo DLL de ejemplo, por lo que el autor de la llamada no tiene que preocuparse de si el cliente ejecuta Windows XP, Windows Vista o Windows 7.

Las funciones exportadas por este archivo DLL son las siguientes:

<dl> <dt>

<span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**GameExplorerInstallW**
</dt> <dd>

Registra un juego con Games Explorer, dada una ruta de acceso al binario de GDF, una ruta de acceso completa a la carpeta donde está instalado el juego y el ámbito de instalación.

</dd> <dt>

<span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**GameExplorerInstallA**
</dt> <dd>

Registra un juego con Games Explorer; Versión ANSI **de GameExplorerInstallW**.

</dd> <dt>

<span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**GameExplorerUninstallW**
</dt> <dd>

Quita un juego del registro con Games Explorer, dada una ruta de acceso al binario de GDF.

</dd> <dt>

<span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**GameExplorerUninstallA**
</dt> <dd>

Quita un juego del registro con Games Explorer; Versión ANSI **de GameExplorerUninstallW**.

</dd> <dt>

<span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**GameExplorerSetMSIProperties**
</dt> <dd>

Configura las propiedades CustomActionData para las acciones de una instalación personalizada diferida de MSI. El uso de esta función se describe con detalle más adelante en este artículo.

</dd> <dt>

<span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**GameExplorerInstallUsingMSI**
</dt> <dd>

Agrega un juego a Games Explorer; para su uso durante la instalación de una acción personalizada de MSI.

</dd> <dt>

<span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**GameExplorerUninstallUsingMSI**
</dt> <dd>

Quitar un juego de Games Explorer; para su uso durante la instalación de una acción personalizada de MSI.

</dd> </dl>

Estas funciones se explican más adelante en el encabezado GameUXInstallHelper.h.

## <a name="integration-process"></a>Proceso de integración

Una vez que el GDF y los archivos relacionados se han agregado a un recurso binario, es posible integrar el juego con Games Explorer. El **uso de GameUXInstallHelper simplificará** el proceso de integración. Para registrar el juego con Games Explorer, llame a **GameExplorerInstall** con una ruta de acceso al binario de GDF, una ruta de acceso completa a la carpeta donde está instalado el juego y el ámbito de instalación. Para quitar el registro del juego, llame a **GameExplorerUninstall** con una ruta de acceso al binario de GDF.

Tenga en cuenta que el proceso de eliminación solo quita una instalación única. Si un juego se ha instalado varias veces, este proceso debe repetirse para cada instalación única.

## <a name="games-explorer-tasks"></a>Tareas del Explorador de juegos

Las tareas de Games Explorer aparecerán en el menú contextual de un elemento de Games Explorer. Las tareas se dividen en tareas de reproducción y tareas de soporte técnico. Las tareas de juego inician un juego en un modo determinado, mientras que las tareas de soporte técnico sirven para cualquier otro propósito, incluida la vinculación a sitios web.

En Windows Vista, las tareas son simplemente accesos directos que se encuentran en carpetas específicas. Las tareas de reproducción y las tareas de soporte técnico se almacenan en carpetas con los nombres correspondientes PlayTasks y SupportTasks. GameUXInstallHelper puede leer la información de la tarea del juego desde el archivo binario de GDF y crear todos los accesos directos automáticamente.

En Windows 7, los accesos directos a las tareas no son necesarios, ya que Games Explorer obtiene toda la información de la tarea directamente del archivo binario de GDF.

## <a name="integrating-into-installscript"></a>Integración en InstallScript

Llamar a las API de Games Explorer desde InstallScript de InstallShield se facilita mediante el ejemplo GameUXInstallHelper. Los pasos necesarios para la integración con InstallShield son los siguientes:

1.  Abra un proyecto de InstallScript en el editor de InstallShield.
2.  Agregue GameUXInstallHelper.dll al proyecto que se va a instalar en el directorio de destino.

    **Para agregar GameUXInstallHelper.dll a un proyecto de InstallScript:**

    1.  En la pestaña **Diseñador de instalación** , haga clic en Datos de la **aplicación** en el panel de navegación de la izquierda.
    2.  Haga **clic en Archivos y carpetas** y busque en **Carpetas del** equipo de origen para GameUXInstallerHelper.dll en Archivos del equipo de **origen.**

        La ubicación predeterminada de la GameUXInstallerHelper.dll es DirectX SDK root \\ Samples \\ C++ Misc Bin x86 (Ejemplos de C++ \\ misc Bin \\ \\ x86).

    3.  En **Carpetas del equipo de destino,** haga clic **en Carpeta de destino de la aplicación**.
    4.  Arrastre GameUXInstallerHelper.dll desde **Archivos del equipo de origen** hasta Archivos del equipo de **destino**.

3.  En el explorador de InstallScript, haga clic en el archivo InstallScript (normalmente setup.rul) que llama a la función DLL.
4.  Pegue el siguiente archivo InstallScript en el archivo :

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

A continuación se muestra una descripción de alto nivel de los pasos necesarios para llamar a las API de Games Explorer mediante acciones personalizadas de MSI:

1.  Agregue una propiedad a la tabla de propiedades msi denominada "RelativePathToGDF" que contenga la ruta de acceso relativa al binario de GDF.
2.  Después de la acción CostFinalize, llame a la función DLL **SetMSIGameExplorerProperties** de GameUXInstallHelper en una acción personalizada inmediata para establecer las propiedades MSI adecuadas para las otras acciones personalizadas.
3.  Tras la instalación, desencadene una acción personalizada diferida después de la acción InstallFiles que llama a la función DLL **AddToGameExplorerUsingMSI** de GameUXInstallHelper. Si la instalación es para todos los usuarios, la acción personalizada debe establecer la marca msidbCustomActionTypeNoImpersonate; De lo contrario, no debe establecer esta marca. Por lo tanto, se definen dos acciones personalizadas casi idénticas: GameUXAddAsAdmin y GameUXAddAsCurUser.
4.  Tras la eliminación de la instalación, desencadene una acción personalizada diferida antes de la acción RemoveFiles que llama a la función DLL GameUXInstallHelper **RemoveFromGameExplorerUsingMSI**. Si la instalación era para todos los usuarios, la acción personalizada debe establecer la marca msidbCustomActionTypeNoImpersonate; De lo contrario, no debe establecer esta marca. Por lo tanto, se definen dos acciones personalizadas casi idénticas: GameUXRemoveAsAdmin y GameUXRemoveAsCurUser.
5.  Defina acciones personalizadas de reversión para controlar el caso en el que el usuario cancela la instalación o eliminación después de que ya se haya producido una de estas acciones personalizadas. Esto da como resultado cuatro acciones personalizadas adicionales: GameUXRollBackAddAsAdmin, GameUXRollBackAddAsCurUser, GameUXRollBackRemoveAsAdmin y GameUXRollBackRemoveAsCurUser.

Este procedimiento se describe en detalle en las instrucciones siguientes, que describen un proceso que se puede realizar mediante un editor MSI, como el editor de Orca que se encuentra en el SDK de plataforma. Algunos editores msi tienen asistentes que simplifican algunos de estos pasos de configuración.

**Para configurar un paquete MSI para la integración con Games Explorer**

1.  Abra el paquete MSI en Orca.
2.  Agregue la fila que se muestra en la tabla siguiente a **la tabla Binaria** del paquete MSI. 

    | Nombre   | Datos                                          |
    |--------|-----------------------------------------------|
    | GAMEUX | ruta de acceso al archivo DLL \\GameUXInstallHelper.dll |

    

     

    > [!Note]  
    > Este archivo se incrustará en el paquete MSI, por lo que debe realizar este paso cada vez que vuelva a compilar GameUXInstallHelper.dll.

     

3.  Agregue las filas que se muestran en la tabla siguiente a la **tabla CustomAction** del paquete MSI.

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

    

     

4.  Agregue los valores que se muestran para Acción, Condición y Secuencia en la tabla siguiente a la **tabla InstallExecuteSequence** del paquete MSI.

    | Acción                        | Condición                      | Secuencia | Notas                                                                                                                                                                                            |
    |-------------------------------|--------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | GameUXSetMSIProperties        |                                | 1015     | El número de secuencia coloca la acción poco después de CostFinalize.                                                                                                                                   |
    | GameUXAddAsAdmin              | NO INSTALADO Y ALLUSERS     | 4003     | Esta acción personalizada solo se realizará durante una instalación nueva para todos los usuarios. El número de secuencia coloca la acción después de InstallFiles y después de las reversión.                                 |
    | GameUXAddAsCurUser            | NO INSTALADO Y NO TODOS LOS USUARIOS | 4004     | Esta acción personalizada solo se realizará durante una instalación nueva solo para el usuario actual. El número de secuencia coloca la acción después de InstallFiles y después de las reversión.                     |
    | GameUXRollBackAddAsAdmin      | NO INSTALADO Y ALLUSERS     | 4001     | Esta acción personalizada solo se realizará cuando se cancele una instalación nueva para todos los usuarios. El número de secuencia coloca la acción después de InstallFiles y antes de la acción agregar personalizada.             |
    | GameUXRollBackAddAsCurUser    | NO INSTALADO Y NO TODOS LOS USUARIOS | 4002     | Esta acción personalizada solo se realizará cuando solo se cancele una instalación nueva para el usuario actual. El número de secuencia coloca la acción después de InstallFiles y antes de la acción agregar personalizada. |
    | GameUXRemoveAsAdmin           | REMOVE~="ALL" Y ALLUSERS     | 3452     | Esta acción personalizada solo se realizará durante la eliminación de todos los usuarios. El número de secuencia coloca la acción directamente antes de RemoveFiles y después de las reversión.                                     |
    | GameUXRemoveAsCurUser         | REMOVE~="ALL" Y NO ALLUSERS | 3453     | Esta acción personalizada solo se realizará durante la eliminación del usuario actual. El número de secuencia coloca la acción directamente antes de RemoveFiles y después de las reversión.                              |
    | GameUXRollBackRemoveAsAdmin   | REMOVE~="ALL" Y ALLUSERS     | 3450     | Esta acción personalizada solo se realizará cuando se cancele la eliminación de todos los usuarios. El número de secuencia coloca la acción directamente antes de RemoveFiles y antes de la acción personalizada Quitar.              |
    | GameUXRollBackRemoveAsCurUser | REMOVE~="ALL" Y NO ALLUSERS | 3451     | Esta acción personalizada solo se realizará cuando se cancele la eliminación del usuario actual. El número de secuencia coloca la acción directamente antes de RemoveFiles y antes de la acción personalizada Quitar.       |

    

     

5.  Agregue la fila que se muestra en la tabla siguiente a la tabla Property del paquete MSI.

    | Propiedad          | Value                                                         |
    |-------------------|---------------------------------------------------------------|
    | RelativePathToGDF | nombre de ruta \\ de acceso de archivo relativa del archivo binario que contiene el GDF |

    

     

    > [!Note]  
    > La ubicación especificada por la ruta de acceso es relativa a la ubicación especificada por la ruta de acceso de instalación. Por ejemplo, bin \\GDF.dll.

     

6.  Guarde el paquete MSI.

Para obtener información más detallada sobre los paquetes MSI y Windows Installer, [consulte Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Depuración Sugerencias

Estas son algunas sugerencias para ayudar a depurar problemas al llamar a las API de Games Explorer:

### <a name="test-with-sample-code"></a>Prueba con código de ejemplo

La creación de la solución de ejemplo GameUXInstallHelper creará un GameUXInstallHelper.dll y un GDFInstall.exe. La GDFInstall.exe es una aplicación de ejemplo que usa GameUXInstallHelper.dll. Al GDFInstall.exe se le preguntará si quiere instalar o quitar un binario de GDF del explorador de juegos. Puede probar el archivo binario de GDF si lo pasa como el primer argumento de línea de comandos para GDFInstall.exe.

Si no tiene un archivo binario de GDF o el de usted no se puede instalar, pruebe a usar el GDF de ejemplo en el SDK de DirectX. El ejemplo GDFExampleBinary se encuentra en el SDK de DirectX y es simplemente un archivo DLL que solo contiene un archivo GDF. También se incluye en el origen su proyecto GDFMaker. Puede compilarlo y probarlo mediante GDFInstall.exe. También puede comparar su XML con el de usted para identificar exactamente dónde está el problema.

### <a name="make-sure-that-your-game-was-removed-properly"></a>Asegúrese de que el juego se quitó correctamente.

Si el juego ya está instalado en El Explorador de juegos, las llamadas posteriores a **IGameExplorer::AddGame** devolverán E FAIL, por lo que debe asegurarse de que el juego no esté instalado antes de realizar \_ las pruebas. Esto también se aplica si instala el GDF solo para el usuario actual y, a continuación, intenta instalar el GDF para todos los usuarios. Primero debe quitar el juego de los usuarios actuales antes de **que IGameExplorer::AddGame** se realizará correctamente.

Si ejecuta una **enumeraciónGDFInstall.exe**, la aplicación de ejemplo entrará en un modo diferente que enumerará todos los juegos instalados de Games Explorer y le pedirá que los quite. También puede examinar y buscar en el Registro en HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion GameUX \\ para asegurarse de que el juego no está instalado para otro usuario en el sistema. Sin embargo, no modifique esta configuración del Registro para ningún otro propósito, ya que no se garantiza que sigan siendo compatibles en versiones futuras del sistema operativo.

### <a name="be-sure-to-sign-using-authenticode"></a>Asegúrese de firmar con Authenticode.

Si ha proporcionado una clasificación, pero no la ve en Games Explorer, asegúrese de que ha usado Authenticode para firmar el archivo ejecutable o DLL que contiene la clasificación. El Explorador de juegos omite la información de clasificaciones de los archivos sin signo. Para obtener más información sobre Authenticode, vea [Firma de Authenticode para desarrolladores de juegos.](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

### <a name="be-sure-that-parental-controls-are-available"></a>Asegúrese de que los controles parentales están disponibles.

Asegúrese de probar los controles parentales en una edición de Windows Vista que proporciona controles parentales: Home Basic, Home Premium o Ultimate. Windows Vista Business y Windows Vista Enterprise no proporcionan controles parentales, pero si realiza pruebas en Windows Vista Ultimate y el equipo de prueba está unido a un dominio, debe cambiar una configuración de directiva de grupo para que los controles parentales sean visibles. Para ello, consulte Tareas iniciales [con Games Explorer](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85)).

### <a name="verify-that-tasks-are-of-the-correct-type"></a>Comprobar que las tareas son del tipo correcto

Si ha especificado tareas de soporte técnico que no aparecen en Games Explorer, compruebe que se trata de todos los vínculos web. Cualquier otra tarea de acceso directo debe crearse como tareas de reproducción. Las tareas se tratan anteriormente en este artículo en [Tareas de Games Explorer](#games-explorer-tasks).

### <a name="verify-the-data-in-gdf-binary"></a>Comprobación de los datos en el binario de GDF

GDFTrace.exe es una herramienta que se encuentra en el SDK de DirectX. Puede ejecutar GDFTrace.exe en el binario de GDF y se mostrarán todos los metadatos de GDF contenidos en el archivo binario para cada lenguaje admitido para una validación rápida. También muestra las advertencias sobre la información que falta o no está actualizada.

## <a name="summary"></a>Resumen

El Explorador de juegos de Windows Vista proporciona una manera fácil y personalizable de presentar el juego a los usuarios de Windows Vista, pero también requiere que registre el juego con el sistema durante el proceso de instalación. El ejemplo GameUXInstallHelper simplifica enormemente este proceso para los desarrolladores.

 

 