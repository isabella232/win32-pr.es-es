---
description: Muestra cómo extender el menú contextual de arrastrar y colocar (a veces denominado menú contextual).
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248031"
---
# <a name="nondefaultdropmenuverb-sample"></a>Ejemplo de NonDefaultDropMenuVerb

Muestra cómo extender el menú contextual de arrastrar y colocar (a veces denominado menú contextual).

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo NonDefaultDropMenuVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **NonDefaultDropMenuVerb.**
2.  Escriba `msbuild NonDefaultDropMenuVerb.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows Explorador de aplicaciones y vaya al directorio del proyecto **NonDefaultDropMenuVerb.**
2.  Haga doble clic en el icono del archivo NonDefaultDropMenuVerb.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo archivo DLL, mediante el símbolo del sistema o Windows Explorer.
2.  Copie NonDefaultDropMenuVerb.dll en el directorio System (por ejemplo, C: \\ Windows \\ System32).
3.  En un símbolo del sistema, escriba `regedit NonDefaultDropMenuVerb.reg` .
4.  Use el botón derecho del mouse para arrastrar un archivo de una carpeta a otra. Verá elementos de menú adicionales para la operación de colocación.

 

 



