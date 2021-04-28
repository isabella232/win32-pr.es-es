---
title: Ejemplo customAccServer
description: Ejemplo customAccServer
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f8ee7d82361177af07aa7ad53a6137c39bc38
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088013"
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

El ejemplo CustomAccServer se instala como parte de [Microsoft Kit de desarrollo de software de Windows (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) y está disponible en la siguiente ubicación.



| Location    | Ruta de acceso o dirección URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Windows SDK | %Program Files% \\ Microsoft SDKs \\ Windows version number Samples \\ \[ \] \\ \\ winui \\ msaa |



 

## <a name="minimum-requirements"></a>Requisitos mínimos



| Producto          | Versión                         |
|------------------|---------------------------------|
| Sistema operativo | Windows XP, Windows Server 2003 |
| Windows SDK      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo mediante Visual Studio 2008:

1.  Ejecute la herramienta de configuración de Microsoft Kit de desarrollo de software de Windows (SDK) proporcionada con el SDK para agregar directorios de incluyen del SDK a Visual Studio.
2.  Abra Explorador de Windows y vaya al directorio del proyecto.
3.  Haga doble clic en el icono del archivo .sln (solución) para abrir el proyecto en Visual Studio.
4.  En el **menú Compilar,** seleccione **Compilar solución** para compilar la solución. La aplicación se compilará en el directorio \\ debug o \\ release predeterminado.

Para compilar el ejemplo desde la línea de comandos, vea Compilar ejemplos en las notas de la versión de Windows SDK en la siguiente ubicación: %Archivos de programa% Sdk \\ de Microsoft para Windows \\ \\ v7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Vaya al directorio que contiene el nuevo ejecutable mediante el símbolo del sistema o Explorador de Windows.
2.  Escriba AccServer.exe en la línea de comandos o haga doble clic en el icono AccServer.exe para iniciarlo desde Explorador de Windows.

Para ejecutar desde Visual Studio, presione F5 o haga clic **en Iniciar depuración** en el **menú** Depurar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras](samples.md)
</dt> </dl>

 

 




