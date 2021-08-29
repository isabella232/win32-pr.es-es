---
title: Implementación de Direct3D 11 para desarrolladores de juegos
description: En este artículo se describe cómo implementar los componentes de Direct3D 11 en un sistema si es necesario.
ms.assetid: 1fd43638-0d67-4a94-3be6-8789095f491e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a65cb51a360fbe732566e3560719d02a087e0a46e45b07f41413e6faa0f66a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627795"
---
# <a name="direct3d-11-deployment-for-game-developers"></a>Implementación de Direct3D 11 para desarrolladores de juegos

En este artículo se describe cómo implementar los componentes de Direct3D 11 en un sistema si es necesario.

-   [Información general](#overview)
-   [Direct3D 11.3](#direct3d-113)
-   [Direct3D 11.2](#direct3d-112)
-   [Direct3D 11.1](#direct3d-111)
-   [D3D11InstallHelper.dll](#d3d11installhelperdll)
-   [D3D11Install.exe](#d3d11installexe)
-   [Integración en programas de instalación](#integrating-into-installation-programs)
    -   [Integración en InstallShield](#integrating-into-installshield)
    -   [Integración en un paquete MSI](#integrating-into-an-msi-package)
-   [Depuración Sugerencias](#debugging-tips)
-   [Configuración corporativa](#corporate-settings)
-   [Artículos relacionados](#related-articles)

## <a name="overview"></a>Información general

La API de Direct3D 11 amplía la API existente de Direct3D 10.1 con compatibilidad con la representación multiproceso y la creación de recursos, el sombreador de proceso, la teselación de hardware, la compresión de textura BC6H/BC7 y el modelo de sombreador HLSL 5.0 con vinculación dinámica del sombreador. Además del componente Direct3D 11, se incluyen varios componentes gráficos adicionales en el entorno de ejecución de DirectX 11: Direct3D 11, DXGI 1.1, niveles de características de 10level9, dispositivo de representación de software WARP10, Direct2D, DirectWrite y direct3D 10.1 actualizado con compatibilidad con 10level9 y WARP10. Para obtener información sobre estos y otros componentes Windows gráficos, vea [API de gráficos en Windows](graphics-apis-in-windows-vista.md).

Todos estos nuevos componentes gráficos están integrados en los sistemas operativos Windows 7 y Windows Server 2008 R2. La API de Direct3D 11 y los componentes relacionados también se pueden instalar en Windows Vista mediante una actualización del sistema de Windows Update; consulte Knowledge Base artículo [KB 971644](https://support.microsoft.com/kb/971644). Esta actualización requiere Windows Vista y Service Pack 2. Por lo tanto, es probable que los usuarios finales con actualizaciones automáticas habilitadas ya tengan instalados los componentes de Direct3D 11, al igual que todos los Windows 7 usuarios.

El ejemplo D3D11InstallHelper está diseñado para simplificar la detección de la API de Direct3D 11, instalar automáticamente la actualización del sistema si procede en el equipo de un usuario final y proporcionar los mensajes adecuados al usuario final en el procedimiento manual si se requiere un Service Pack más reciente.

> [!Note]  
> El compilador HLSL (D3DCompile.dll) y la biblioteca de utilidades \* D3DX para Direct3D 11 (D3DX11.dll) no están integrados en ninguna versión del sistema operativo Windows, pero se pueden implementar como parte del instalador de una aplicación mediante la tecnología DirectSetup existente; para obtener más información sobre el uso de DirectSetup, vea Instalación de \* [DirectX](/windows/desktop/DxTechArts/directx-setup-for-game-developers)para desarrolladores de juegos. "Effects 11" está disponible como biblioteca de compatibilidad de código fuente compartido en Effects for Direct3D 11 Update (Efectos para [direct3D 11 Update)](https://github.com/Microsoft/FX11)y se puede incluir directamente en una aplicación (muy parecido a la biblioteca de utilidades DXUT). Por lo tanto, no tiene ningún requisito adicional de redistribución en tiempo de ejecución.

## <a name="direct3d-113"></a>Direct3D 11.3

Windows 10 se incluye con la API de Direct3D 11.3 integrada. Consulte [Características de Direct3D 11.3](/windows/desktop/direct3d11/direct3d-11-3-features) para obtener una lista de las nuevas características de la API de Direct3D 11.3.

## <a name="direct3d-112"></a>Direct3D 11.2

Windows 8.1 y Windows Server 2012 R2 se envían con la API de Direct3D 11.2 integrada. Consulte [Características de Direct3D 11.2](/windows/desktop/direct3d11/direct3d-11-2-features) para obtener una lista de las nuevas características de la API de Direct3D 11.2.

## <a name="direct3d-111"></a>Direct3D 11.1

Windows 8 y Windows Server 2012 con la API [de Direct3D 11.1](/windows/desktop/direct3d11/direct3d-11-1-features) integrada. La compatibilidad parcial con la API de Direct3D 11.1 está disponible en Windows 7 o Windows Server 2008 R2 con la actualización de plataforma [para Windows 7](https://support.microsoft.com/kb/2670838) instalada. Para obtener más información sobre la actualización de plataforma para Windows 7, vea Actualización de plataforma [para Windows 7](platform-update-for-windows-7.md).

## <a name="d3d11installhelperdll"></a>D3D11InstallHelper.dll

D3D11InstallHelper.dll hospeda la funcionalidad principal para detectar componentes de Direct3D 11 y realizar la actualización del sistema a través del servicio Windows Update, si procede. El archivo DLL no muestra mensajes ni cuadros de diálogo directamente.

El archivo DLL consta de los siguientes puntos de entrada:

<dl> <dt>

<span id="CheckDirect3D11Status"></span><span id="checkdirect3d11status"></span><span id="CHECKDIRECT3D11STATUS"></span>CheckDirect3D11Status
</dt> <dd>

Esta función realiza las comprobaciones necesarias y devuelve el estado de Direct3D 11 en este equipo. Esta función no requiere derechos de administrador.

-   Un estado D3D11 STATUS INSTALLED indica que \_ Direct3D 11 ya está instalado en el equipo y \_ está listo para su uso.
-   D3D11 STATUS NOT SUPPORTED indica que esta versión de Windows no admite \_ \_ \_ Direct3D 11 ni tecnologías relacionadas.
-   El estado D3D11 STATUS NEED LATEST SP indica que el usuario debe instalar la versión \_ Windows Service Pack de Vista más \_ \_ \_ reciente.
-   Por último, un estado D3D11 STATUS REQUIRES UPDATE indica que el sistema no tiene \_ \_ Instalado Direct3D 11, pero que la actualización del sistema se aplica a esta \_ versión de Windows.

</dd> <dt>

<span id="DoUpdateForDirect3D11"></span><span id="doupdatefordirect3d11"></span><span id="DOUPDATEFORDIRECT3D11"></span>DoUpdateForDirect3D11
</dt> <dd>

Esta función usa la API Windows update para realizar la actualización del sistema para instalar Direct3D 11 en este sistema, si procede. Tenga en cuenta que esta función requiere conectividad de red para Windows update se realiza correctamente, así como derechos administrativos. Toma una función de devolución de llamada de progreso opcional y un puntero de contexto de usuario, y devuelve un código de resultado final cuando se completa.

-   El resultado de D3D11PLIQUEN RESULT SUCCESS indica que la actualización del sistema se aplicó y está lista para su uso, mientras que \_ \_ D3D11 LE RESULT SUCCESS REBOOT indica que la actualización del sistema requiere que el equipo se reinicie antes de que se \_ \_ \_ complete. Tenga en cuenta que esta función no programa un reinicio del sistema.
-   D3D11 RESULT NOT SUPPORTED indica que la actualización del sistema no \_ se aplica a esta versión de \_ \_ Windows. Este resultado no debería producirse si solo se llama a esta función después de obtener D3D11 STATUS \_ REQUIRES UPDATE status de \_ \_ CheckDirect3D11Status.
-   Un resultado de D3D11LA ACTUALIZACIÓN DE RESULTADOS DE D3D11 NO ENCONTRADO indica que no se encontró el paquete de actualización del sistema en \_ \_ los servidores Windows \_ \_ update.
-   Si se produce un error en la descarga o instalación de la actualización de Windows, se devolverá D3D11LA DESCARGA DE LA ACTUALIZACIÓN DE RESULTADOS de D3D11 FAILED o \_ \_ \_ \_ D3D11 NULL \_ RESULT UPDATE INSTALL FAILED como \_ \_ \_ resultado.
-   Si se devuelve un error de conectividad de red desde la API de actualización de Windows, se devuelve el resultado D3D11 NULL RESULT WU SERVICE ERROR, lo que indica que el problema puede ser intermitente o relacionado con la configuración de red o la configuración del \_ \_ \_ \_ firewall. Intentar de nuevo la función de actualización puede ser correcta.

</dd> </dl>

Para obtener más información sobre la API Windows Update, [consulte Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client).

## <a name="d3d11installexe"></a>D3D11Install.exe

> [!Note]  
> D3D11Install.exe requiere D3D11InstallHelper.dll ejecutar.

D3D11Install.exe es una herramienta para usar D3D11InstallHelper.dll como un instalador independiente completo con mensajes de interfaz de usuario y de usuario final, así como para actuar como ejemplo para el uso adecuado del archivo DLL. El proceso se cierra con un 0 si Direct3D 11 ya está instalado, si la actualización del sistema se aplica correctamente sin necesidad de reiniciar el sistema, si se requiere una instalación de Service Pack o si este equipo no admite Direct3D 11. Se devuelve un valor 1 si la actualización del sistema se aplica correctamente y requiere que se complete un reinicio del sistema. Se devuelve un 2 para otras condiciones de error. Tenga en cuenta que este archivo ejecutable requiere derechos de administrador para ejecutarse y tiene un manifiesto que solicita elevación cuando se ejecuta en Windows Vista o Windows 7 con UAC habilitado. D3D11Install.exe puede usarse como una herramienta independiente para implementar la actualización de Direct3D 11, o bien puede ser utilizada directamente por los instaladores.

Admite los siguientes modificadores de línea de comandos:

<dl> <dt>

<span id="_quiet__"></span><span id="_QUIET__"></span>/quiet 
</dt> <dd>

No muestra mensajes, avisos, cuadros de diálogo de progreso ni mensajes de error.

</dd> <dt>

<span id="_passive__"></span><span id="_PASSIVE__"></span>/passive 
</dt> <dd>

No muestra ningún mensaje, aviso o mensaje de error, pero mostrará el cuadro de diálogo progreso.

</dd> <dt>

<span id="_minimal__"></span><span id="_MINIMAL__"></span>/minimal 
</dt> <dd>

Muestra solo mensajes mínimos.

</dd> <dt>

<span id="_y__"></span><span id="_Y__"></span>/y 
</dt> <dd>

Suprime las solicitudes para confirmar la instalación de la actualización, si es necesario y aplicable, para una instalación estándar y mínima.

</dd> <dt>

<span id="_langid_decimal__"></span><span id="_LANGID_DECIMAL__"></span>/langid decimal 
</dt> <dd>

Fuerza el código de identificador de idioma que se debe usar al mostrar los mensajes del usuario final y los recursos del cuadro de diálogo. El valor predeterminado es 1024, que usa la configuración de idioma predeterminada del sistema.

</dd> <dt>

<span id="_wu__"></span><span id="_WU__"></span>/wu 
</dt> <dd>

Fuerza el uso de Windows Update en lugar del valor predeterminado del sistema, que puede ser Windows Server Update Services (WSUS) que se ejecuta en un servidor administrado o en alguna otra configuración no estándar.

</dd> </dl>

## <a name="integrating-into-installation-programs"></a>Integración en programas de instalación

Para cumplir con el Requisito técnico [3.1](/windows/desktop/DxTechArts/games-for-windows-technical-requirements-1-1-0006)para juegos de Windows, es necesario tener cuidado para que las solicitudes del usuario final se presenten al principio del proceso de instalación y para asegurarse de que no hay varias solicitudes de elevación relacionadas con UAC. Hay tres opciones básicas para lograr este objetivo:

1.  El método más básico consiste en ejecutar el D3D11Install.exe con el modificador de línea de comandos **/minimal**. Esto debe hacerse al principio del instalador Q&A y la instalación debe usar el valor devuelto de 1 para indicar que se debe programar un reinicio al final de la instalación. La ejecución del programa requiere derechos administrativos.
2.  Use D3D11InstallHelper.dll directamente para detectar la necesidad de la actualización, proporcionando los mensajes de usuario final necesarios para el estado D3D11 STATUS NEED LATEST SP, donde la resolución requiere operaciones manuales del \_ \_ \_ \_ usuario. El resultado de estado de D3D11 STATUS NOT SUPPORTED podría usarse para controlar la instalación de recursos relacionados con Direct3D 11 o como una condición de error para aplicaciones solo de \_ \_ Direct3D 11, pero de lo contrario no es necesariamente un mensaje de usuario final \_ útil. Para el estado D3D11 STATUS REQUIRES UPDATE, el instalador puede usar directamente el punto de entrada \_ \_ de DLL DoUpdateForDirect3D11 para realizar la actualización y controlar los distintos mensajes de usuario final \_ resultantes. Para encontrar ejemplos de mensajes estándar, examine el cuadro D3D11Install.exe de diálogo y los recursos de la tabla de cadenas. El punto de entrada de actualización requiere derechos de administrador.
3.  Un enfoque híbrido es comprobar el estado con D3D11InstallHelper.dll y, en el caso del código de estado D3D11 STATUS \_ NEED LATEST SP o \_ \_ \_ D3D11 STATUS \_ REQUIRES UPDATE, \_ \_ D3D11Install.exe   se puede ejecutar con los modificadores /minimal e /y para mostrar el cuadro de diálogo o para realizar la actualización, según sea necesario. Estos pasos deben realizarse al principio del proceso de instalación, normalmente inmediatamente después de la Q&A, y la ejecución del ejecutable requiere derechos administrativos.

### <a name="integrating-into-installshield"></a>Integración en InstallShield

El control de la implementación de Direct3D 11 desde InstallScript de InstallShield se realiza fácilmente mediante el ejemplo D3D11InstallHelper. Los pasos necesarios para la integración con InstallShield mediante InstallScript son los siguientes (mediante el método 3, descrito en la sección anterior):

1.  Abra un proyecto de InstallScript en el editor de InstallShield.
2.  Agregue D3D11InstallHelper.dll y D3D11Install.exe al proyecto en **Archivos de soporte técnico**.

    **Para agregar los archivos a la Project**

    1.  En la **pestaña Diseñador de instalación,** haga clic en Archivos de soporte **técnico/Paneles** en **Comportamiento y lógica** en el panel de navegación de la izquierda.
    2.  Haga **clic en Independiente del** lenguaje y, a continuación, haga clic con el botón derecho en la **ventana** Archivos y seleccione **Insertar archivos.** Vaya para agregar D3D11InstallHelper.dll y D3D11Install.exe. La ubicación predeterminada de estos archivos es: Ejemplos raíz del SDK \\ \\ C++ \\ Misc \\ Bin \\ x86

3.  En el explorador de InstallScript, haga clic en el archivo InstallScript (normalmente Setup.rul) que llamará al archivo DLL o ejecutable, ubicado en **Comportamiento** y lógica en el panel de navegación de la izquierda.
4.  Pegue el siguiente archivo InstallScript en el archivo situado cerca de la parte superior:

    ``` syntax
#define D3D11IH_STATUS_INSTALLED       0
#define D3D11IH_STATUS_NOT_SUPPORTED   1
#define D3D11IH_STATUS_REQUIRES_UPDATE 2
#define D3D11IH_STATUS_NEED_LATEST_SP  3
#define D3D11IH_STATUS_ERROR           -1
    prototype NUMBER D3D11InstallHelper.CheckDirect3D11StatusIS();

#define D3D11IH_RESULT_SUCCESS                0
#define D3D11IH_RESULT_SUCCESS_REBOOT         1
#define D3D11IH_RESULT_NOT_SUPPORTED          2
#define D3D11IH_RESULT_UPDATE_NOT_FOUND       3
#define D3D11IH_RESULT_UPDATE_DOWNLOAD_FAILED 4
#define D3D11IH_RESULT_UPDATE_INSTALL_FAILED  5
#define D3D11IH_RESULT_WU_SERVICE_ERROR       6
#define D3D11IH_RESULT_ERROR                  -1
    prototype NUMBER D3D11InstallHelper.DoUpdateForDirect3D11IS(BOOL);
    ```

5.  Pegue el siguiente valor de InstallScript en el archivo de la función **OnFirstUIBefore,** justo antes de la devolución 0:

    ``` syntax
    Dlg_D3D11:
        UseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        nResult = D3D11InstallHelper.CheckDirect3D11StatusIS();   
        UnUseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        
        if ( nResult = D3D11IH_STATUS_REQUIRES_UPDATE
             || nResult = D3D11IH_STATUS_NEED_LATEST_SP) then
            nResult = LaunchAppAndWait(
    SUPPORTDIR^"D3D11Install.exe",
    "/minimal /y", WAIT);
            if ( nResult < 0 ) then
                MessageBox("Unable to launch D3D11Install.exe",
     SEVERE);
            elseif ( nResult == 1 ) then
                BATCH_INSTALL = 1;
            endif;          
        endif;
    ```

### <a name="integrating-into-an-msi-package"></a>Integración en un paquete MSI

A continuación se muestra una descripción de alto nivel de los pasos necesarios para integrar la implementación de Direct3D 11 mediante acciones personalizadas de MSI (mediante el método 3, descrito anteriormente en este tema):

1.  Agregue una propiedad a la tabla de propiedades MSI denominada **RelativePathToD3D11JET** que contenga la ruta de acceso relativa a D3D11Install.exe y D3D11InstallHelper.dll durante la instalación (normalmente se encuentra en la imagen multimedia). Esto también establece una propiedad MSI D3D11MODE STATUS en el estado devuelto por CheckDirect3D11Status (una propiedad de cadena igual al símbolo de enumeración \_ o "ERROR").
2.  Después de la acción CostFinalize, llame a la función **D3D11InstallHelper.dll SetD3D11InstallMSIProperties** como una acción personalizada inmediata para establecer las propiedades MSI adecuadas para las otras acciones personalizadas.
3.  Tras la instalación, desencadene una acción personalizada diferida después de la acción InstallFiles que llama a la D3D11InstallHelper.dll **doD3D11InstallUsingMSI**. La acción personalizada debe establecer la marca msidbCustomActionTypeNoImpersonate para que se ejecute en un contexto con privilegios elevados.
4.  Después de la acción InstallFinalize, llame a la función **D3D11InstallHelper.dll FinishD3D11InstallUsingMSI** como una acción personalizada inmediata para controlar el código de resultado de la solicitud de reinicio correcto, si es necesario.

Este procedimiento se describe en detalle en las instrucciones siguientes, que describen un proceso que se puede realizar mediante un editor MSI, como el [editor de Orca](/windows/desktop/Msi/orca-exe). Algunos editores msi tienen asistentes que simplifican algunos de estos pasos de configuración.

**Para configurar un paquete MSI para la integración con D3D11InstallHelper.dll**

1.  Abra el paquete MSI en Orca.
2.  Agregue la fila que se muestra en la tabla siguiente a la tabla Binary en el paquete MSI.

    | Nombre    | data                                         |
    |---------|----------------------------------------------|
    | D3D11JET | Ruta de acceso del archivo al archivo DLL \\D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > Este archivo se incrustará en el paquete MSI, por lo que debe realizar este paso cada vez que vuelva a compilar D3D11InstallHelper.dll.

     

3.  Agregue las filas que se muestran en la tabla siguiente a la tabla CustomAction en el paquete MSI. 

    | Acción              | Tipo                                                                                                                                                                   | Source  | Destino                       |
    |---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|------------------------------|
    | Direct3D11SetProps  | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11JET | SetD3D11InstallMSIProperties |
    | Direct3D11DoInstall | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137 | D3D11JET | DoD3D11InstallUsingMSI       |
    | Direct3D11Finish    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11JET | FinishD3D11InstallUsingMSI   |

    

     

4.  Agregue los valores que se muestran para Acción, Condición y Secuencia en la tabla siguiente a la tabla InstallExecuteSequence del paquete MSI. 

    | Acción              | Condición     | Secuencia | Notas                                                                                                                                                          |
    |---------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Direct3D11SetProps  |               | 1016     | El número de secuencia coloca la acción poco después de CostFinalize.                                                                                                 |
    | Direct3D11DoInstall | NO instalado | 4004     | Esta acción personalizada solo se realizará durante una nueva instalación para todos los usuarios. El número de secuencia coloca la acción después de InstallFiles y después de las reversión. |
    | Direct3D11Finish    |               | 6615     | El número de secuencia coloca la acción poco después de InstallFinalize.                                                                                              |

    

     

5.  Agregue la fila que se muestra en la tabla siguiente a la **tabla Property** del paquete MSI. 

    | Propiedad              | Value                                                                        |
    |-----------------------|------------------------------------------------------------------------------|
    | RelativePathToD3D11MT | ruta de acceso relativa al archivo que D3D11Install.exe y D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > La ubicación especificada por la ruta de acceso es relativa a la ubicación especificada por la ruta de instalación, por ejemplo, \\ "redist".

     

6.  Guarde el paquete MSI. Para obtener información más detallada sobre los paquetes MSI y Windows Installer, [vea Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Sugerencias de depuración

Tanto D3D11InstallHelper.dll como D3D11Install.exe se pueden crear con la configuración de depuración en Visual Studio, y estas versiones imprimirán mensajes en el mecanismo de salida de depuración Windows estándar.

## <a name="corporate-settings"></a>Configuración corporativa

El ejemplo D3D11InstallHelper está diseñado para la implementación estándar a través de Windows Update, que es el escenario más común para la instalación de un juego por parte de los consumidores. Sin embargo, muchos desarrolladores de juegos, que trabajan para publicadores y en estudios de desarrollo, lo hacen en configuraciones empresariales que tienen un servidor administrado localmente que proporciona actualizaciones de software mediante Windows Server Update Services (WSUS). En este tipo de entorno, el administrador de TI local tiene control de aprobación sobre qué actualizaciones están disponibles para los equipos dentro de la red corporativa y la versión de consumidor estándar de la actualización de KB 971644 no está disponible.

Hay tres soluciones básicas para implementar DirectX 11 en la configuración corporativa o empresarial:

-   En algunas configuraciones, es posible comprobar directamente Windows actualizar en lugar de usar el servidor WSUS administrado localmente. Por este motivo, D3D11InstallHelper admite el modificador de línea de comandos **/wu.** Sin embargo, no todas las redes corporativas permiten conexiones a los servidores públicos de Microsoft.
-   El administrador de TI local puede aprobar 971512 KB, una actualización compatible con la empresa implementada desde WSUS, que incluye la API de Direct3D 11. Esta es la única opción para que un usuario estándar obtenga la actualización de Direct3D 11 en un entorno totalmente bloqueado.
-   Como alternativa, [los 971512](https://support.microsoft.com/kb/971512/) KB se pueden instalar manualmente.

Es muy poco frecuente que el equipo de un jugador solo pueda obtener actualizaciones de un servidor WSUS administrado localmente, y solo son los desarrolladores de organizaciones grandes los que probablemente estén en estos entornos.

## <a name="related-articles"></a>Artículos relacionados

[Firewall de Windows para desarrolladores de juegos](/windows/desktop/DxTechArts/games-and-firewalls)

[Windows Explorador de juegos para desarrolladores de juegos](/windows/desktop/DxTechArts/windows-game-explorer-integration)