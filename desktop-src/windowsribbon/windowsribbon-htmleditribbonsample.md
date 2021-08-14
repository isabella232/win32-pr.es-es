---
title: Ejemplo HTMLEditRibbon
description: En este ejemplo de código se muestra el marcado y el código necesarios para migrar una aplicación Microsoft Foundation Classes (MFC) existente para usar Windows cinta de opciones.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 0f1299bdc20b1b94a5113d3cfcdda205b6ad8e513a59706d708362fbc8383bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202123"
---
# <a name="htmleditribbon-sample"></a>Ejemplo HTMLEditRibbon

En este ejemplo de código se muestra el marcado y el código necesarios para migrar una aplicación Microsoft Foundation Classes (MFC) existente para usar Windows cinta de opciones. Se creó tomando la aplicación de ejemplo HTMLEdit de MFC existente y modificando su código y recursos para usar Windows cinta de opciones.

- [Comentarios:](#remarks)
- [Uso](#usage)
  - [Compilar el ejemplo](#building-the-sample)
  - [Ejecución del ejemplo](#running-the-sample)
- [Soporte técnico](#support)
- [Requisitos mínimos](#minimum-requirements)

## <a name="remarks"></a>Comentarios

Para obtener el ejemplo de MFC, vea [HtmlEdit Sample: Wraps the Internet Explorer control de edición MSHTML](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).

## <a name="usage"></a>Uso

Los ejemplos Windows marco de la cinta de opciones de Windows se pueden descargar como proyectos de Microsoft Visual Studio independientes desde el Centro de descarga de [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o instalarse como parte del Kit de desarrollo de [software (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/)de Windows.

- Windows Kit de desarrollo de software (SDK) (ruta de instalación estándar): %ProgramFiles% SDK de Microsoft Windows número de versión \\ \\ Ejemplos \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ HTMLEditRibbon

### <a name="building-the-sample"></a>Generar el ejemplo

Descargue el ejemplo.

Instale el SDK Windows para Windows 7 y abra su ventana de comandos del entorno de compilación. En el menú Inicio, elija Todos los programas, Microsoft Windows SDK y haga clic en Shell CMD.

Para generar el ejemplo en la ventana de comados del entorno de compilación, vaya al directorio de origen del ejemplo. En el símbolo del sistema, escriba MSBUILD.

Para compilar el ejemplo en Microsoft Visual Studio, cargue la solución de ejemplo o el archivo del proyecto y presione CTRL+MAYÚS+B.

### <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo desde la ventana de comandos del entorno de compilación, ejecute los archivos .exe en la carpeta Bin Debug o Bin Release contenida en la carpeta \\ \\ de origen de ejemplo.

Para ejecutar el ejemplo compilado con depuración en Visual Studio, presione F5.

## <a name="support"></a>Soporte técnico

El [foro Windows desarrollo de la cinta](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de opciones está disponible para analizar temas y hacer preguntas relacionadas con el desarrollo de Windows ribbon.

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Valor |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) y [Platform Update para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo compatible | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 y [actualización de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7,0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Archivos de encabezado e IDL     | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> La actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores dirigir aplicaciones de cinta de opciones de Windows a Windows Vista y Windows Server 2008. Las actualizaciones de la plataforma estarán disponibles para todos los Windows Vista y Windows Server 2008 a través de Windows Update. Las aplicaciones de terceros que requieren Actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o Actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden hacer que Windows Update detecte si está instalada la actualización necesaria; Si no es así, Windows Update la descargará e instalará en segundo plano.

 

 

 





