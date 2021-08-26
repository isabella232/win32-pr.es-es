---
description: La aplicación globalizada debe definir diversos elementos de la interfaz de usuario, como menús, cuadros de diálogo, cadenas de ayuda y otros elementos, representados como recursos localizados.
ms.assetid: 4d8b769d-0830-4e4e-b284-ce0b21dfe5d4
title: Administración de recursos de LAN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c0b489d10ae28ca0fe7c659153b58c6ee7713e4eda4e1da9d96ffe16ae1a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041275"
---
# <a name="mui-resource-management"></a>Administración de recursos de LAN

La aplicación globalizada debe definir diversos elementos de la interfaz de usuario, como menús, cuadros de diálogo, cadenas de ayuda y otros elementos, representados como recursos localizados. El lenguaje de la interfaz de usuario se convierte en uno de los valores de la aplicación. En esta sección se describe la tecnología de recursos DE LAN, que se recomienda usar para crear los recursos de la aplicación.

## <a name="features-of-the-mui-resource-technology"></a>Características de la tecnología de recursos DE LA

La tecnología de recursos DE LA, expuesta en Windows Vista y versiones posteriores, tiene las siguientes características:

-   Los archivos de recursos específicos del lenguaje se almacenan por separado del binario de código de aplicación, de modo que un cambio de código no afecte a los recursos.
-   Los recursos de varios idiomas se pueden implementar en una sola instalación o en instalaciones independientes para cada idioma.
-   Un recurso se carga y se muestra según el idioma de la aplicación según lo establecido por el usuario.

Esta tecnología asocia los recursos definidos en archivos específicos del lenguaje con una versión determinada de un archivo de lenguaje neutro (LN). El archivo LN es un archivo Win32 PE que representa los recursos binarios y neutrales del lenguaje del código de la aplicación. La asociación de archivos usa una suma de comprobación reflejada en los datos de configuración de recursos contenidos en todos los archivos asociados. El cargador de recursos usa la suma de comprobación para comprobar que los archivos tienen la misma versión de los recursos necesarios. También valida el idioma del archivo específico del idioma con su nombre de carpeta. El cargador no carga un archivo de recursos si no se establece la asociación adecuada.

En concreto, la suma de comprobación principal se calcula a partir de los números de versión principal y secundaria de un archivo y del nombre de archivo (distingue mayúsculas de minúsculas), que se obtienen del recurso de versión. Esta suma de comprobación no debe cambiar entre las versiones RTM y Service Pack del mismo componente. Además, se usa una suma de comprobación de servicio para determinar la versión adecuada del archivo de recursos específico del lenguaje que se va a cargar. Esta suma de comprobación se calcula en función de los recursos localizables del archivo.

EL SITIO ofrece dos utilidades de recursos que puede usar para preparar los archivos de recursos para la aplicación. Una utilidad específica de CSV, denominada MUIRCT, le permite compilar un archivo LN y los archivos de recursos específicos del lenguaje asociados. En Windows Vista y versiones posteriores, el compilador de Windows RC también se ha modificado para compilar estos archivos de acuerdo con la tecnología de recursos DEG. Para obtener sintaxis y detalles de estas herramientas, vea [Utilidades de recursos](resource-utilities.md).

## <a name="ln-file"></a>Archivo LN

El archivo LN de una aplicación DE JAVA contiene código ejecutable y recursos neutrales del lenguaje que comparten e instalan todas las versiones de idioma de la aplicación.

## <a name="language-specific-resource-file"></a>Language-Specific de recursos

Normalmente, un archivo de recursos específico del lenguaje contiene cadenas de interfaz de usuario y otros elementos que requieren localización para un idioma determinado. La aplicación DEA usa un archivo de recursos específico del idioma por cada idioma admitido. El archivo LN de la aplicación es el mismo para cada archivo de recursos específico del lenguaje.

Cuando se genera mediante la tecnología de recursos DEG, los archivos específicos del lenguaje tienen una extensión ".mui" y se controlan de la siguiente manera:

-   Todos los archivos específicos del lenguaje asociados a un archivo LN determinado comparten el mismo nombre de archivo, que se forma agregando la extensión ".csv" al nombre de archivo completo (con extensión) del archivo LN correspondiente. Por ejemplo, un archivo LN denominado "Myfile.dll" tiene archivos específicos del lenguaje denominados "Myfile.dll.csv".
-   Los archivos específicos del lenguaje residen en subcarpetas de la carpeta que contiene el archivo LN. Cada nombre de carpeta refleja el idioma.

## <a name="resource-configuration-data"></a>Datos de configuración de recursos

Para asociar un archivo LN a sus archivos específicos del lenguaje, la tecnología de recursos DE JAVA usa datos de configuración de recursos, incluida la suma de comprobación. El procedimiento de compilación de recursos coloca esta información en una sección rc config de cada LN y archivo específico del lenguaje. Hay disponible una forma legible de esta información a través de la utilidad MUIRCT. Para obtener más información, vea [Utilidades de recursos.](resource-utilities.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Interfaz de usuario multilingüe](about-multilingual-user-interface.md)
</dt> <dt>

[Utilidades de recursos](resource-utilities.md)
</dt> </dl>

 

 



