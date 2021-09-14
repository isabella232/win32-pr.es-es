---
description: El tipo de datos Con formato es una cadena de texto que se procesa para resolver nombres de propiedades incrustadas, claves de tabla, referencias de variables de entorno y otras subcadenas especiales.
ms.assetid: 7a1bc160-a06c-4d57-b429-e39167893a45
title: Formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd15dca46839b25dbf186d8a741b7a5c37c05f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074755"
---
# <a name="formatted"></a>Formato

El tipo de datos Con formato es una cadena de texto que se procesa para resolver nombres de propiedades incrustadas, claves de tabla, referencias de variables de entorno y otras subcadenas especiales. Se reconocen las convenciones siguientes para resolver la cadena:

-   Los corchetes ( \[ \] ) o llaves ({ }) sin par que coincidan se quedan en el texto.
-   Si se encuentra una subcadena con el formato \[ *propertyname,* \] se reemplaza por el valor de la propiedad . Si *propertyname* no es un nombre de propiedad válido, la subcadena se resuelve como en blanco. Por ejemplo, la columna Descripción de [la tabla LaunchCondition](launchcondition-table.md) toma una cadena con formato. Si ERRORTXT se ha establecido en "Póngase en contacto con el personal de soporte técnico". a continuación, el texto mostrado para el error de la condición de inicio incluiría esta cadena. Si ERRORTXT no se establece, el texto que se muestra para el error de la condición de inicio sería simplemente "El sistema no cumple los requisitos de instalación".

    

    | Condición | Descripción                                                  |
    |-----------|--------------------------------------------------------------|
    | Versión9X | El sistema no cumple los requisitos de instalación. \[ERRORTXT\] |

    

     

-   Los corchetes se pueden iterar y los nombres de propiedad se resuelven desde dentro hacia fuera. Por ejemplo, suponga que la subcadena \[ \[ PropertyA \] \] aparece en el texto. En primer lugar, se recupera el valor de la propiedad PropertyA. Si el valor es un nombre de propiedad válido, como PropertyB, se recupera el valor de PropertyB y toda la subcadena PropertyA se sustituye por el valor \[ \[ \] \] de PropertyB. Si PropertyA no es un nombre de propiedad válido o si el valor de PropertyA no es un nombre de propiedad válido, la subcadena está en blanco.
-   Si se encuentra una subcadena con el formato environmentvariable, el valor de \[ %  \] la variable de entorno se sustituye por la subcadena.
-   Si se encuentra una subcadena con el formato x, se reemplaza por el carácter x , donde \[ \\  \] *x* es un carácter, sin  ningún procesamiento adicional. Solo se conserva el primer carácter después de la barra diagonal inversa; se quita todo lo demás. Por ejemplo, para incluir un corchete de apertura literal ( \[ ), use \[ \\ \[ \] . El texto \[ \\ \[ \] Texto entre \[ \\ \] \] corchetes se resuelve como \[ Texto entre \] corchetes.
-   Si una subcadena está entre llaves ({ }) y no contiene nombres de propiedad entre corchetes ( ), la subcadena se deja sin modificar, incluidas las \[ \] llaves.
-   Si una subcadena está entre llaves ({ }) y contiene uno o varios nombres de propiedad entre corchetes ( ) , si todos los nombres de propiedad son válidos, el texto (con las sustituciones resueltas) se muestra sin \[ \] llaves.
-   Si se encuentra una subcadena \[ ~ \] del formulario, se reemplaza por el carácter nulo. Se usa para crear cadenas **de caracteres REG MULTI \_ \_ SZ** en la [tabla del Registro](registry-table.md). Tenga en cuenta \[ ~ \] que también se usa para anexar o agregar valores de prefijo a variables de entorno mediante la [tabla Environment](environment-table.md).
-   Si se encuentra una subcadena de la clave de archivo de formulario, se reemplaza por la ruta de acceso completa del archivo, con el valor \[ \#  \] *filekey* [](file-table.md)usado como clave en la tabla File . El valor de filekey permanece en blanco y no se reemplaza por una ruta de acceso hasta que el instalador ejecuta la acción \[ \#  \] [CostInitialize](costinitialize-action.md), la acción [FileCost](filecost-action.md)y [la acción CostFinalize](costfinalize-action.md). El valor de \[ \# *filekey* \] depende del estado de instalación del componente al que pertenece el archivo. Si el componente se ejecuta desde el origen, el valor es la ruta de acceso a la ubicación de origen del archivo. Si el componente se ejecuta localmente, el valor es la ruta de acceso a la ubicación de destino del archivo después de la instalación. Si el componente tiene un estado de acción ausente, se usa el estado instalado del componente para determinar \[ \) .
-   Si se encuentra una subcadena del formulario \[ $ *componentkey,* se reemplaza por el directorio de instalación del \] [](component-table.md)componente, con el valor *componentkey* usado como clave en la tabla Component . El valor de componentkey permanece en blanco y no se reemplaza por un directorio hasta que el instalador ejecuta la acción \[ $  \] [CostInitialize](costinitialize-action.md), la acción [FileCost](filecost-action.md)y [la acción CostFinalize](costfinalize-action.md). El valor de \[ $ *componentkey* \] depende del estado de instalación del componente y de dónde se produzca. En la columna Valor de la [tabla del Registro](registry-table.md), esta subcadena puede hacer referencia al estado de acción o al estado de acción solicitado del componente. En todos los demás casos, esta subcadena hace referencia al estado de acción del componente. Por ejemplo, si el componente se ejecuta desde el origen, el valor es el directorio de origen del archivo. Si el componente se ejecuta localmente, el valor es el directorio de destino después de la instalación. Si el componente no está presente, el valor se deja en blanco. Windows El instalador realiza un seguimiento de la acción y los estados de instalación solicitados de los componentes. Por ejemplo, si un componente ya está instalado, puede tener un estado solicitado de local y un estado de acción null. Para obtener más información sobre cómo comprobar el estado de instalación de los componentes, vea Comprobar la instalación [de características, componentes, archivos](checking-the-installation-of-features-components-files.md).
-   Tenga en cuenta que si un componente ya está instalado y no se vuelve a instalar, quitar o mover durante la instalación actual, el estado de acción del componente es NULL y la clave de componente de cadena se evalúa como \[ $  \] Null.
-   Si es una subcadena con el formato \[ !*se encuentra filekey,* se reemplaza por la ruta de acceso corta completa del archivo, con el valor filekey usado como clave \] en la tabla [File](file-table.md). 

    Esta sintaxis solo es válida cuando se usa en la columna Valor de las tablas Registry o IniFile. Cuando se usa en otras columnas, esta sintaxis se trata igual que \[ \# *filekey* \] .

 

 



