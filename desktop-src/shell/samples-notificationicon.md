---
description: Muestra cómo usar las API de Shell \_ NotifyIcon y Shell \_ NotifyIconGetRect para mostrar un icono de notificación.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985578"
---
# <a name="notificationicon-sample"></a>Ejemplo de NotificationIcon

Muestra cómo usar las API de Shell [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) y [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) para mostrar un icono de notificación.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)

## <a name="description"></a>Descripción

Además del uso de los comandos [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) y [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) de Shell para mostrar un icono de notificación, en este ejemplo también se muestra cómo mostrar una ventana flotante enriquecida, un menú contextual y una notificación de globo.

> [!Note]  
> [**Shell \_ de NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) solo está disponible en Windows 7 y versiones posteriores.

 

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de NotificationIcon](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **NotificationIcon** .
2.  Escriba `msbuild NotificationIcon.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **NotificationIcon** .
2.  Haga doble clic en el icono del archivo NotificationIcon. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.
2.  En la línea de comandos, escriba `NotificationIcon.exe` . Como alternativa, en el explorador de Windows, haga doble clic en el icono de NotificationIcon.exe.

> [!Note]  
> Los iconos de notificación especificados con un GUID están protegidos contra la suplantación de identidad mediante la validación de que solo una única aplicación los registra. Este registro se realiza la primera vez que se llama a NotifyIcon del shell \_ (Nim \_ Add,...) y se almacena el nombre de la ruta de acceso completa de la aplicación que realiza la llamada. Si posteriormente mueve el archivo binario a una ubicación diferente, el sistema no permitirá que el icono se vuelva a agregar. Para obtener más información, consulte [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .

 

 

 



