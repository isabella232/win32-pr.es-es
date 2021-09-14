---
description: Muestra cómo usar las API NotifyIcon y \_ \_ NotifyIconGetRect del shell para mostrar un icono de notificación.
title: Ejemplo de NotificationIcon
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359668"
---
# <a name="notificationicon-sample"></a>Ejemplo de NotificationIcon

Muestra cómo usar las API NotifyIcon y [**\_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) del shell para mostrar un icono de notificación. [**\_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)

## <a name="description"></a>Descripción

Además del uso de [**\_ Shell NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) y [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) para mostrar un icono de notificación, en este ejemplo también se muestra cómo mostrar una ventana flotante enriquecte, un menú contextual y una notificación en globo.

> [!Note]  
> [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) solo está disponible en Windows 7 y versiones posteriores.

 

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de NotificationIcon](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al **directorio del proyecto NotificationIcon.**
2.  Escriba `msbuild NotificationIcon.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows Explorador de aplicaciones y vaya al **directorio del proyecto NotificationIcon.**
2.  Haga doble clic en el icono del archivo NotificationIcon.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable mediante el símbolo del sistema o Windows Explorador.
2.  En la línea de comandos, escriba `NotificationIcon.exe` . Como alternativa, en Windows Explorer haga doble clic en el icono de NotificationIcon.exe.

> [!Note]  
> Los iconos de notificación especificados con un GUID se protegen contra la suplantación de identidad validando que solo una aplicación los registra. Este registro se realiza la primera vez que se llama a Shell NotifyIcon (NIM ADD, ...) y se almacena el nombre completo de la ruta \_ de acceso de la aplicación que realiza la \_ llamada. Si más adelante mueve el archivo binario a otra ubicación, el sistema no permitirá que se vuelva a agregar el icono. Consulte [**Shell \_ NotifyIcon para**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) obtener más información.

 

 

 



