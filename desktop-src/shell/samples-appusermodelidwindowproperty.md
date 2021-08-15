---
description: Muestra cómo controlar el comportamiento de agrupación de la barra de tareas de las ventanas de una aplicación a través de System.AppUserModel.ID propiedad .
title: Ejemplo de propiedad de ventana de identificador de modelo del usuario de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a6a4b0daca8b6bd4147c1e36d921b58b3802d975e678e49a9b9153761e61820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219885"
---
# <a name="application-user-model-id-appid-window-property-sample"></a>Ejemplo de propiedad de ventana Id. de modelo de usuario de aplicación (AppID)

Muestra cómo controlar el comportamiento de agrupación de la barra de tareas de las ventanas de una aplicación a través [de System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) propiedad .

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestra cómo establecer la propiedad [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) mediante el uso de la implementación [**de IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) de la ventana, que se obtiene a través de [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7,0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo AppUserModelIDWindowProperty](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **AppUserModelIDWindowProperty.**
2.  Escriba `msbuild AppUserModelIDWindowProperty.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra Windows Explorador de aplicaciones y vaya al directorio del proyecto **AppUserModelIDWindowProperty.**
2.  Haga doble clic en el icono del archivo AppUserModelIDWindowProperty.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable mediante el símbolo del sistema o Windows Explorador.
2.  En la línea de comandos, escriba `AppUserModelIDWindowProperty.exe` . Como alternativa, en Windows Explorer haga doble clic en el icono de AppUserModelIDWindowProperty.exe.
3.  Para demostrar el efecto que tienen los id. de modelo de usuario de la aplicación (AppUserModelID) en la agrupación de la barra de tareas, inicie al menos tres instancias de la aplicación al mismo tiempo.
4.  Use el menú para establecer un AppUserModelID diferente en cada una de las tres ventanas. Tenga en cuenta que cada AppUserModelID independiente da como resultado un botón de barra de tareas independiente y que las ventanas pueden cambiar su identidad en tiempo de ejecución.
5.  Establezca al menos dos ventanas en el segundo AppUserModelID. Observe que ambos se mueven al mismo grupo de la barra de tareas.
6.  Abra la **ventana Propiedades de la barra** de tareas y del menú Inicio haciendo clic con el botón derecho en la barra de tareas y **seleccionando Propiedades** en el menú contextual. Cambie los **botones de la barra** de tareas: lista desplegable entre Combinar cuando la barra de tareas está **llena** y **Nunca combinar** valores. Observe que cada ventana puede obtener un botón independiente, pero que los botones se agrupan por AppUserModelID.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Id. de modelo de usuario de aplicación (AppUserModelID)](appids.md)
</dt> </dl>

 

 
