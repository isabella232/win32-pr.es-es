---
description: Muestra cómo escribir un controlador que se usa para mostrar una vista previa de archivos dentro del panel de vista previa Windows Explorer u otros hosts de controlador de vista previa.
title: Ejemplo de controlador de vista previa de recetas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267815"
---
# <a name="recipe-preview-handler-sample"></a>Ejemplo de controlador de vista previa de recetas

Muestra cómo escribir un controlador que se usa para mostrar una vista previa de archivos dentro del panel de vista previa Windows Explorer u otros hosts de controlador de vista previa.

Este tema contiene las siguientes secciones:

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Anulación del registro del archivo DLL del controlador de vista previa de ejemplo](#unregistering-the-sample-preview-handler-dll)
-   [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo RecipePreviewHandler](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **RecipePreviewHandler.** Por ejemplo, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.
2.  Escriba `msbuild PreviewHandlerSDKSample.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows explorador y vaya al directorio del proyecto **RecipePreviewHandler.**
2.  Haga doble clic en el icono del archivo PreviewHandlerSDKSample.sln para abrir el proyecto en Visual Studio.
    > [!Note]  
    > La extensión de nombre de archivo .sln no se muestra en la configuración de carpeta predeterminada. En esa situación, se puede identificar por su icono único o por su descripción de tipo "Microsoft Visual Studio solución".

     

3.  En el menú **Compilar**, seleccione **Compilar solución**.

> [!Note]  
> Si el sistema de destino es de 64 bits (x64), este controlador de vista previa de ejemplo debe crearse como una aplicación de 64 bits.

 

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **RecipePreviewHandler** creado. Por ejemplo, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`. Escriba `regsvr32.exe PreviewHandlerSDKSample.dll` para registrar el controlador.
2.  Abra Windows explorador y muestre el panel de vista previa si aún no se muestra.
    -   **Windows 7:** haga clic en el botón del panel de vista previa.
    -   **Windows Vista:** haga clic en **el menú** Organizar, vaya al submenú **Diseño** y seleccione Panel de **vista previa**.
3.  Use Windows Explorer para ir al directorio del proyecto **RecipePreviewHandler.**
4.  Seleccione el archivo .recipe de ejemplo.

Para que la salida de 32 bits (x86) y de 64 bits (x64) funcione en una versión de 64 bits de Windows, establezca el valor **de AppId** en el host suplente WOW64 , como se muestra en el `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` código siguiente.


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a>Anulación del registro del archivo DLL del controlador de vista previa de ejemplo

-   Abra la ventana del símbolo del sistema y escriba `regsvr32.exe /u PreviewHandlerSDKSample.dll` para anular el registro del controlador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[Id. de modelo de usuario de aplicación (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 
