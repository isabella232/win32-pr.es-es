---
description: Muestra cómo determinar el estado de pertenencia a HomeGroup, enumerar elementos de nivel superior en la carpeta Shell de HomeGroup e iniciar el Asistente para uso compartido de HomeGroup.
title: Ejemplo de HomeGroup
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f706eafd974487d8e91e15e3685bee72250235a704678ac4353577b8ae5ac675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048927"
---
# <a name="homegroup-sample"></a>Ejemplo de HomeGroup

Muestra cómo determinar el estado de pertenencia a HomeGroup, enumerar elementos de nivel superior en la carpeta Shell de **HomeGroup** e iniciar el Asistente para uso compartido **de HomeGroup**.

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

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo homeGroup](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio **del proyecto HomeGroup.**
2.  Escriba `msbuild HomeGroup.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra Windows explorador y vaya al directorio **del proyecto HomeGroup.**
2.  Haga doble clic en el icono del archivo HomeGroup.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o Windows Explorer.
2.  En la línea de comandos, escriba `HomeGroup.exe` . Como alternativa, en Windows Explorer haga doble clic en el icono de HomeGroup.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IHomeGroup**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[**KNOWNFOLDERID**](knownfolderid.md)
</dt> </dl>

 

 



