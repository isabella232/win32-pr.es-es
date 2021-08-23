---
description: Muestra cómo crear una aplicación personalizada Lista de accesos directos una aplicación, incluida la adición de una categoría y tareas personalizadas.
title: Ejemplo de lista de accesos directos personalizada
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb6f5db0b9576f360abcbaacb8a8a5a291d3dbe07754281954ea585d3ebe965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968834"
---
# <a name="custom-jump-list-sample"></a>Ejemplo de lista de accesos directos personalizada

Muestra cómo crear una aplicación personalizada Lista de accesos directos una aplicación, incluida la adición de una categoría y tareas personalizadas.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7,0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo CustomJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **CustomJumpList.**
2.  Escriba `msbuild CustomJumpListSample.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra Windows explorador y vaya al directorio del proyecto **CustomJumpList.**
2.  Haga doble clic en el icono del archivo CustomJumpListSample.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o Windows Explorer.
2.  En la línea de comandos, escriba `CustomJumpListSample.exe` . Como alternativa, en Windows Explorer haga doble clic en el icono de CustomJumpListSample.exe.
3.  Este ejemplo debe ejecutarse como administrador la primera vez que se ejecuta para poder instalar los registros de tipo de archivo necesarios. Una vez registrados los tipos de archivo, el ejemplo se puede ejecutar como un usuario estándar.
4.  Seleccione opciones en el menú de la aplicación de ejemplo para ver cómo afectan a la configuración Lista de accesos directos aplicación en la barra de tareas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Id. de modelo de usuario de aplicación (AppUserModelID)](appids.md)
</dt> </dl>

 

 



