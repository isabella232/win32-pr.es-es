---
description: Muestra cómo agregar elementos a la Lista de accesos directos automática para una aplicación, incluido el cambio entre la presentación de las categorías Frecuente y Reciente.
title: Ejemplo de lista de accesos directos automática
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256916"
---
# <a name="automatic-jump-list-sample"></a>Ejemplo de lista de accesos directos automática

Muestra cómo agregar elementos a la Lista de accesos directos automática para una aplicación, incluido el cambio entre la presentación de las categorías Frecuente y Reciente.

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
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo AutomaticJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **AutomaticJumpList.**
2.  Escriba `msbuild AutomaticJumpListSample.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows Explorador de aplicaciones y vaya al directorio del proyecto **AutomaticJumpList.**
2.  Haga doble clic en el icono del archivo AutomaticJumpListSample.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable mediante el símbolo del sistema o Windows Explorador.
2.  En la línea de comandos, escriba `AutomaticJumpListSample.exe` . Como alternativa, en Windows Explorer haga doble clic en el icono de AutomaticJumpListSample.exe.
3.  Este ejemplo debe ejecutarse como administrador la primera vez que se ejecuta para poder instalar los registros de tipo de archivo necesarios. Una vez registrados los tipos de archivo, el ejemplo se puede ejecutar como un usuario estándar.
4.  Seleccione las opciones del menú de la aplicación de ejemplo, incluida la selección  de documentos .txt o .doc a través del cuadro de diálogo Abrir para ver cómo afectan a los Lista de accesos directos de la aplicación en la barra de tareas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Id. de modelo de usuario de aplicación (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



