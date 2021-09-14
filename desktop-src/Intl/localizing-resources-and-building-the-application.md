---
description: En este tema se describe cómo compilar una aplicación TÍPICA de MUI.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localización de recursos y creación de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063070"
---
# <a name="localizing-resources-and-building-the-application"></a>Localización de recursos y creación de la aplicación

En este tema se describe cómo compilar una aplicación TÍPICA de MUI. Se supone que está usando Microsoft Visual Studio para codificar y Microsoft Visual Studio o la Visual Studio de comandos para la creación. Se supone que usa un archivo de solución .sln para la aplicación y admite un archivo Resource.h para reflejar el archivo de recursos del lenguaje base.

> [!Note]  
> Si usa la Visual Studio de comandos para la compilación, usará el **comando vcbuild** para compilar el archivo de solución.

 

Los archivos de aplicación se construyen por separado para cada lenguaje. Cada compilación crea archivos de .exe y específicos del .exe.mui. Además, se copian otros archivos en las carpetas de versión adecuadas.

La compilación de la aplicación depende del tipo de recursos y del tipo de localización que se use. Para la localización previa a la compilación, tiene una copia del archivo de idioma base localizado para cada idioma admitido. Para la localización posterior a la compilación, puede copiar el archivo .mui resultante de la compilación del módulo ejecutable y de recursos y proporcionar las copias a los localizadores.

> [!Note]  
> En el procedimiento siguiente se asumen los recursos de Win32 PE con Visual Studio proyecto creado para cada lenguaje. Los recursos de lenguaje base se proporcionan en un archivo .rc y se cargan mediante un módulo DLL. Puede repetir el procedimiento según sea necesario para compilar para todos los idiomas admitidos.

 

**Para compilar la aplicación**

1.  Configure un proyecto Visual Studio para el lenguaje base.
2.  Si está interesado en usar un archivo de configuración de recursos con las herramientas de recursos, configure uno como se describe en [Preparar un archivo de configuración de recursos](preparing-a-resource-configuration-file.md).
3.  Establezca los parámetros requeridos por la utilidad del compilador RC en las páginas de propiedades del proyecto en Propiedades de configuración → recursos → línea de **comandos → opciones adicionales**.
4.  Ejecute el compilador RC. La utilidad compila y divide los recursos no localizables y localizables en dos archivos de objeto diferentes, mediante datos de configuración de recursos. En este paso, los recursos sin idioma se vinculan a un archivo LN. Para más información, consulte la descripción de la utilidad en [Utilidades de recursos.](resource-utilities.md)
5.  Para vincular los recursos específicos del idioma a un archivo .mui específico del lenguaje, establezca un evento posterior a la compilación para el proyecto en las páginas de propiedades en Propiedades de configuración → Eventos de compilación → Evento posterior a la compilación → línea **de comandos**.
6.  Establezca un evento posterior a la compilación para aplicar el valor de suma de comprobación del archivo LN al archivo .mui para el idioma. Puede usar la utilidad MUIRCT para este paso. Para más información, consulte la descripción de la utilidad en [Utilidades de recursos.](resource-utilities.md)
7.  Use la línea de comandos del evento posterior a la compilación para agregar comandos para copiar los archivos en la estructura de carpetas de versión adecuada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Interfaz de usuario multilingüe](using-multilingual-user-interface.md)
</dt> <dt>

[Preparar un archivo de configuración de recursos](preparing-a-resource-configuration-file.md)
</dt> <dt>

[Utilidades de recursos](resource-utilities.md)
</dt> </dl>

 

 



