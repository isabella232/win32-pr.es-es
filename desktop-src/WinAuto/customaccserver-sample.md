---
title: Ejemplo de CustomAccServer
description: .
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c047bde41bdf4a486e14ce6f293113a41ae9e285
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420363"
---
# <a name="customaccserver-sample"></a>Ejemplo de CustomAccServer

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Descargar información](#download-information)
-   [Requisitos mínimos](#minimum-requirements)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

Este ejemplo muestra cómo implementar un servidor de Microsoft Active Accessibility para un control personalizado simple. El objeto accesible para el control está compuesto del elemento raíz (un cuadro de lista) y sus elementos secundarios (los elementos de lista).

## <a name="download-information"></a>Descargar información

El ejemplo CustomAccServer se instala como parte del [Kit de desarrollo de software (SDK) de Microsoft Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) y está disponible en la siguiente ubicación.



| Location    | Ruta de acceso/URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Windows SDK | % Archivos de programa% \\ Microsoft SDK \\ Windows número de \\ \[ versión \] \\ ejemplos \\ WinUI \\ MSAA |



 

## <a name="minimum-requirements"></a>Requisitos mínimos



| Producto          | Versión                         |
|------------------|---------------------------------|
| Sistema operativo | Windows XP, Windows Server 2003 |
| Windows SDK      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo con Visual Studio 2008:

1.  Ejecute la herramienta de configuración del kit de desarrollo de software (SDK) de Microsoft Windows que se proporciona con el SDK para agregar directorios de inclusión de SDK a Visual Studio.
2.  Abra el explorador de Windows y navegue hasta el directorio del proyecto.
3.  Haga doble clic en el icono del archivo. sln (solución) para abrir el proyecto en Visual Studio.
4.  En el menú **compilar** , seleccione **compilar solución** para compilar la solución. La aplicación se compilará en el \\ Directorio de depuración o \\ versión predeterminado.

Para generar el ejemplo desde la línea de comandos, vea crear ejemplos en las notas de la versión de Windows SDK en la siguiente ubicación:% archivos de programa% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.
2.  Escriba AccServer.exe en la línea de comandos o haga doble clic en el icono de AccServer.exe para iniciarlo desde el explorador de Windows.

Para ejecutar desde Visual Studio, presione F5 o haga clic en **iniciar depuración** en el menú **depurar** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras](samples.md)
</dt> </dl>

 

 




