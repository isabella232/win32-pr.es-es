---
title: Ejemplo de la galería
description: En este ejemplo de código se muestra el marcado y el código necesarios para usar los distintos tipos de controles de Galería incluidos en el marco de cinta de Windows.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aacc52081fbcd2b6b58fd4c2439894705880d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150024"
---
# <a name="gallery-sample"></a>Ejemplo de la galería

En este ejemplo de código se muestra el marcado y el código necesarios para usar los distintos tipos de controles de Galería incluidos en el marco de cinta de Windows. En el ejemplo se incluye código que se puede usar para rellenar los elementos de forma dinámica en las galerías y controlar eventos especiales de vista previa de la galería que admiten la interfaz de usuario orientada a los resultados.

-   [Uso](#usage)
    -   [Compilar el ejemplo](#building-the-sample)
    -   [Ejecutar el ejemplo](#running-the-sample)
-   [Soporte técnico](#support)
-   [Requisitos mínimos](#minimum-requirements)
-   [Temas relacionados](#related-topics)

## <a name="usage"></a>Uso

El ejemplo de la galería de se puede descargar como un proyecto de Microsoft Visual Studio independiente desde el [centro de descarga de Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) o instalarse como parte del kit de desarrollo de [software (SDK) de Windows](https://msdn.microsoft.com/windows/bb980924.aspx).

-   Centro de descarga de Microsoft: [ejemplos de cinta de Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)
-   Kit de desarrollo de software (SDK) de Windows (ruta de instalación estándar):% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ número de versión de \] \\ ejemplo \\ WinUI \\ WindowsRibbon \\ Gallery

### <a name="building-the-sample"></a>Generar el ejemplo

Descargue el ejemplo en el disco duro.

Instale el Windows SDK para Windows 7 y abra la ventana de comandos del entorno de compilación. En el menú Inicio, elija Todos los programas, Microsoft Windows SDK y haga clic en Shell CMD.

Para generar el ejemplo en la ventana de comados del entorno de compilación, vaya al directorio de origen del ejemplo. En el símbolo del sistema, escriba MSBUILD.

Para compilar el ejemplo en Microsoft Visual Studio, cargue la solución de ejemplo o el archivo del proyecto y presione CTRL+MAYÚS+B.

### <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo desde la ventana de comandos del entorno de compilación, ejecute los archivos. exe de la \\ carpeta bin Debug o bin \\ Release incluida en la carpeta de origen de ejemplo.

Para ejecutar el ejemplo compilado con depuración en Visual Studio, presione F5.

## <a name="support"></a>Soporte técnico

El [Foro de desarrollo](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de la cinta de opciones de Windows está disponible para discutir temas y formular preguntas relacionadas con el desarrollo de aplicaciones de la cinta de opciones de Windows.

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Value |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) y la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo compatible | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 y [actualización de la plataforma para Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Archivos de encabezado y IDL     | uiribbon. h, uiribbon. idl                                                                                                                                                 |



 

> [!Note]  
> La [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores tener como destino aplicaciones de cinta de Windows para Windows Vista y Windows Server 2008. Las actualizaciones de la plataforma estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update. Las aplicaciones de terceros que requieren la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden detectar Windows Update detectar si está instalado el requerido actualizado; en caso contrario, Windows Update lo descargará e instalará en segundo plano.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con galerías](ribbon-controls-galleries.md)
</dt> <dt>

[Cuadro combinado](windowsribbon-controls-combobox.md)
</dt> <dt>

[Galería desplegable](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[En la galería de la cinta de opciones](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Galería de botones de expansión](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Propiedades de la colección](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





