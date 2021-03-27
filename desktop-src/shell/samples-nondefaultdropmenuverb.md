---
description: Muestra cómo extender el menú contextual de arrastrar y colocar (a veces conocido como menú contextual).
title: Ejemplo de NonDefaultDropMenuVerb
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361185"
---
# <a name="nondefaultdropmenuverb-sample"></a>Ejemplo de NonDefaultDropMenuVerb

Muestra cómo extender el menú contextual de arrastrar y colocar (a veces conocido como menú contextual).

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de NonDefaultDropMenuVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **NonDefaultDropMenuVerb** .
2.  Escriba `msbuild NonDefaultDropMenuVerb.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **NonDefaultDropMenuVerb** .
2.  Haga doble clic en el icono del archivo NonDefaultDropMenuVerb. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo archivo DLL mediante el símbolo del sistema o el explorador de Windows.
2.  Copie NonDefaultDropMenuVerb.dll en el directorio del sistema (por ejemplo, C: \\ Windows \\ system32).
3.  En un símbolo del sistema, escriba `regedit NonDefaultDropMenuVerb.reg` .
4.  Use el botón secundario del mouse para arrastrar un archivo de una carpeta a otra. Verá elementos de menú adicionales para la operación de colocar.

 

 



