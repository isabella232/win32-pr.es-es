---
description: Muestra cómo determinar el estado de pertenencia a un grupo en el hogar, enumerar los elementos de nivel superior en la carpeta del shell del grupo hogar e iniciar el Asistente para compartir el grupo en el hogar.
title: Ejemplo de HomeGroup
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c22ea84431f464ef8fcae6bfad0d90a45ba310d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082814"
---
# <a name="homegroup-sample"></a>Ejemplo de HomeGroup

Muestra cómo determinar el estado de pertenencia a un grupo en el hogar, enumerar los elementos de nivel superior en la carpeta del shell del **Grupo hogar** e iniciar el **Asistente para compartir el grupo** en el hogar.

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
| GitHub  | [Ejemplo de grupo hogar](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **Grupo hogar** .
2.  Escriba `msbuild HomeGroup.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **Grupo hogar** .
2.  Haga doble clic en el icono del archivo webhogar. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.
2.  En la línea de comandos, escriba `HomeGroup.exe` . Como alternativa, en el explorador de Windows, haga doble clic en el icono de HomeGroup.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IHomeGroup**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[**KNOWNFOLDERID**](knownfolderid.md)
</dt> </dl>

 

 



