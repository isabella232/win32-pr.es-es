---
title: Ejemplo customAccServer
description: Ejemplo customAccServer
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ebf1ecde2821208d788b20b5cb0fc1a00403c1607fb4604eb92845daf49d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325994"
---
# <a name="customaccserver-sample"></a>Ejemplo customAccServer

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Descargar información](#download-information)
-   [Requisitos mínimos](#minimum-requirements)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestra cómo implementar un servidor Microsoft Active Accessibility para un control personalizado simple. El objeto accesible para el control consta del elemento raíz (un cuadro de lista) y sus elementos secundarios (los elementos de lista).

## <a name="download-information"></a>Descargar información

El ejemplo CustomAccServer se instala como parte del Kit de desarrollo de [software (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) de Microsoft Windows y está disponible en la siguiente ubicación.



| Ubicación    | Ruta de acceso o dirección URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Windows SDK | %Program Files% \\ Microsoft SDKs \\ Windows version number Samples \\ \[ \] \\ \\ winui \\ msaa |



 

## <a name="minimum-requirements"></a>Requisitos mínimos



| Producto          | Versión                         |
|------------------|---------------------------------|
| Sistema operativo | Windows XP, Windows Server 2003 |
| Windows SDK      | 7,0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo mediante Visual Studio 2008:

1.  Ejecute la herramienta de configuración del Kit de desarrollo de software (SDK) de Microsoft Windows que se proporciona con el SDK para agregar directorios de incluyen del SDK a Visual Studio.
2.  Abra Windows Explorador de proyectos y vaya al directorio del proyecto.
3.  Haga doble clic en el icono del archivo .sln (solución) para abrir el proyecto en Visual Studio.
4.  En el **menú Compilar,** seleccione **Compilar solución** para compilar la solución. La aplicación se compilará en el directorio \\ debug o \\ release predeterminado.

Para compilar el ejemplo desde la línea de comandos, consulte Compilar ejemplos en las notas de la versión del SDK de Windows en la siguiente ubicación: %Archivos de programa% SDK de \\ Microsoft \\ Windows \\ v7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Vaya al directorio que contiene el nuevo ejecutable mediante el símbolo del sistema o Windows Explorador.
2.  Escriba AccServer.exe en la línea de comandos o haga doble clic en el icono de AccServer.exe para iniciarlo desde Windows Explorador.

Para ejecutar desde Visual Studio, presione F5 o haga clic **en Iniciar depuración** en el **menú** Depurar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras](samples.md)
</dt> </dl>

 

 




