---
title: Ejemplo de DropDownColorPicker
description: En este ejemplo de código se muestra el marcado y el código necesarios para usar Windows control DropDownColorPicker de la cinta de opciones.
ms.assetid: cc8e18a6-9ed5-47ca-a807-f50838821f14
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 8c506dcd5497eb8822e8158337a7affcfa25622d68d9cc1e8d6a43324e7a1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933225"
---
# <a name="dropdowncolorpicker-sample"></a>Ejemplo de DropDownColorPicker

En este ejemplo de código se muestra el marcado y el código necesarios para usar Windows control DropDownColorPicker de la cinta de opciones.

- [Uso](#usage)
  - [Compilar el ejemplo](#building-the-sample)
  - [Ejecución del ejemplo](#running-the-sample)
- [Soporte técnico](#support)
- [Requisitos mínimos](#minimum-requirements)
- [Temas relacionados](#related-topics)

## <a name="usage"></a>Uso

Los ejemplos del marco Windows Ribbon se pueden descargar como proyectos de Microsoft Visual Studio independientes desde el Centro de descarga de [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o instalarse como parte del Kit de desarrollo de [software (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/)de Windows.

- Windows Kit de desarrollo de software (SDK) (ruta de instalación estándar): %ProgramFiles% SDK de Microsoft Windows número de versión \\ \\ Ejemplos \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ DropDownColorPicker

### <a name="building-the-sample"></a>Generar el ejemplo

Descargue el ejemplo.

Instale el SDK Windows para Windows 7 y abra su ventana de comandos del entorno de compilación. En el menú Inicio, elija Todos los programas, Microsoft Windows SDK y haga clic en Shell CMD.

Para generar el ejemplo en la ventana de comados del entorno de compilación, vaya al directorio de origen del ejemplo. En el símbolo del sistema, escriba MSBUILD.

Para compilar el ejemplo en Microsoft Visual Studio, cargue la solución de ejemplo o el archivo del proyecto y presione CTRL+MAYÚS+B.

### <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo desde la ventana de comandos del entorno de compilación, ejecute los archivos .exe en la carpeta Bin Debug o Bin Release contenida en la carpeta \\ \\ de origen de ejemplo.

Para ejecutar el ejemplo compilado con depuración en Visual Studio, presione F5.

## <a name="support"></a>Soporte técnico

El [foro Windows desarrollo de la cinta](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de opciones está disponible para analizar temas y hacer preguntas relacionadas con el desarrollo de Windows de cinta de opciones.

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Value |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) y [actualización de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo compatible | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 y [actualización de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7,0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Archivos de encabezado e IDL     | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> La actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores dirigir aplicaciones de la cinta de opciones de Windows a Windows Vista y Windows Server 2008. Las actualizaciones de la plataforma estarán disponibles para todos los Windows Vista y Windows Server 2008 a través de Windows Update. Las aplicaciones de terceros que requieren Actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o Actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden hacer que Windows Update detecte si está instalada la actualización necesaria. Si no es así, Windows Update lo descargará e instalará en segundo plano.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista desplegable Selector de colores](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[Selector de colores propiedades](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 





