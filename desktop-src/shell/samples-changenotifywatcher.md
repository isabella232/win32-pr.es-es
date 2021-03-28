---
description: Muestra cómo escuchar las notificaciones de cambios de Shell en una carpeta o un elemento en el espacio de nombres del explorador de Windows.
title: Ejemplo de cambio del monitor de notificaciones
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278014"
---
# <a name="change-notify-watcher-sample"></a>Ejemplo de cambio del monitor de notificaciones

Muestra cómo escuchar las notificaciones de cambios de Shell en una carpeta o un elemento en el espacio de nombres del explorador de Windows.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de ChangeNotifyWatcher](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **ChangeNotifyWatcher** .
2.  Escriba `msbuild ChangeNotifyWatcher.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **ChangeNotifyWatcher** .
2.  Haga doble clic en el icono del archivo ChangeNotifyWatcher. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.
2.  En el símbolo del sistema, escriba `ChangeNotifyWatcher.exe`. Como alternativa, en el explorador de Windows, haga doble clic en el icono de ChangeNotifyWatcher.exe.
3.  Para demostrar el efecto, los identificadores de modelo de usuario de la aplicación (AppUserModelIDs) seleccionan la carpeta que se va a ver haciendo clic en **"Pick..."** o mediante arrastrar y colocar en una carpeta de una ventana del explorador de Windows en la vista de lista del ejemplo.

 

 



