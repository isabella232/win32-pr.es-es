---
description: Muestra cómo crear una Jump List personalizada para una aplicación, incluida la adición de una categoría y tareas personalizadas.
title: Ejemplo de lista de accesos directos personalizada
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c20592e508a24985e0f8283993482c7bd61af232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278012"
---
# <a name="custom-jump-list-sample"></a>Ejemplo de lista de accesos directos personalizada

Muestra cómo crear una Jump List personalizada para una aplicación, incluida la adición de una categoría y tareas personalizadas.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de CustomJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **CustomJumpList** .
2.  Escriba `msbuild CustomJumpListSample.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **CustomJumpList** .
2.  Haga doble clic en el icono del archivo CustomJumpListSample. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.
2.  En la línea de comandos, escriba `CustomJumpListSample.exe` . Como alternativa, en el explorador de Windows, haga doble clic en el icono de CustomJumpListSample.exe.
3.  Este ejemplo debe ejecutarse como administrador la primera vez que se ejecuta para que pueda instalar los registros de tipo de archivo necesarios. Una vez que se han registrado los tipos de archivo, el ejemplo se puede ejecutar como un usuario estándar.
4.  Seleccione opciones en el menú de la aplicación de ejemplo para ver cómo afectan a la Jump List de la aplicación en la barra de tareas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



