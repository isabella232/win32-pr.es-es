---
title: Instalación de DirectX para desarrolladores de juegos
description: Este artículo está pensado para abordar algunas de las preguntas comunes sobre el entorno de ejecución de DirectX y el uso de DirectSetup para instalar DirectX.
ms.assetid: 2ab439be-8d99-bcf8-89af-d4274e044c88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0509084232f1dcfe63a7d956516aa723f8cd724b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477291"
---
# <a name="directx-installation-for-game-developers"></a>Instalación de DirectX para desarrolladores de juegos

Este artículo está pensado para abordar algunas de las preguntas comunes sobre el entorno de ejecución de DirectX y el uso de DirectSetup para instalar DirectX.

-   [DirectX Runtime](#directx-runtime)
-   [Número de versión de DirectX](#directx-version-number)
-   [Bibliotecas de DirectX](#directx-libraries)
-   [Instalación de DirectX mediante el instalador del juego](#installation-of-directx-by-the-games-installer)
-   [Paquetes de instalación pequeños](#small-installation-packages)
-   [Implementación interna del entorno de ejecución de DirectX de depuración](#internal-deployment-of-the-debug-directx-runtime)

> [!IMPORTANT]
> El SDK de DirectX heredado está al final del ciclo de vida, pero sigue estando disponible para admitir juegos, tutoriales y proyectos antiguos. Los proyectos nuevos no deben usarlo. El uso del SDK de DirectX heredado requiere el uso de DirectSetup en desuso para componentes como D3DX9, D3DX10, D3DX11, XAudio 2.7, XInput 1.3 y XACT. Para obtener más información sobre el estado actual del SDK de DirectX, consulte ¿Dónde está el [SDK de DirectX?](../directx-sdk--august-2009-.md)y la entrada de blog [Not So Direct Setup](https://walbourn.github.io/not-so-direct-setup/).

## <a name="directx-runtime"></a>DirectX Runtime

El entorno de ejecución de DirectX consta de componentes principales y componentes opcionales.

Los componentes principales, como Direct3D y DirectInput, se consideran parte del sistema operativo. Los componentes principales de DirectX 9.0c no han cambiado desde la actualización del verano de 2004 del SDK de DirectX y coinciden con lo que se publicó con Microsoft Windows XP SP2, Windows XP Pro x64 Edition y Windows Server 2003 SP1. Windows Vista incluye DirectX 10, que admite Windows Display Driver Model (WDDM) y Direct3D 10.x. Windows 7 y Windows Vista (consulte [KB971644)](https://support.microsoft.com/kb/971644)admiten DirectX 11, que admite Direct3D 11, Direct2D, DirectWrite, el dispositivo de representación de software WARP10 y los niveles de características 10level9. Consulte [API de gráficos en Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista) para obtener más detalles.

Los componentes opcionales se lanzan en las actualizaciones del SDK de DirectX e incluyen D3DX, XACT, XAudio2, XINPUT, Managed DirectX y otros componentes de este tipo. Muchos de los componentes opcionales se actualizan periódicamente para integrar los comentarios de los clientes y exponer nuevas características.

## <a name="directx-version-number"></a>Número de versión de DirectX

El número de versión de DirectX, como 9.0c, solo hace referencia a la versión de los componentes principales, como Direct3D, DirectInput o Direct Sound. Este número no cubre las versiones de los distintos componentes opcionales que se lanzan en el SDK de DirectX, como D3DX, XACT, XINPUT, entre otros.

Por lo general, el número de versión de DirectX no es significativo, excepto como referencia rápida a los bits en tiempo de ejecución principales. Este número no debe usarse para comprobar si el entorno de ejecución de DirectX correcto ya está instalado, ya que no tiene en cuenta los componentes opcionales de DirectX.

## <a name="directx-libraries"></a>Bibliotecas de DirectX

En el pasado, los componentes opcionales del SDK de DirectX, incluido D3DX, se publicaron como bibliotecas estáticas. Sin embargo, ahora se lanzan como bibliotecas de tipo dinámico (DLL) debido al aumento de la demanda de mejores prácticas de seguridad. Los archivos DLL permiten el mantenimiento del código publicado anteriormente. Si estos componentes se implementaron como bibliotecas estáticas, no habría ninguna manera de que Microsoft solucionara los problemas de seguridad encontrados después de la versión.

A medida que las características se agregan o cambian a los componentes opcionales, los nombres de los archivos DLL correspondientes también se cambian para asegurarse de que no se produce ninguna regresión en los juegos existentes que usan componentes publicados. Los archivos DLL de cada componente están en directo en paralelo y los desarrolladores de juegos pueden elegir exactamente qué versión de DLL usa el juego mediante la vinculación a la biblioteca de importación correspondiente.

Aunque asegurarse de que los archivos DLL están instalados en un sistema no es tan fácil como simplemente vincular a bibliotecas estáticas, se han realizado algunos cambios en el SDK de DirectX para solucionar el problema del modelo dll:

-   DirectX redistributable se puede configurar para contener solo los componentes que la aplicación requiere para minimizar los tamaños de distribución y multimedia.
-   La carpeta redistribuible, Program Files DirectX SDK Redist , ahora contiene un archivo \\ \\ de archivador (.cab) para cada componente opcional posible, por lo que no tiene que profundizar en un SDK anterior para \\ encontrarlos.
-   Al instalar el propio SDK, se instalan todos los componentes opcionales posibles.
-   DirectX redistribuible que contiene todos los componentes opcionales está disponible como instalador basado en web y como paquete descargable. Consulte el Centro para desarrolladores de DirectX[(DirectX)](/previous-versions/windows/apps/hh452744(v=win.10))para obtener más información.

## <a name="installation-of-directx-by-the-games-installer"></a>Instalación de DirectX mediante el instalador del juego

> [!Note]  
> Consulte [Implementación de Direct3D 11 para desarrolladores de juegos.](/windows/desktop/direct3darticles/direct3d11-deployment)

 

Estos son los procedimientos recomendados para agregar la instalación de DirectX al instalador de un juego:




| Término | Descripción | 
|------|-------------|
| <span id="Install_the_redistributable_components_every_time.__"></span><span id="install_the_redistributable_components_every_time.__"></span><span id="INSTALL_THE_REDISTRIBUTABLE_COMPONENTS_EVERY_TIME.__"></span>Instale los componentes redistribuibles cada vez. <br /> | El proceso de instalación de un juego debe instalar los componentes redistribuibles de DirectX durante cada instalación sin permitir que los usuarios no lo usen. Si permite la exclusión, algunos usuarios adivinarán que no lo necesitan y, si realmente lo hacen, el juego no se ejecutará. <br /> | 
| <span id="Let_the_DirectX_installer_check_for_optional_components.__"></span><span id="let_the_directx_installer_check_for_optional_components.__"></span><span id="LET_THE_DIRECTX_INSTALLER_CHECK_FOR_OPTIONAL_COMPONENTS.__"></span>Deje que el instalador de DirectX compruebe si hay componentes opcionales. <br /> | No suponga que los componentes opcionales más recientes ya están instalados en un sistema, ya que Windows Update y Service Pack no proporcionan ninguno de los componentes opcionales de DirectX. Debe instalar el entorno de ejecución de DirectX ejecutando dxsetup.exe directamente o llamando a DirectSetup. <br /> | 
| <span id="Set_up_silently.__"></span><span id="set_up_silently.__"></span><span id="SET_UP_SILENTLY.__"></span>Configurar en modo silencioso. <br /> | Inicie la instalación en modo silencioso para que los usuarios no omita accidentalmente la actualización del entorno de ejecución de DirectX. Para ello, inicie dxsetup.exe con el siguiente comando: <br /><pre class="syntax" data-space="preserve"><code>   path-to-redistributable\dxsetup.exe /silent</code></pre>o llamando a DirectSetup y sin mostrar ninguna interfaz de usuario. <br /> | 
| <span id="Combine_EULA_acceptances.__"></span><span id="combine_eula_acceptances.__"></span><span id="COMBINE_EULA_ACCEPTANCES.__"></span>Combinar las aceptaciones del CLUF. <br /> | Si solicita al usuario que acepte un CLUF, combine esto con la solicitud de aceptación del CLUF de DirectX al realizar la instalación en modo silencioso para que la solicitud de aceptación de las EULA se haga una sola vez. Las solicitudes deben producirse antes de instalar nada para que, si el usuario no acepta, no termine con una instalación parcial y con errores. <br /> | 
| <span id="Just_run_dxsetup_or_call_DirectSetup.__"></span><span id="just_run_dxsetup_or_call_directsetup.__"></span><span id="JUST_RUN_DXSETUP_OR_CALL_DIRECTSETUP.__"></span>Simplemente ejecute dxsetup o llame a DirectSetup. <br /> | Dado que el número de versión de DirectX no hace referencia a nada excepto a los componentes principales de DirectX, no compruebe una versión instalada antes de ejecutar dxsetup.exe o llamar a DirectSetup. Además, no compruebe la existencia de un archivo para probar si ya está instalado un componente opcional, ya que normalmente no determinará correctamente cuándo existe un componente, pero debe actualizarse. Sin embargo, el paquete de instalación de DirectX lo determinará rápidamente y realizará la acción correcta. <br /> | 




 

## <a name="small-installation-packages"></a>Paquetes de instalación pequeños

Puede crear paquetes de instalación más pequeños para DirectX quitando el contenido de la carpeta redistribuible de DirectX al conjunto mínimo de archivos necesarios para que el instalador funcione y conservando los componentes adicionales que usa el juego.

En función de las especificaciones mínimas, es posible que ni siquiera necesite incluir los archivos principales del archivador de DirectX 9.0c en la carpeta redistribuible del medio de instalación. Una gran mayoría de las instalaciones de Windows XP tienen Service Pack 2, que incluye los componentes principales de DirectX 9.0c, por lo que la operación de instalación de DirectX será muy rápida y no requerirá un reinicio. El paquete más pequeño que se puede crear es de aproximadamente 3 MB y se puede comprimir a aproximadamente la mitad de ese tamaño. Un paquete como este contiene una versión del archivo DLL D3DX y requiere que DirectX 9.0c ya esté presente.

El conjunto mínimo de archivos necesarios para compilar un paquete redistribuible son los siguientes archivos, ubicados en la carpeta Redist del SDK de DirectX (Archivos de programa \\ DirectX SDK \\ Redist \) :

-   dxsetup.exe
-   dsetup32.dll
-   dsetup.dll
-   dxupdate.cab

Agregue a estos los archivos de archivador para los componentes que desea instalar. Si necesita que los usuarios de la aplicación ya tengan DirectX 9.0c, no es necesario incluir DirectX.cab o dxnt.cab, que son la mayor parte del requisito de espacio. DirectX.cab solo es necesario para Windows 98 y Windows ME; dxnt.cab solo es necesario para Windows 2000, Windows XP y Windows XP SP1; y dxdllregx86.cab solo es necesario para \_ Windows 2000, Windows XP RTM, Windows XP SP1 y Windows Server 2003 RTM. Además, si no usa DirectShow o supone que ya está instalado, puede omitir BDA.cab, BDANT.cab y BDAXP.cab.

> [!Note]  
> Puede suponer que los usuarios de la aplicación ya tienen DirectX 9.0c si se instaló mediante una versión anterior de la aplicación, forzar a los usuarios a actualizar manualmente a través del Instalador web o asumir que tienen Windows XP SP2 o posterior.

 

Siguiendo con este ejemplo, si solo usa la versión de 32 bits de D3DX para abril de 2006, puede agregar apr2006 \_ d3dx9 \_ 30 \_x86.cab. Si usa la versión de 32 bits de agosto de 2006 de 32 bits de XINPUT, agregue xinput de ago2006 \_ \_x86.cab.

Si tiene una aplicación nativa de 64 bits, deberá agregar las \_ versiones x64. Sin embargo, si tiene una aplicación de 32 bits que se ejecuta en un sistema operativo de 64 bits, las versiones de 32 bits de los archivos DLL funcionarán.

A continuación, puede distribuir este paquete de archivos e iniciar DirectSetup en modo silencioso o ejecutar dxsetup.exe en el shell de comandos en modo silencioso. No olvide proteger este paquete mediante la comprobación de versiones de los archivos y asegúrese de que los usuarios no puedan optar por no ejecutar la instalación de DirectX. Cualquiera de estos eventos crea un proceso de instalación fallible.

## <a name="internal-deployment-of-the-debug-directx-runtime"></a>Implementación interna del entorno de ejecución de DirectX de depuración

Los entornos de ejecución de depuración de los componentes de DirectX se instalan cuando se instala el SDK de DirectX, pero la instalación del SDK en cada equipo de prueba puede ser difícil. Debe diseñar el proceso de instalación para copiar los archivos DLL del entorno de ejecución de depuración de la arquitectura del entorno de ejecución para desarrolladores del SDK de Microsoft DirectX de Archivos de programa \\ \\ Windows \\ \\ \\ system32 o en la carpeta \\ del juego.

Sin embargo, se recomienda encarecidamente no copiar simplemente los archivos DLL en tiempo de ejecución publicados, ya que es fácil olvidarse de quitarlos para el producto final. En su lugar, coloque los archivos de instalación de DirectX en una carpeta compartida y ejecute el programa de instalación en modo silencioso desde la carpeta compartida.

## <a name="desktop-bridge-applications"></a>Puente de dispositivo de escritorio aplicaciones 

Puente de dispositivo de escritorio que usan D3DX9, D3DX10, D3DX11, XAudio 2.7, XInput 1.3 o XACT deben descargar el marco [Microsoft.DirectX.x86](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x86.appx) o [Microsoft.DirectX.x64](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x64.appx) para implementar estos componentes heredados del SDK de DirectX en paralelo. Como alternativa, puede quitar todas estas dependencias (consulte la guía para desarrolladores de la versión redistribuible de &mdash; [XAudio 2.9](../xaudio2/xaudio2-redistributable.md)y las entradas de blog [Living without D3DX](https://walbourn.github.io/living-without-d3dx/) and [XINPUT and Windows 8](https://walbourn.github.io/xinput-and-windows-8/)).
