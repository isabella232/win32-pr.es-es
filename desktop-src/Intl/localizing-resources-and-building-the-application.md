---
description: En este tema se describe cómo compilar una aplicación de MUI típica.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localizar recursos y compilar la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687096"
---
# <a name="localizing-resources-and-building-the-application"></a>Localizar recursos y compilar la aplicación

En este tema se describe cómo compilar una aplicación de MUI típica. Se supone que usa Microsoft Visual Studio para la codificación y Microsoft Visual Studio o la línea de comandos de Visual Studio para la compilación. Se supone que usa un archivo de solución. sln para la aplicación y que admite un archivo resource. h para reflejar el archivo de recursos de idioma base.

> [!Note]  
> Si usa la línea de comandos de Visual Studio para la compilación, usará el comando **VCBUILD** para compilar el archivo de solución.

 

Los archivos de aplicación se compilan por separado para cada idioma. Cada compilación crea idénticos archivos. exe, independientes del lenguaje y específicos del lenguaje. Además, se copian varios archivos en las carpetas de versión correspondientes.

La compilación de la aplicación depende del tipo de recursos y del tipo de localización que esté usando. Para la localización anterior a la compilación, tiene una copia del archivo de idioma base localizado para cada idioma admitido. En la localización posterior a la compilación, puede copiar el archivo. mui resultante de la compilación del módulo ejecutable y de recursos, y proporcionar las copias a los localizadores.

> [!Note]  
> En el procedimiento siguiente se presupone que los recursos de Win32 PE tienen un proyecto de Visual Studio creado para cada lenguaje. Los recursos de idioma base se proporcionan en un archivo. RC y se cargan mediante un módulo DLL. Puede repetir el procedimiento según sea necesario para compilar para todos los idiomas admitidos.

 

**Para compilar la aplicación**

1.  Configure un proyecto de Visual Studio para el idioma base.
2.  Si está interesado en usar un archivo de configuración de recursos con las herramientas de recursos, configure uno como se describe en [preparación de un archivo de configuración de recursos](preparing-a-resource-configuration-file.md).
3.  Establezca los parámetros requeridos por la utilidad del compilador RC en las páginas de propiedades del proyecto, en **propiedades de configuración → recursos → línea de comandos → opciones adicionales**.
4.  Ejecute el compilador RC. La utilidad compila y divide los recursos no localizables y localizables en dos archivos de objeto diferentes, utilizando los datos de configuración de recursos. En este paso, los recursos independientes del lenguaje están vinculados a un archivo LN. Para obtener más información, consulte la descripción de la utilidad en [Resource Utilities](resource-utilities.md).
5.  Para vincular los recursos específicos del idioma a un archivo. mui específico del idioma, establezca un evento posterior a la compilación para el proyecto en las páginas de propiedades de **propiedades de configuración → eventos de compilación → evento posterior a la compilación → línea de comandos**.
6.  Establezca un evento posterior a la compilación para aplicar el valor de la suma de comprobación del archivo LN al archivo. mui correspondiente al idioma. Puede usar la utilidad MUIRCT para este paso. Para obtener más información, consulte la descripción de la utilidad en [Resource Utilities](resource-utilities.md).
7.  Use la línea de comandos del evento posterior a la compilación para agregar comandos para copiar los archivos en la estructura de carpetas de versión adecuada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la interfaz de usuario multilingüe](using-multilingual-user-interface.md)
</dt> <dt>

[Preparación de un archivo de configuración de recursos](preparing-a-resource-configuration-file.md)
</dt> <dt>

[Utilidades de recursos](resource-utilities.md)
</dt> </dl>

 

 



