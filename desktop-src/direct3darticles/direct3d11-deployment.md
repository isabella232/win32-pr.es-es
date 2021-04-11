---
title: Implementación de Direct3D 11 para desarrolladores de juegos
description: En este artículo se describe cómo implementar los componentes de Direct3D 11 en un sistema si es necesario.
ms.assetid: 1fd43638-0d67-4a94-3be6-8789095f491e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd935aedee23ba731bc74e52c0773e6f02e5b5fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271333"
---
# <a name="direct3d-11-deployment-for-game-developers"></a>Implementación de Direct3D 11 para desarrolladores de juegos

En este artículo se describe cómo implementar los componentes de Direct3D 11 en un sistema si es necesario.

-   [Información general](#overview)
-   [Direct3D 11,3](#direct3d-113)
-   [Direct3D 11,2](#direct3d-112)
-   [Direct3D 11,1](#direct3d-111)
-   [D3D11InstallHelper.dll](#d3d11installhelperdll)
-   [D3D11Install.exe](#d3d11installexe)
-   [Integrar en programas de instalación](#integrating-into-installation-programs)
    -   [Integración en InstallShield](#integrating-into-installshield)
    -   [Integración en un paquete MSI](#integrating-into-an-msi-package)
-   [Sugerencias de depuración](#debugging-tips)
-   [Configuración corporativa](#corporate-settings)
-   [Artículos relacionados](#related-articles)

## <a name="overview"></a>Información general

La API de Direct3D 11 amplía la API de Direct3D 10,1 existente compatible con la representación multiproceso y la creación de recursos, el sombreador de cálculo, la teselación de hardware, la compresión de texturas de BC6H/BC7 y el modelo de sombreador de HLSL 5,0 con vinculación dinámica del sombreador. Además del componente Direct3D 11, se incluyen varios componentes gráficos adicionales en el tiempo de ejecución de DirectX 11: Direct3D 11, DXGI 1,1, niveles de características de 10level9, dispositivo de representación de software WARP10, Direct2D, DirectWrite y un nivel de compatibilidad de Direct3D 10,1 actualizado con 10level9 y WARP10. Para obtener información sobre estos y otros componentes de gráficos de Windows, vea [API de gráficos en Windows](graphics-apis-in-windows-vista.md).

Todos estos componentes gráficos nuevos están integrados en los sistemas operativos Windows 7 y Windows Server 2008 R2. La API de Direct3D 11 y los componentes relacionados también se pueden instalar en Windows Vista mediante una actualización del sistema desde Windows Update; Vea el artículo [KB 971644](https://support.microsoft.com/kb/971644)de Knowledge base. Esta actualización requiere Windows Vista y Service Pack 2. Los usuarios finales con actualizaciones automáticas habilitadas, por lo tanto, es probable que ya tengan instalados los componentes de Direct3D 11, al igual que todos los usuarios de Windows 7.

El ejemplo D3D11InstallHelper se ha diseñado para simplificar la detección de la API de Direct3D 11, instalar automáticamente la actualización del sistema si es aplicable a un equipo del usuario final y proporcionar los mensajes adecuados al usuario final en el procedimiento manual si se requiere un Service Pack más reciente.

> [!Note]  
> El compilador de HLSL (D3DCompile \* . dll) y la biblioteca de utilidades de D3DX para Direct3D 11 (D3DX11 \* . dll) no están integrados en ninguna versión del sistema operativo Windows, pero se pueden implementar como parte del instalador de una aplicación mediante la tecnología DirectSetup existente; para obtener más información sobre el uso de DirectSetup, consulte [instalación de DirectX para desarrolladores de juegos](/windows/desktop/DxTechArts/directx-setup-for-game-developers). "Effects 11" está disponible como una biblioteca de compatibilidad de código fuente compartido en [efectos para la actualización de Direct3D 11](https://github.com/Microsoft/FX11), y puede incluirlo directamente en una aplicación (como la biblioteca de utilidades DXUT). Por lo tanto, no tiene ningún requisito de redistribución adicional en tiempo de ejecución.

## <a name="direct3d-113"></a>Direct3D 11,3

Windows 10 se incluye con la API de Direct3D 11,3 integrada. Vea [características de direct3d 11,3](/windows/desktop/direct3d11/direct3d-11-3-features) para obtener una lista de las nuevas características de la API de Direct3D 11,3.

## <a name="direct3d-112"></a>Direct3D 11,2

Windows 8.1 y Windows Server 2012 R2 se incluyen con la API de Direct3D 11,2 integrada. Vea [características de direct3d 11,2](/windows/desktop/direct3d11/direct3d-11-2-features) para obtener una lista de las nuevas características de la API de Direct3D 11,2.

## <a name="direct3d-111"></a>Direct3D 11,1

Windows 8 y Windows Server 2012 vienen con la [API de Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features) integrada. La compatibilidad parcial con la API Direct3D 11,1 está disponible en Windows 7 o Windows Server 2008 R2 con la [actualización de la plataforma para Windows 7](https://support.microsoft.com/kb/2670838) instalada. Para obtener más información sobre la actualización de la plataforma para Windows 7, consulte [actualización de la plataforma para Windows 7](platform-update-for-windows-7.md).

## <a name="d3d11installhelperdll"></a>D3D11InstallHelper.dll

D3D11InstallHelper.dll hospeda la funcionalidad básica para detectar componentes de Direct3D 11 y realizar la actualización del sistema a través del servicio Windows Update, si procede. El archivo DLL no muestra ningún mensaje o cuadro de diálogo directamente.

El archivo DLL consta de los siguientes puntos de entrada:

<dl> <dt>

<span id="CheckDirect3D11Status"></span><span id="checkdirect3d11status"></span><span id="CHECKDIRECT3D11STATUS"></span>CheckDirect3D11Status
</dt> <dd>

Esta función realiza las comprobaciones necesarias y devuelve el estado de Direct3D 11 en este equipo. Esta función no requiere derechos de administrador.

-   Un estado de estado de D3D11IH \_ \_ instalado indica que Direct3D 11 ya está instalado en el equipo y está listo para su uso.
-   \_El estado \_ de D3D11IH no \_ compatible indica que esta versión de Windows no admite Direct3D 11 ni tecnologías relacionadas.
-   Un estado de estado de D3D11IH \_ \_ necesario el \_ SP más reciente \_ indica que el usuario debe instalar el Service Pack más reciente de Windows Vista.
-   Por último, un estado de \_ Estado de D3D11IH \_ requiere \_ actualización indica que el sistema no tiene Direct3D 11 instalado, pero que la actualización del sistema sí se aplica a esta versión de Windows.

</dd> <dt>

<span id="DoUpdateForDirect3D11"></span><span id="doupdatefordirect3d11"></span><span id="DOUPDATEFORDIRECT3D11"></span>DoUpdateForDirect3D11
</dt> <dd>

Esta función usa la API de Windows Update para realizar la actualización del sistema para instalar Direct3D 11 en este sistema, si procede. Tenga en cuenta que esta función requiere conectividad de red para Windows Update para que se realice correctamente, así como derechos administrativos. Toma una función de devolución de llamada de progreso opcional y un puntero de contexto de usuario, y devuelve un código de resultado final cuando se completa.

-   El \_ resultado de resultado correcto de D3D11IH \_ indica que la actualización del sistema se aplicó y está lista para su uso, mientras \_ \_ que el reinicio del resultado correcto de D3D11IH \_ indica que la actualización del sistema requiere que el equipo se reinicie antes de completarse. Tenga en cuenta que esta función no programa el reinicio del sistema.
-   \_El resultado \_ de D3D11IH no \_ compatible indica que la actualización del sistema no se aplica a esta versión de Windows. Este resultado no debería producirse si solo se llama a esta función después de obtener un \_ Estado de D3D11IH que \_ requiere el \_ Estado de actualización de CheckDirect3D11Status.
-   El resultado de la \_ actualización de resultados de D3D11IH \_ \_ no \_ encontrada indica que no se encontró el paquete de actualización del sistema en los servidores de Windows Update.
-   Si se produce un error en la descarga o la instalación del Windows Update, se producirá un error en la descarga de la actualización de resultados de D3D11IH \_ \_ o se \_ \_ \_ \_ \_ \_ devolverá un error de instalación de actualización de resultados D3D11IH
-   Si se devuelve un error de conectividad de red desde la API de Windows Update, \_ se devuelve el resultado del error del servicio D3D11IH de resultados de \_ Wu \_ \_ , lo que indica que el problema podría ser intermitente o estar relacionado con la configuración de la red o del firewall. Es posible que vuelva a intentar la función de actualización.

</dd> </dl>

Para obtener más información sobre la API de Windows Update, consulte [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client).

## <a name="d3d11installexe"></a>D3D11Install.exe

> [!Note]  
> D3D11Install.exe requiere que D3D11InstallHelper.dll se ejecute.

D3D11Install.exe es una herramienta para usar D3D11InstallHelper.dll como instalador independiente completado con mensajes de usuario final y de interfaz de usuario, así como para actuar como ejemplo para el uso correcto del archivo DLL. El proceso finaliza con un 0 si ya está instalado Direct3D 11, si la actualización del sistema se aplica correctamente sin requerir un reinicio del sistema, si se requiere una instalación del Service Pack o si el equipo no admite Direct3D 11. Se devuelve 1 si la actualización del sistema se aplica correctamente y requiere el reinicio del sistema para completarse. Se devuelve un 2 para otras condiciones de error. Tenga en cuenta que este archivo ejecutable requiere derechos de administrador para ejecutarse y que tiene un manifiesto que solicita la elevación cuando se ejecuta en Windows Vista o Windows 7 con UAC habilitado. D3D11Install.exe puede usarse como una herramienta independiente para implementar la actualización de Direct3D 11, o bien se puede usar directamente mediante instaladores.

Admite los siguientes modificadores de línea de comandos:

<dl> <dt>

<span id="_quiet__"></span><span id="_QUIET__"></span>/Quiet 
</dt> <dd>

No muestra ningún mensaje, mensaje, cuadro de diálogo de progreso o mensajes de error.

</dd> <dt>

<span id="_passive__"></span><span id="_PASSIVE__"></span>/Passive 
</dt> <dd>

No muestra ningún mensaje, mensaje o mensaje de error, pero mostrará el cuadro de diálogo de progreso.

</dd> <dt>

<span id="_minimal__"></span><span id="_MINIMAL__"></span>/minimal 
</dt> <dd>

Muestra solo los mensajes mínimos.

</dd> <dt>

<span id="_y__"></span><span id="_Y__"></span>/y 
</dt> <dd>

Suprime la solicitud de confirmación de la instalación de la actualización, si es necesario y aplicable, para una instalación estándar y mínima.

</dd> <dt>

<span id="_langid_decimal__"></span><span id="_LANGID_DECIMAL__"></span>/langid decimal 
</dt> <dd>

Fuerza el código de identificador de idioma que se va a usar al mostrar los mensajes del usuario final y los recursos del cuadro de diálogo. El valor predeterminado es 1024, que utiliza la configuración de idioma predeterminado del sistema.

</dd> <dt>

<span id="_wu__"></span><span id="_WU__"></span>/wu 
</dt> <dd>

Fuerza el uso de Windows Update en lugar del valor predeterminado del sistema, que puede ser Windows Server Update Services (WSUS) que se ejecuta en un servidor administrado u otra configuración no estándar.

</dd> </dl>

## <a name="integrating-into-installation-programs"></a>Integrar en programas de instalación

Con el fin de que sea compatible con la instalación sencilla, el [requisito técnico 3,1 para juegos para Windows](/windows/desktop/DxTechArts/games-for-windows-technical-requirements-1-1-0006), tiene que tener cuidado para que los mensajes del usuario final se presenten al principio del proceso de instalación y para asegurarse de que no haya varias peticiones de elevación relacionadas con UAC. Existen tres opciones básicas para lograr este objetivo:

1.  El método más básico consiste en ejecutar el D3D11Install.exe con el modificador de línea de comandos **/minimal**. Esto se debe hacer al principio en el instalador Q&A, y la instalación debe usar el valor devuelto de 1 para indicar que se debe programar un reinicio al final de la instalación. La ejecución del programa requiere derechos administrativos.
2.  Use D3D11InstallHelper.dll directamente para detectar la necesidad de la actualización, proporcionando los mensajes de usuario final necesarios para el estado D3D11IH \_ status \_ \_ \_ require el SP más reciente, donde la resolución requiere operaciones manuales de usuario. El resultado del estado de \_ D3D11IH \_ no \_ admitido se puede usar para controlar la instalación de los recursos relacionados con Direct3D 11, o como una condición de error para las aplicaciones de Direct3D 11 únicamente, pero no es necesariamente un mensaje de usuario final útil. Para el estado D3D11IH \_ status \_ requires \_ Update, el instalador puede usar directamente el punto de entrada de dll DoUpdateForDirect3D11 para realizar la actualización y administrar los distintos mensajes de usuario final. Se pueden encontrar ejemplos de mensajes estándar examinando el cuadro de diálogo D3D11Install.exe y los recursos de tabla de cadenas. El punto de entrada de actualización requiere derechos de administrador.
3.  Un enfoque híbrido consiste en comprobar el estado con D3D11InstallHelper.dll y, en el caso del código de estado D3D11IH \_ status require el estado de la \_ \_ versión más reciente de \_ SP o D3D11IH, es necesario \_ \_ \_ actualizar, D3D11Install.exe se puede ejecutar con los modificadores **/minimal** y **/y** para mostrar el cuadro de diálogo o realizar la actualización, según sea necesario. Estos pasos deben realizarse al principio del proceso de instalación, normalmente inmediatamente después de la p&A, y la ejecución del archivo ejecutable requiere derechos administrativos.

### <a name="integrating-into-installshield"></a>Integración en InstallShield

La administración de la implementación de Direct3D 11 desde el InstallScript de InstallShield se realiza fácilmente mediante el ejemplo D3D11InstallHelper. Los pasos necesarios para la integración con InstallShield mediante InstallScript son los siguientes (con el método 3, que se describe en la sección anterior):

1.  Abra un proyecto de InstallScript en el editor de InstallShield.
2.  Agregue D3D11InstallHelper.dll y D3D11Install.exe al proyecto en **archivos auxiliares**.

    **Para agregar los archivos al proyecto de InstallShield**

    1.  En la pestaña **Diseñador de instalación** , haga clic en **compatibilidad archivos/cartelera** en **comportamiento y lógica** en el panel de navegación de la izquierda.
    2.  Haga clic en **idioma independiente**, haga clic con el botón derecho en la ventana **archivos** y seleccione **insertar archivos**. Vaya a agregar D3D11InstallHelper.dll y D3D11Install.exe. La ubicación predeterminada de estos archivos es: ejemplos raíz del SDK \\ \\ C++ \\ Misc \\ bin \\ x86

3.  En el explorador de InstallScript, haga clic en el archivo InstallScript (normalmente Setup. RUL) que llamará al archivo DLL o ejecutable, que se encuentra en **comportamiento y lógica** en el panel de navegación de la izquierda.
4.  Pegue el siguiente InstallScript en el archivo cerca de la parte superior:

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

5.  Pegue el siguiente InstallScript en el archivo en la función **OnFirstUIBefore** , justo antes de que devuelva 0:

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

La siguiente es una descripción de alto nivel de los pasos necesarios para integrar la implementación de Direct3D 11 mediante acciones personalizadas de MSI (con el método 3, descrito anteriormente en este tema):

1.  Agregue una propiedad a la tabla de propiedades MSI denominada **RelativePathToD3D11IH** que contiene la ruta de acceso relativa que se va a D3D11Install.exe y D3D11InstallHelper.dll durante la instalación (normalmente se encuentra en la imagen multimedia). Esto también establece una propiedad de MSI D3D11IH \_ status en el estado devuelto por CheckDirect3D11Status (una propiedad de cadena igual al símbolo de enumeración o "error").
2.  Después de la acción CostFinalize, llame a la función de D3D11InstallHelper.dll **SetD3D11InstallMSIProperties** como una acción personalizada inmediata para establecer las propiedades MSI adecuadas para las demás acciones personalizadas.
3.  Tras la instalación, desencadene una acción personalizada diferida después de la acción InstallFiles que llama a la función D3D11InstallHelper.dll **DoD3D11InstallUsingMSI**. La acción personalizada debe establecer la marca msidbCustomActionTypeNoImpersonate para que se ejecute en un contexto con privilegios elevados.
4.  Después de la acción InstallFinalize, llame a la función de D3D11InstallHelper.dll **FinishD3D11InstallUsingMSI** como una acción personalizada inmediata para controlar el código de resultado de la solicitud de reinicio correcta, si es necesario.

Este procedimiento se describe en detalle en las siguientes instrucciones, que describen un proceso que se puede realizar mediante un editor MSI, como el [Editor Orca](/windows/desktop/Msi/orca-exe). Algunos editores de MSI tienen asistentes que simplifican algunos de estos pasos de configuración.

**Para configurar un paquete MSI para la integración con D3D11InstallHelper.dll**

1.  Abra el paquete MSI en orca.
2.  Agregue la fila que se muestra en la tabla siguiente a la tabla binaria del paquete MSI.

    | Nombre    | Datos                                         |
    |---------|----------------------------------------------|
    | D3D11IH | Ruta de acceso al archivo DLL \\D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > Este archivo se incrustará en el paquete MSI, por lo que debe realizar este paso cada vez que vuelva a compilar D3D11InstallHelper.dll.

     

3.  Agregue las filas que se muestran en la tabla siguiente a la tabla CustomAction en el paquete MSI. 

    | Acción              | Tipo                                                                                                                                                                   | Source  | Destino                       |
    |---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|------------------------------|
    | Direct3D11SetProps  | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11IH | SetD3D11InstallMSIProperties |
    | Direct3D11DoInstall | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137 | D3D11IH | DoD3D11InstallUsingMSI       |
    | Direct3D11Finish    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11IH | FinishD3D11InstallUsingMSI   |

    

     

4.  Agregue los valores que se muestran para Action, condition y Sequence en la tabla siguiente a la tabla InstallExecuteSequence del paquete MSI. 

    | Acción              | Condición     | Secuencia | Notas                                                                                                                                                          |
    |---------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Direct3D11SetProps  |               | 1016     | El número de secuencia coloca la acción poco después de CostFinalize.                                                                                                 |
    | Direct3D11DoInstall | NO instalado | 4004     | Esta acción personalizada solo se producirá durante una nueva instalación para todos los usuarios. El número de secuencia coloca la acción después de InstallFiles y después de la reversión. |
    | Direct3D11Finish    |               | 6615     | El número de secuencia coloca la acción poco después de InstallFinalize.                                                                                              |

    

     

5.  Agregue la fila que se muestra en la tabla siguiente a la tabla de **propiedades** del paquete MSI. 

    | Propiedad              | Value                                                                        |
    |-----------------------|------------------------------------------------------------------------------|
    | RelativePathToD3D11IH | Ruta de acceso relativa del archivo que contiene D3D11Install.exe y D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > La ubicación especificada por la ruta de acceso es relativa a la ubicación especificada por la ruta de instalación, por ejemplo, "Redist \\ ".

     

6.  Guarde el paquete MSI. Para obtener información más detallada sobre los paquetes MSI y Windows Installer, vea [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Sugerencias de depuración

Tanto D3D11InstallHelper.dll como D3D11Install.exe pueden compilarse con la configuración de depuración en Visual Studio, y estas versiones imprimirán mensajes en el mecanismo estándar de salida de depuración de Windows.

## <a name="corporate-settings"></a>Configuración corporativa

El ejemplo D3D11InstallHelper está diseñado para la implementación estándar a través de Windows Update, que es el escenario más común para la instalación de un juego por parte de los consumidores. Sin embargo, muchos desarrolladores de juegos, que trabajan para publicadores y en estudios de desarrollo, lo hacen en la configuración empresarial que tiene un servidor administrado localmente que proporciona actualizaciones de software mediante la tecnología de Windows Server Update Services (WSUS). En este tipo de entorno, el administrador de ti local tiene el control de aprobación sobre qué actualizaciones están disponibles para los equipos de la red corporativa, y la versión de consumidor estándar de Update KB 971644 no está disponible.

Hay tres soluciones básicas para la implementación de DirectX 11 en la configuración corporativa o empresarial:

-   En algunas configuraciones, es posible comprobar directamente Windows Update en lugar de usar el servidor WSUS administrado localmente. Por esta razón, D3D11InstallHelper admite el modificador de línea de comandos **/Wu** . Sin embargo, no todas las redes corporativas permiten conexiones a los servidores públicos de Microsoft.
-   El administrador de ti local puede aprobar KB 971512, una actualización compatible con la empresa implementada desde WSUS, que incluye la API de Direct3D 11. Esta es la única opción para que un usuario estándar obtenga la actualización de Direct3D 11 en un entorno que está totalmente bloqueado.
-   Como alternativa, se puede instalar de forma manual [KB 971512](https://support.microsoft.com/kb/971512/) .

Es muy poco probable que el equipo de un jugador solo pueda obtener actualizaciones de un servidor WSUS administrado localmente y que sea solo desarrolladores en organizaciones de gran tamaño que probablemente estén en dichos entornos.

## <a name="related-articles"></a>Artículos relacionados

[Firewall de Windows para desarrolladores de juegos](/windows/desktop/DxTechArts/games-and-firewalls)

[Explorador de juegos de Windows para desarrolladores de juegos](/windows/desktop/DxTechArts/windows-game-explorer-integration)