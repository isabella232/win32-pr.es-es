---
description: La aplicación globalizada debe definir una variedad de elementos de la interfaz de usuario, como menús, cuadros de diálogo, cadenas de ayuda y otros elementos, que se representan como recursos localizados.
ms.assetid: 4d8b769d-0830-4e4e-b284-ce0b21dfe5d4
title: Administración de recursos de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeed59c4b835e2c93e5f4cfc9988509349d8b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666737"
---
# <a name="mui-resource-management"></a>Administración de recursos de MUI

La aplicación globalizada debe definir una variedad de elementos de la interfaz de usuario, como menús, cuadros de diálogo, cadenas de ayuda y otros elementos, que se representan como recursos localizados. El idioma de la interfaz de usuario se convierte en uno de los valores de configuración de la aplicación. En esta sección se describe la tecnología de recursos de MUI, que se recomienda utilizar para crear los recursos de la aplicación.

## <a name="features-of-the-mui-resource-technology"></a>Características de la tecnología de recursos de MUI

La tecnología de recursos de MUI, expuesta en Windows Vista y versiones posteriores, tiene las siguientes características:

-   Los archivos de recursos específicos del lenguaje se almacenan de forma independiente del archivo binario del código de la aplicación, de modo que un cambio de código no afecte a los recursos.
-   Los recursos para varios idiomas se pueden implementar en una instalación única o en instalaciones independientes para cada idioma.
-   Un recurso se carga y se muestra según el idioma de la aplicación establecido por el usuario.

Esta tecnología asocia los recursos definidos en archivos específicos del idioma con una versión concreta de un archivo independiente del lenguaje (LN). El archivo LN es un archivo PE de Win32 que representa el código de aplicación binario y los recursos independientes del idioma. La Asociación de archivos utiliza una suma de comprobación que se refleja en los datos de configuración de recursos incluidos en todos los archivos asociados. El cargador de recursos utiliza la suma de comprobación para comprobar que los archivos contienen la misma versión de los recursos necesarios. También valida el idioma del archivo específico del idioma con su nombre de carpeta. El cargador no carga un archivo de recursos si no se establece la Asociación adecuada.

En concreto, la suma de comprobación principal se calcula a partir de los números de versión principal y secundaria de un archivo y el nombre de archivo (distingue mayúsculas de minúsculas), que se obtienen del recurso de versión. Esta suma de comprobación no debe cambiar entre las versiones RTM y Service Pack del mismo componente. Además, una suma de comprobación de servicio se usa para determinar la versión adecuada del archivo de recursos específico del idioma que se va a cargar. Esta suma de comprobación se calcula en función de los recursos localizables del archivo.

MUI aporta dos utilidades de recursos que puede usar para preparar los archivos de recursos para la aplicación. Una utilidad específica de MUI, denominada MUIRCT, permite crear un archivo LN y archivos de recursos específicos del idioma asociados. En Windows Vista y versiones posteriores, el compilador de Windows RC también se ha modificado para compilar estos archivos según la tecnología de recursos de MUI. Para obtener información sobre la sintaxis y los detalles de estas herramientas, consulte [Resource Utilities](resource-utilities.md).

## <a name="ln-file"></a>Archivo LN

El archivo LN para una aplicación MUI contiene código ejecutable y recursos independientes del lenguaje que se comparten e instalan en todas las versiones de idioma de la aplicación.

## <a name="language-specific-resource-file"></a>Language-Specific archivo de recursos

Normalmente, un archivo de recursos específico del lenguaje contiene cadenas de la interfaz de usuario y otros elementos que requieren localización para un idioma determinado. La aplicación MUI usa un archivo de recursos específico del idioma por idioma compatible. El archivo LN de la aplicación es el mismo para cada archivo de recursos específico del idioma.

Cuando se genera mediante la tecnología de recursos de MUI, los archivos específicos del lenguaje tienen una extensión ". mui" y se administran de la siguiente manera:

-   Los archivos específicos del idioma asociados a un archivo LN determinado comparten el mismo nombre de archivo, que se forma mediante la adición de la extensión ". mui" al nombre de archivo completo (con la extensión) del archivo LN correspondiente. Por ejemplo, un archivo LN denominado "Myfile.dll" tiene archivos específicos del idioma denominados "Myfile.dll. mui".
-   Los archivos específicos del idioma residen en las subcarpetas de la carpeta que contiene el archivo LN. Cada nombre de carpeta refleja el idioma.

## <a name="resource-configuration-data"></a>Datos de configuración de recursos

Para asociar un archivo LN a sus archivos específicos del lenguaje, la tecnología de recursos de MUI utiliza datos de configuración de recursos, incluida la suma de comprobación. El procedimiento de compilación de recursos coloca esta información en una sección de configuración de RC de cada archivo LN y específico del idioma. Una forma legible de esta información está disponible a través de la utilidad MUIRCT. Para obtener más información, vea [Resource Utilities](resource-utilities.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la interfaz de usuario multilingüe](about-multilingual-user-interface.md)
</dt> <dt>

[Utilidades de recursos](resource-utilities.md)
</dt> </dl>

 

 



