---
title: Instalación de DirectX para desarrolladores de juegos
description: Este artículo pretende abordar algunas de las preguntas comunes sobre el tiempo de ejecución de DirectX y el uso de DirectSetup para instalar DirectX.
ms.assetid: 2ab439be-8d99-bcf8-89af-d4274e044c88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c0faf346bd8793e61a89128ce573e29b7a8267
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078230"
---
# <a name="directx-installation-for-game-developers"></a>Instalación de DirectX para desarrolladores de juegos

Este artículo pretende abordar algunas de las preguntas comunes sobre el tiempo de ejecución de DirectX y el uso de DirectSetup para instalar DirectX.

-   [Tiempo de ejecución de DirectX](#directx-runtime)
-   [Número de versión de DirectX](#directx-version-number)
-   [Bibliotecas de DirectX](#directx-libraries)
-   [Instalación de DirectX por el instalador del juego](#installation-of-directx-by-the-games-installer)
-   [Paquetes de instalación pequeños](#small-installation-packages)
-   [Implementación interna del tiempo de ejecución de depuración de DirectX](#internal-deployment-of-the-debug-directx-runtime)

> [!IMPORTANT]
> El SDK de DirectX heredado está al final del ciclo de vida, pero sigue estando disponible para admitir juegos, tutoriales y proyectos antiguos. Los proyectos nuevos no deberían usarlo. El uso del SDK de DirectX heredado requiere el uso de DirectSetup en desuso para los componentes como D3DX9, D3DX10, D3DX11, XAudio 2,7, XInput 1,3 y XACT. Para obtener más información sobre el estado actual del SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md)y la entrada de blog [no para la configuración directa](https://walbourn.github.io/not-so-direct-setup/).

## <a name="directx-runtime"></a>Tiempo de ejecución de DirectX

El tiempo de ejecución de DirectX consta de componentes principales y componentes opcionales.

Los componentes principales, como Direct3D y DirectInput, se consideran parte del sistema operativo. Los componentes principales de DirectX 9.0 c no han cambiado desde la actualización del 2004 de verano del SDK de DirectX, y coinciden con lo que se lanzó con Microsoft Windows XP SP2, Windows XP Pro x64 Edition y Windows Server 2003 SP1. Windows Vista incluye DirectX 10, que es compatible con Windows Display Driver Model (WDDM) y Direct3D 10. x. Windows 7 y Windows Vista (consulte [KB971644](https://support.microsoft.com/kb/971644)) admiten DirectX 11, que admite Direct3D 11, Direct2D, DirectWrite, el dispositivo de representación de software WARP10 y los niveles de características 10level9. Consulte [API de gráficos en Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista) para obtener más información.

Los componentes opcionales se publican en las actualizaciones del SDK de DirectX e incluyen D3DX, XACT, XAudio2, XINPUT, DirectX administrado y otros componentes de este tipo. Muchos de los componentes opcionales se actualizan periódicamente para integrar los comentarios de los clientes y exponer nuevas características.

## <a name="directx-version-number"></a>Número de versión de DirectX

El número de versión de DirectX, como 9.0 c, solo hace referencia a la versión de los componentes principales, como Direct3D, DirectInput o DirectSound. Este número no cubre las versiones de los distintos componentes opcionales que se publican en el SDK de DirectX, como D3DX, XACT, XINPUT, etc.

Por lo general, el número de versión de DirectX no es significativo excepto como referencia rápida a los bits principales en tiempo de ejecución. Este número no debe usarse para comprobar si el tiempo de ejecución de DirectX correcto ya está instalado, ya que no tiene en cuenta los componentes opcionales de DirectX.

## <a name="directx-libraries"></a>Bibliotecas de DirectX

En el pasado, los componentes opcionales del SDK de DirectX, incluido D3DX, se publicaron como bibliotecas estáticas. Sin embargo, ahora se publican como bibliotecas de tipo dinámico (DLL) debido al aumento de la demanda de mejores prácticas de seguridad. Los archivos dll permiten el mantenimiento del código publicado anteriormente. Si estos componentes se han implementado como bibliotecas estáticas, no habrá forma de que Microsoft solucione los problemas de seguridad que se encuentran después de la versión.

A medida que se agregan o se cambian características en los componentes opcionales, también se cambian los nombres de los archivos dll correspondientes para asegurarse de que no se producen regresiones en los juegos existentes que usan componentes publicados. Los archivos DLL para cada componente en directo en paralelo y los desarrolladores de juegos pueden elegir exactamente la versión de DLL que el juego usa vinculando a la biblioteca de importación correspondiente.

A la vez que se asegura de que los archivos DLL se instalan en un sistema no es tan fácil como vincular a bibliotecas estáticas, se han realizado algunos cambios en el SDK de DirectX para solucionar el problema del modelo de DLL:

-   DirectX Redistributable puede configurarse para que contenga solo los componentes que requiere la aplicación para minimizar los tamaños de distribución y medios.
-   La carpeta redistribuible, archivos \\ de programa \\ de DirectX SDK Redist \\ , contiene un archivo contenedor (. cab) para cada posible componente opcional, por lo que no tiene que preparar un SDK más antiguo para encontrarlos.
-   La instalación del propio SDK instala cada componente opcional posible.
-   Un redistribuible de DirectX que contiene todos los componentes opcionales está disponible como un instalador basado en Web y como un paquete descargable; para obtener más información, vea el centro para desarrolladores de DirectX ([DirectX](/previous-versions/windows/apps/hh452744(v=win.10))).

## <a name="installation-of-directx-by-the-games-installer"></a>Instalación de DirectX por el instalador del juego

> [!Note]  
> Vea [implementación de Direct3D 11 para desarrolladores de juegos](/windows/desktop/direct3darticles/direct3d11-deployment).

 

A continuación se muestran los procedimientos recomendados para agregar la instalación de DirectX al instalador de un juego:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Término</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Install_the_redistributable_components_every_time.__"></span><span id="install_the_redistributable_components_every_time.__"></span><span id="INSTALL_THE_REDISTRIBUTABLE_COMPONENTS_EVERY_TIME.__"></span>Instale los componentes redistribuibles cada vez. <br/></td>
<td>El proceso de instalación de un juego debe instalar los componentes redistribuibles de DirectX durante cada instalación única sin permitir que los usuarios se destaquen. Si permite la retirada, algunos usuarios adivinarán que no lo necesitan y, si realmente lo hacen, el juego no se ejecutará. <br/></td>
</tr>
<tr class="even">
<td><span id="Let_the_DirectX_installer_check_for_optional_components.__"></span><span id="let_the_directx_installer_check_for_optional_components.__"></span><span id="LET_THE_DIRECTX_INSTALLER_CHECK_FOR_OPTIONAL_COMPONENTS.__"></span>Deje que el instalador de DirectX Compruebe los componentes opcionales. <br/></td>
<td>No asuma que los componentes opcionales más recientes ya están instalados en un sistema, porque Windows Update y los Service Pack no proporcionan ninguno de los componentes opcionales de DirectX. Debe instalar el tiempo de ejecución de DirectX ejecutando dxsetup.exe directamente o llamando a DirectSetup. <br/></td>
</tr>
<tr class="odd">
<td><span id="Set_up_silently.__"></span><span id="set_up_silently.__"></span><span id="SET_UP_SILENTLY.__"></span>Configuración silenciosa. <br/></td>
<td>Inicie el programa de instalación en modo silencioso para que los usuarios no omitan accidentalmente la actualización del tiempo de ejecución de DirectX. Puede hacerlo iniciando dxsetup.exe con el siguiente comando: <br/>
<pre class="syntax" data-space="preserve"><code>   path-to-redistributable\dxsetup.exe /silent</code></pre>
o bien llamando a DirectSetup y sin mostrar ninguna interfaz de usuario. <br/></td>
</tr>
<tr class="even">
<td><span id="Combine_EULA_acceptances.__"></span><span id="combine_eula_acceptances.__"></span><span id="COMBINE_EULA_ACCEPTANCES.__"></span>Combine las aceptaciones de los términos de licencia. <br/></td>
<td>Si solicita al usuario que acepte un CLUF, combínelo con la solicitud de aceptación del CLUF de DirectX al instalar en modo silencioso, de modo que la solicitud de aceptación de los términos de licencia se produzca una sola vez. La solicitud debe realizarse antes de instalar cualquier cosa, de modo que si el usuario no la acepta, no acabe con una instalación parcial y con errores. <br/></td>
</tr>
<tr class="odd">
<td><span id="Just_run_dxsetup_or_call_DirectSetup.__"></span><span id="just_run_dxsetup_or_call_directsetup.__"></span><span id="JUST_RUN_DXSETUP_OR_CALL_DIRECTSETUP.__"></span>Basta con ejecutar DxSetup o llamar a DirectSetup. <br/></td>
<td>Dado que el número de versión de DirectX no hace referencia a ninguno de los componentes principales de DirectX, no active una versión instalada antes de ejecutar dxsetup.exe o llamando a DirectSetup. Además, no Compruebe la existencia de un archivo para probar si ya está instalado un componente opcional, ya que normalmente no determinará correctamente cuando un componente existe pero necesita actualizarse. Sin embargo, el paquete de instalación de DirectX lo determinará rápidamente y realizará la acción correcta. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="small-installation-packages"></a>Paquetes de instalación pequeños

Puede crear paquetes de instalación más pequeños para DirectX quitando el contenido de la carpeta redistribuible de DirectX hasta el conjunto mínimo de archivos necesario para que el instalador funcione y conservando cualquier componente adicional que use el juego.

En función de las especificaciones mínimas, es posible que no necesite incluir los archivos. cab básicos de DirectX 9.0 c en la carpeta redistribuible de los medios de instalación. Una gran mayoría de las instalaciones de Windows XP tienen Service Pack 2, que incluye los componentes básicos de DirectX 9.0 c, por lo que la operación de instalación de DirectX será muy rápida y no requerirá un reinicio. El paquete más pequeño que se puede crear es aproximadamente de 3 MB y se puede comprimir aproximadamente a la mitad del tamaño. Un paquete como este contiene una versión de la DLL de D3DX y requiere que ya esté presente DirectX 9.0 c.

El conjunto mínimo de archivos necesarios para compilar un paquete redistribuible son los siguientes archivos, que se encuentran en la carpeta Redist del SDK de DirectX (archivos de programa \\ DirectX SDK \\ Redist \) :

-   dxsetup.exe
-   dsetup32.dll
-   dsetup.dll
-   dxupdate.cab

Agregue estos archivos. cab para los componentes que desea instalar. Si necesita que los usuarios de la aplicación ya tengan DirectX 9.0 c, no es necesario incluir DirectX.cab o dxnt.cab, que constituyen la mayor parte del espacio necesario. DirectX.cab solo es necesario para Windows 98 y Windows ME; dxnt.cab solo es necesario para Windows 2000, Windows XP y Windows XP SP1; y dxdllreg \_x86.cab solo es necesario para windows 2000, Windows XP RTM, Windows XP SP1 y Windows Server 2003 RTM. Además, si no hace uso de DirectShow o supone que ya está instalado, puede omitir BDA.cab, BDANT.cab y BDAXP.cab.

> [!Note]  
> Puede suponer que los usuarios de la aplicación ya tienen DirectX 9.0 c si se instaló con una versión anterior de la aplicación, obliga a los usuarios a actualizar manualmente a través del instalador web o asume que tienen Windows XP SP2 o posterior.

 

Siguiendo con este ejemplo, si solo usa la versión de 32 bits de D3DX para el 2006 de abril, puede Agregar Apr2006 \_ d3dx9 \_ 30 \_x86.cab. Si usa la versión de 32 bits de agosto de 2006 32 bits de XINPUT, agregue Aug2006 \_ XINPUT \_x86.cab.

Si tiene una aplicación nativa de 64 bits, deberá agregar las \_ versiones x64. Sin embargo, si tiene una aplicación de 32 bits que se ejecuta en un sistema operativo de 64 bits, las versiones de 32 bits de los archivos dll funcionarán.

Después, puede distribuir este paquete de archivos e iniciar DirectSetup en modo silencioso o ejecutar dxsetup.exe en el shell de comandos en modo silencioso. Recuerde no proteger este paquete mediante la comprobación de la versión de los archivos y asegúrese de que los usuarios no pueden no participar en la ejecución del programa de instalación de DirectX. Cualquiera de estos eventos crea un proceso de instalación de fallible.

## <a name="internal-deployment-of-the-debug-directx-runtime"></a>Implementación interna del tiempo de ejecución de depuración de DirectX

Los tiempos de ejecución de depuración de los componentes de DirectX se instalan cuando se instala el SDK de DirectX, pero la instalación del SDK en cada equipo de prueba puede ser difícil. Debe diseñar el proceso de instalación para copiar los archivos dll de tiempo de ejecución de depuración de los archivos de programa \\ Microsoft DirectX SDK \\ Developer Runtime \\ Architecture \\ en Windows \\ system32 \\ o en la carpeta del juego.

Sin embargo, se recomienda encarecidamente no copiar simplemente los archivos dll de tiempo de ejecución publicados, ya que es fácil olvidarse de quitarlos para el producto final. En su lugar, coloque los archivos de instalación de DirectX en una carpeta compartida y ejecute el programa de instalación de forma silenciosa desde la carpeta compartida.

## <a name="desktop-bridge-applications"></a>Aplicaciones de puente de escritorio 

Las aplicaciones de puente de escritorio que usan D3DX9, D3DX10, D3DX11, XAudio 2,7, XInput 1,3 o XACT deben descargar [Microsoft. DirectX. x86](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x86.appx) o el marco [Microsoft. DirectX. x64](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x64.appx) para implementar estos componentes en paralelo de DirectX SDK. Como alternativa, puede quitar todas las dependencias &mdash; (consulte la [Guía del desarrollador para la versión redistribuible de XAudio 2,9](../xaudio2/xaudio2-redistributable.md)y las entradas de blog que [viven sin D3DX](https://walbourn.github.io/living-without-d3dx/) y [XInput y Windows 8](https://walbourn.github.io/xinput-and-windows-8/)).