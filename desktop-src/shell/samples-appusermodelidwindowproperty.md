---
description: Muestra cómo controlar el comportamiento de agrupación de la barra de tareas de las ventanas de una aplicación a través de la propiedad System.AppUserModel.ID.
title: Ejemplo de propiedad de ventana de identificador de modelo del usuario de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985831"
---
# <a name="application-user-model-id-appid-window-property-sample"></a>Ejemplo de propiedad de ventana ID. de modelo de usuario (AppID)

Muestra cómo controlar el comportamiento de agrupación de la barra de tareas de las ventanas de una aplicación a través de la propiedad [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) .

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

Este ejemplo muestra cómo establecer la propiedad [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) mediante el uso de la implementación de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) de la ventana, que se obtiene a través de [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de AppUserModelIDWindowProperty](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **AppUserModelIDWindowProperty** .
2.  Escriba `msbuild AppUserModelIDWindowProperty.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **AppUserModelIDWindowProperty** .
2.  Haga doble clic en el icono del archivo AppUserModelIDWindowProperty. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.
2.  En la línea de comandos, escriba `AppUserModelIDWindowProperty.exe` . Como alternativa, en el explorador de Windows, haga doble clic en el icono de AppUserModelIDWindowProperty.exe.
3.  Para demostrar el efecto que tienen los identificadores de modelo de usuario de la aplicación (AppUserModelIDs) en la agrupación de la barra de tareas, inicie al menos tres instancias de la aplicación al mismo tiempo.
4.  Use el menú para establecer un AppUserModelID diferente en cada una de las tres ventanas. Tenga en cuenta que cada uno de los distintos resultados de AppUserModelID es un botón de la barra de tareas independiente y que Windows puede cambiar su identidad en tiempo de ejecución.
5.  Establezca al menos dos ventanas en el segundo AppUserModelID. Tenga en cuenta que ambos se mueven al mismo grupo de la barra de tareas.
6.  Abra la **barra de tareas y la ventana Propiedades del menú Inicio** haciendo clic con el botón secundario en la barra de tareas y seleccionando **propiedades** en el menú contextual. Cambiar los **botones de la barra de tareas:** desplegable entre **combinar cuando la barra de tareas está llena** y **nunca combinar** valores. Observe que cada ventana puede obtener un botón independiente, pero que los botones están agrupados por AppUserModelID.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 
