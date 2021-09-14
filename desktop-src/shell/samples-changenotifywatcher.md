---
description: Muestra cómo escuchar las notificaciones de cambios de Shell en una carpeta o elemento del espacio de nombres Windows Explorer.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248043"
---
# <a name="change-notify-watcher-sample"></a>Ejemplo de cambio del monitor de notificaciones

Muestra cómo escuchar las notificaciones de cambios de Shell en una carpeta o elemento del espacio de nombres Windows Explorer.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de ChangeNotifyWatcher](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **ChangeNotifyWatcher.**
2.  Escriba `msbuild ChangeNotifyWatcher.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows explorador y vaya al directorio del proyecto **ChangeNotifyWatcher.**
2.  Haga doble clic en el icono del archivo ChangeNotifyWatcher.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable mediante el símbolo del sistema o Windows Explorador.
2.  En el símbolo del sistema, escriba `ChangeNotifyWatcher.exe`. Como alternativa, en Windows Explorer haga doble clic en el icono de ChangeNotifyWatcher.exe.
3.  Para mostrar el efecto, los id. de modelo de usuario de la aplicación (AppUserModelIDs) seleccionan una carpeta que se va a ver haciendo clic en **"Seleccionar..."** o mediante el uso de arrastrar y colocar en una carpeta desde una ventana del Explorador de Windows en la vista de lista del ejemplo.

 

 



