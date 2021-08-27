---
description: International Components for Unicode (ICU) es un conjunto maduro y ampliamente utilizado de API de globalización de código abierto.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: Componentes internacionales para Unicode (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7fec661b24e352c24abddf687e6b119752e39ce80c12dc409000afa179f1f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107034"
---
# <a name="international-components-for-unicode-icu"></a>Componentes internacionales para Unicode (ICU)

International Components for Unicode (ICU) es un conjunto maduro y ampliamente utilizado de API de globalización de código abierto. ICU usa el gran repositorio de datos de configuración regional común (CLDR) de Unicode como biblioteca de datos, lo que proporciona compatibilidad de globalización para las aplicaciones de software. ICU es ampliamente portátil y proporciona a las aplicaciones los mismos resultados en todas las plataformas.

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a>Aspectos destacados de API de globalización servicios proporcionados por ICU

-   **Conversión de página de** códigos: convierta datos de texto a o desde Unicode y casi cualquier otro juego de caracteres o codificación. Las tablas de conversión de ICU se basan en los datos de juego de caracteres recopilados por IBM a lo largo de muchas décadas y es la más completa disponible en cualquier lugar.
-   **Intercalación:** compare cadenas según las convenciones y estándares de un idioma, región o país determinados. La intercalación de ICU se basa en el algoritmo de intercalación Unicode más reglas de comparación específicas de la configuración regional de CLDR.
-   **Formato:** dar formato a números, fechas, horas y importes de moneda según las convenciones de una configuración regional elegida. Esto incluye traducir nombres de mes y día al idioma seleccionado, elegir las abreviaturas adecuadas, ordenar los campos correctamente, etc. Estos datos también proceden del repositorio de datos de configuración regional común.
-   **Cálculos de tiempo:** se proporcionan varios tipos de calendarios más allá del gregoriano tradicional. Se proporciona un conjunto exhaustivo de API de cálculo de zona horaria.
-   Compatibilidad con **Unicode:** ICU realiza un seguimiento del estándar Unicode, lo que proporciona un acceso sencillo a todas las muchas propiedades de caracteres Unicode, normalización Unicode, plegado de mayúsculas y minúsculas y otras operaciones fundamentales especificadas por el [estándar Unicode](https://www.unicode.org/).
-   **Expresión regular:** las expresiones regulares de ICU son totalmente compatibles con Unicode y proporcionan un rendimiento muy competitivo.
-   **Bidi: compatibilidad** con el control de texto que contiene una combinación de datos de izquierda a derecha (inglés) y de derecha a izquierda (árabe o hebreo).

Para más información, puede visitar el sitio web de ICU: <http://site.icu-project.org/>

## <a name="overview"></a>Información general

En Windows 10 Creators Update, ICU se integró en Windows, haciendo que las API y los datos de C se puedan acceder públicamente.

> [!IMPORTANT]
> La versión de ICU en Windows solo expone las API de C. No expone ninguna de las API de C++. Desafortunadamente, es imposible exponer las API de C++ debido a la falta de una ABI estable en C++.

Para obtener documentación sobre las API de C de ICU, consulte la página de documentación oficial de ICU aquí: <http://icu-project.org/apiref/icu4c/index.html#Module>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a>Historial de cambios en la biblioteca de ICU en Windows

### <a name="version-1703-creators-update"></a>Versión 1703 (Creators Update)
La biblioteca de ICU se agregó por primera vez al sistema Windows 10 sistema operativo en esta versión.
Se agregó como:
- Dos archivos DLL del sistema:
    -   **icuuc.dll** (esta es la biblioteca "común" de ICU)
    -   **icuin.dll** (esta es la biblioteca "i18n" de ICU)
- Dos archivos de encabezado en el SDK Windows 10:
    -   **icucommon.h**
    -   **icui18n.h**
- Dos bibliotecas de importación en Windows 10 SDK:
    -   **icuuc.lib**
    -   **icuin.lib**

### <a name="version-1709-fall-creators-update"></a>Versión 1709 (Fall Creators Update)
Se ha agregado un archivo de encabezado combinado, **icu.h,** que contiene el contenido de los dos archivos de encabezado anteriores (icucommon.h e icui18n.h) y también cambia el tipo de `UCHAR` a `char16_t` .

### <a name="version-1903-may-2019-update"></a>Versión 1903 (actualización de mayo de 2019)
Se ha agregado un nuevo archivo DLLicu.dll **,** que contiene las bibliotecas "common" e "i18n". Además, se ha agregado una nueva biblioteca de importación al SDK Windows 10: **icu.lib**.

En el futuro, no se agregarán nuevas API a los encabezados antiguos (icucommon.h e icui18n.h) ni a las bibliotecas de importación antiguas (icuuc.lib e icuin.lib). Las nuevas API solo se agregarán al encabezado combinado (icu.h) y a la biblioteca de importación combinada (icu.lib).

## <a name="getting-started"></a>Introducción

Hay tres pasos principales que se deben seguir: (Windows 10 Creators Update o superior)

<dl>

1. La aplicación debe tener como destino Windows 10 versión 1703 (Creators Update) o superior.

2. Agregue los encabezados:

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   En Windows 10 versión 1709 y posteriores, debe incluir el encabezado combinado en su lugar:

   ``` syntax
   #include <icu.h>
   ```
  
3. Vínculo a las dos bibliotecas:

   -   icuuc.lib
   -   icuin.lib

   En Windows 10 versión 1903 y posteriores, debe usar la biblioteca combinada en su lugar:

   -   icu.lib

</dl>

A continuación, puede llamar a cualquier API de C de ICU desde estas bibliotecas que desee. (No se expone ninguna API de C++).

> [!IMPORTANT]
> Si usa las bibliotecas de importación heredadas, icuuc.lib e icuin.lib, asegúrese de que aparecen antes que las bibliotecas de paraguas, como onecoreuap.lib o WindowsApp.lib, en la configuración del vinculador de dependencias adicionales (consulte la imagen siguiente). De lo contrario, el vinculador se vinculará a icu.lib, lo que provocará un intento de icu.dll durante el tiempo de ejecución. Ese archivo DLL solo está presente a partir de la versión 1903. Por lo tanto, si un usuario actualiza el SDK de Windows 10 en una máquina de Windows anterior a la versión 1903, la aplicación no se cargará y ejecutará. Para obtener un historial de las bibliotecas de ICU Windows, consulte Historial de cambios en la biblioteca [de ICU en Windows](#history-of-changes-to-the-icu-library-in-windows).

![Ejemplo de icu](images/icu-example.png)

> [!Note]  
>
> - Esta es la configuración de "Todas las plataformas".
> - Para que las aplicaciones Win32 usen ICU, primero deben llamar a [CoInitializeEx.](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) En Windows 10 versión 1903 y posteriores, donde está disponible la biblioteca de ICU combinada (icu.dll/icu.lib), puede omitir la llamada a CoInitializeEx mediante la biblioteca combinada.
> - No todos los datos devueltos por las API de ICU se alinearán con Windows sistema operativo, ya que este trabajo de alineación todavía está en curso. 

## <a name="icu-example-app"></a>Aplicación de ejemplo de ICU

### <a name="example-code-snippet"></a>Fragmento de código de ejemplo

A continuación se muestra un ejemplo que ilustra el uso de las API de ICU desde una aplicación para UWP de C++. (No está pensado para ser una aplicación independiente completa, sino simplemente un ejemplo de llamada a un método ICU).

En el ejemplo pequeño siguiente se supone que hay métodos **ErrorMessage** y **OutputMessage** que devuelven las cadenas al usuario de alguna manera.

``` syntax
// On Windows 10 Creators Update, include the following two headers. With Windows 10 Fall Creators Update and later, you can just include the single header <icu.h>.
#include <icucommon.h>
#include <icui18n.h>

void FormatDateTimeICU()
{
    UErrorCode status = U_ZERO_ERROR;

    // Create a ICU date formatter, using only the 'short date' style format.
    UDateFormat* dateFormatter = udat_open(UDAT_NONE, UDAT_SHORT, nullptr, nullptr, -1, nullptr, 0, &status);

    if (U_FAILURE(status))
    {
        ErrorMessage(L"Failed to create date formatter.");
        return;
    }

    // Get the current date and time.
    UDate currentDateTime = ucal_getNow();

    int32_t stringSize = 0;
    
    // Determine how large the formatted string from ICU would be.
    stringSize = udat_format(dateFormatter, currentDateTime, nullptr, 0, nullptr, &status);

    if (status == U_BUFFER_OVERFLOW_ERROR)
    {
        status = U_ZERO_ERROR;
        // Allocate space for the formatted string.
        auto dateString = std::make_unique<UChar[]>(stringSize + 1);

        // Format the date time into the string.
        udat_format(dateFormatter, currentDateTime, dateString.get(), stringSize + 1, nullptr, &status);

        if (U_FAILURE(status))
        {
            ErrorMessage(L"Failed to format the date time.");
            return;
        }

        // Output the formatted date time.
        OutputMessage(dateString.get());
    }
    else
    {
        ErrorMessage(L"An error occured while trying to determine the size of the formatted date time.");
        return;
    }

    // We need to close the ICU date formatter.
    udat_close(dateFormatter);
}
```

 

 



