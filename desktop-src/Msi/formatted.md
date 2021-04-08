---
description: El tipo de datos con formato es una cadena de texto que se procesa para resolver nombres de propiedad incrustados, claves de tabla, referencias de variables de entorno y otras subcadenas especiales.
ms.assetid: 7a1bc160-a06c-4d57-b429-e39167893a45
title: Formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd15dca46839b25dbf186d8a741b7a5c37c05f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002267"
---
# <a name="formatted"></a>Formato

El tipo de datos con formato es una cadena de texto que se procesa para resolver nombres de propiedad incrustados, claves de tabla, referencias de variables de entorno y otras subcadenas especiales. Se reconocen las siguientes convenciones para resolver la cadena:

-   \[ \] En el texto se dejan corchetes () o llaves ({}) sin ningún par coincidente.
-   Si se encuentra una subcadena con el formato \[ *PropertyName* \] , se reemplaza por el valor de la propiedad. Si *PropertyName* no es un nombre de propiedad válido, la subcadena se resuelve como Blank. Por ejemplo, la columna Descripción de la [tabla LaunchCondition](launchcondition-table.md) toma una cadena con formato. Si ERRORTXT se ha establecido en "Póngase en contacto con el personal de soporte técnico". después, el texto que se muestra para el error de la condición de inicio incluiría esta cadena. Si no se establece ERRORTXT, el texto que se muestra para el error de la condición de inicio sería simplemente "el sistema no cumple los requisitos de instalación".

    

    | Condición | Descripción                                                  |
    |-----------|--------------------------------------------------------------|
    | Version9X | El sistema no cumple los requisitos de instalación. \[ERRORTXT\] |

    

     

-   Los corchetes se pueden recorrer en iteración y los nombres de propiedad se resuelven desde fuera. Por ejemplo, supongamos que la propiedad Substring \[ \[ \] \] aparece en el texto. En primer lugar, se recupera el valor de propiedad propertya. Si el valor es un nombre de propiedad válido, como PropertyB, se recupera el valor de PropertyB y toda la propiedad Substring a \[ \[ \] \] se sustituye por el valor de PropertyB. Si Propertya no es un nombre de propiedad válido o si el valor de Propertya no es un nombre de propiedad válido, la subcadena está en blanco.
-   Si se encuentra una subcadena con el formato \[ % *environmentvariable* \] , el valor de la variable de entorno se sustituye por la subcadena.
-   Si se encuentra una subcadena con el formato \[ \\ *x* \] , se reemplaza por el carácter *x* , donde *x* es un carácter, sin procesamiento adicional. Solo se mantiene el primer carácter después de la barra diagonal inversa; se quita todo lo demás. Por ejemplo, para incluir un corchete de apertura literal ( \[ ), use \[ \\ \[ \] . El \[ \\ \[ \] texto del corchete de texto \[ \\ \] \] se resuelve en el \[ texto entre corchetes \] .
-   Si una subcadena está delimitada por llaves ({}) y no contiene nombres de propiedad entre corchetes ( \[ \] ), la subcadena se deja sin cambios, incluidas las llaves.
-   Si una subcadena está encerrada entre llaves ({}) y contiene uno o varios nombres de propiedad entre corchetes (), \[ \] entonces, si todos los nombres de propiedad son válidos, el texto (con las sustituciones resueltas) se muestra sin las llaves.
-   Si se encuentra una subcadena con el formato \[ ~ \] , se reemplaza por el carácter nulo. Se utiliza para crear cadenas de caracteres de **reg \_ multi \_ SZ** en la [tabla del registro](registry-table.md). Tenga en cuenta que \[ ~ \] también se usa para anexar o prefijar valores a las variables de entorno mediante la [tabla de entorno](environment-table.md).
-   Si se encuentra una subcadena con el formato \[ \# *filekey* \] , se reemplaza por la ruta de acceso completa del archivo, con el valor *filekey* usado como clave en la [tabla de archivos](file-table.md). El valor de \[ \# *filekey* \] permanece en blanco y no se reemplaza por una ruta de acceso hasta que el instalador ejecuta la acción [CostInitialize](costinitialize-action.md), la acción [FileCost](filecost-action.md)y la [acción CostFinalize](costfinalize-action.md). El valor de \[ \# *filekey* \] depende del estado de instalación del componente al que pertenece el archivo. Si el componente se ejecuta desde el origen, el valor es la ruta de acceso a la ubicación de origen del archivo. Si el componente se ejecuta localmente, el valor es la ruta de acceso a la ubicación de destino del archivo después de la instalación. Si el componente tiene un estado de acción de ausente, el estado instalado del componente se utiliza para determinar el \[ \) .
-   Si se encuentra una subcadena con el formato \[ $ *componentkey* \] , se reemplaza por el directorio de instalación del componente, con el valor *componentkey* usado como clave en la tabla de [componentes](component-table.md). El valor de \[ $ *componentkey* \] permanece en blanco y no se reemplaza por un directorio hasta que el instalador ejecuta la acción [CostInitialize](costinitialize-action.md), la acción [FileCost](filecost-action.md)y la [acción CostFinalize](costfinalize-action.md). El valor de \[ $ *componentkey* \] depende del estado de instalación del componente y dónde se produce. En la columna valor de la [tabla del registro](registry-table.md), esta subcadena puede hacer referencia al estado de la acción o al estado de acción solicitado del componente. En todos los demás casos, esta subcadena hace referencia al estado de acción del componente. Por ejemplo, si el componente se ejecuta desde el origen, el valor es el directorio de origen del archivo. Si el componente se ejecuta localmente, el valor es el directorio de destino después de la instalación. Si el componente está ausente, el valor se deja en blanco. Windows Installer realiza un seguimiento de la acción y de los Estados de instalación solicitados de los componentes. Por ejemplo, si un componente ya está instalado, puede tener un estado solicitado de local y un estado de acción null. Para obtener más información acerca de cómo comprobar el estado de instalación de los componentes de, vea [comprobar la instalación de características, componentes y archivos](checking-the-installation-of-features-components-files.md).
-   Tenga en cuenta que si un componente ya está instalado y no se reinstala, se quita o se mueve durante la instalación actual, el estado de acción del componente es NULL y la cadena \[ $ *componentkey* se \] evalúa como null.
-   Si es una subcadena con el formato \[ !*filekey* \] , se reemplaza por la ruta de acceso corta completa del archivo, con el valor *filekey* usado como clave en la [tabla de archivos](file-table.md).

    Esta sintaxis solo es válida cuando se usa en la columna valor del registro o en las tablas IniFile. Cuando se usa en otras columnas, esta sintaxis se trata igual que \[ \# *filekey* \] .

 

 



