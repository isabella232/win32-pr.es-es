---
description: International Components for Unicode (ICU) es un conjunto de API de globalización de código abierto que se usa ampliamente.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: Componentes internacionales para Unicode (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00a72885b37efebf8de0d5eb60a22fe01dfba4f
ms.sourcegitcommit: 176ef0a00690f849282cb48464c97f6526a82113
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2021
ms.locfileid: "104003233"
---
# <a name="international-components-for-unicode-icu"></a>Componentes internacionales para Unicode (ICU)

International Components for Unicode (ICU) es un conjunto de API de globalización de código abierto que se usa ampliamente. ICU emplea el amplio repositorio de datos de configuración regional común (CLDR) de Unicode como su biblioteca de datos, lo que proporciona compatibilidad de globalización con las aplicaciones de software. Las ICU son muy portátiles y proporcionan a las aplicaciones los mismos resultados en todas las plataformas.

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a>Aspectos destacados de los servicios de API de globalización proporcionados por ICU

-   **Conversión de páginas de códigos**: Convierta datos de texto a o desde Unicode y prácticamente cualquier otro juego de caracteres o codificación. Las tablas de conversión de ICU se basan en los datos de juego de caracteres recopilados por IBM en el transcurso de muchas décadas y es el más completo disponible en cualquier lugar.
-   **Intercalación**: Compare cadenas según las convenciones y los estándares de un determinado idioma, región o país. La intercalación de ICU se basa en el algoritmo de intercalación Unicode más las reglas de comparación específicas de la configuración regional de CLDR.
-   **Formato**: dar formato a números, fechas, horas y importes de divisa según las convenciones de una configuración regional elegida. Esto incluye la traducción de los nombres de mes y día en el idioma seleccionado, la elección de las abreviaturas adecuadas, el orden correcto de los campos, etc. Estos datos también proceden del repositorio de datos de configuración regional común.
-   **Cálculos de tiempo**: se proporcionan varios tipos de calendarios más allá del gregoriano tradicional. Se proporciona un conjunto completo de API de cálculo de zona horaria.
-   **Compatibilidad con Unicode**: ICU realiza un seguimiento estrechamente del estándar Unicode, lo que proporciona un acceso fácil a todas las muchas propiedades de caracteres Unicode, normalización Unicode, doblado de cajas y otras operaciones fundamentales, tal como se especifica en el [estándar Unicode](https://www.unicode.org/).
-   **Expresión regular**: las expresiones regulares de ICU admiten totalmente Unicode a la vez que proporcionan un rendimiento muy competitivo.
-   **Bidi**: compatibilidad con el control de texto que contiene una combinación de datos de izquierda a derecha (Inglés) y de derecha a izquierda (árabe o hebreo).

Para obtener más información, puede visitar el sitio web de ICU: <http://site.icu-project.org/>

## <a name="overview"></a>Información general

En Windows 10 Creators Update, se integró en Windows, lo que permite que las API y los datos de C sean accesibles públicamente.

> [!IMPORTANT]
> La versión de ICU en Windows solo expone las API de C. No expone ninguna de las API de C++. Desafortunadamente, es imposible exponer nunca las API de C++ debido a la falta de una ABI estable en C++.

Para obtener documentación sobre las API de ICU C, consulte la página de documentación de ICU oficial aquí: <http://icu-project.org/apiref/icu4c/index.html#Module>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a>Historial de cambios en la biblioteca ICU en Windows

### <a name="version-1703-creators-update"></a>Versión 1703 (Creators Update)
La biblioteca ICU se agregó por primera vez al sistema operativo Windows 10 en esta versión.
Se agregó como:
- Dos archivos DLL del sistema:
    -   **icuuc.dll** (esta es la biblioteca "común" de ICU)
    -   **icuin.dll** (es la biblioteca "i18n" de ICU)
- Dos archivos de encabezado en el SDK de Windows 10:
    -   **icucommon. h**
    -   **icui18n. h**
- Dos bibliotecas de importación en el SDK de Windows 10:
    -   **icuuc. lib**
    -   **icuin. lib**

### <a name="version-1709-fall-creators-update"></a>Versión 1709 (Fall Creators Update)
Se ha agregado un archivo de encabezado combinado, **ICU. h**, que incluye el contenido de los dos archivos de encabezado anteriores (icucommon. h y icui18n. h), y también cambia el tipo de `UCHAR` a `char16_t` .

### <a name="version-1903-may-2019-update"></a>Versión 1903 (actualización de mayo de 2019)
Se ha agregado una nueva DLL combinada, **icu.dll**, que contiene las bibliotecas "Common" y "i18n". Además, se ha agregado una nueva biblioteca de importación al SDK de Windows 10: **ICU. lib**.

En el futuro, no se agregarán nuevas API a los encabezados antiguos (icucommon. h y icui18n. h) o a las bibliotecas de importación anteriores (icuuc. lib y icuin. lib). Las nuevas API solo se agregarán al encabezado combinado (ICU. h) y a la biblioteca de importación combinada (ICU. lib).

## <a name="getting-started"></a>Introducción

Hay tres pasos principales que debe seguir: (Windows 10 Creators Update o posterior)

<dl>

1. La aplicación debe tener como destino la versión 1703 de Windows 10 (Creators Update) o posterior.

2. Agregue los encabezados:

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   En Windows 10 versión 1709 y versiones posteriores, debe incluir el encabezado combinado en su lugar:

   ``` syntax
   #include <icu.h>
   ```
  
3. Vínculo a las dos bibliotecas:

   -   icuuc. lib
   -   icuin. lib

   En Windows 10 versión 1903 y versiones posteriores, debe usar en su lugar la biblioteca combinada:

   -   ICU. lib

</dl>

A continuación, puede llamar a cualquier API de la C de las bibliotecas que quiera. (No se exponen las API de C++).

> [!IMPORTANT]
> Si usa las bibliotecas de importación heredadas, icuuc. lib y icuin. lib, asegúrese de que estén enumeradas antes de las bibliotecas de paraguas, como onecoreuap. lib o WindowsApp. lib, en la configuración del enlazador de dependencias adicionales (vea la imagen siguiente). De lo contrario, el vinculador se vinculará a ICU. lib, lo que provocará un intento de cargar icu.dll en tiempo de ejecución. Ese archivo DLL está presente solo a partir de la versión 1903. Por lo tanto, si un usuario actualiza el SDK de Windows 10 en una máquina de Windows anterior a la versión 1903, la aplicación no podrá cargarse ni ejecutarse. Para ver un historial de las bibliotecas de ICU en Windows, consulte [historial de cambios en la biblioteca ICU en Windows](#history-of-changes-to-the-icu-library-in-windows).

![ejemplo de ICU](images/icu-example.png)

> [!Note]  
>
> - Esta es la configuración de "todas las plataformas".
> - Para que las aplicaciones Win32 usen ICU, deben llamar primero a [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) .
> - No todos los datos devueltos por las API de ICU se alinearán con el sistema operativo Windows, ya que este trabajo de alineación todavía está en curso. 

## <a name="icu-example-app"></a>Aplicación de ejemplo de ICU

### <a name="example-code-snippet"></a>Fragmento de código de ejemplo

A continuación se muestra un ejemplo que ilustra el uso de las API de ICU desde una aplicación de C++ UWP. (No pretende ser una aplicación independiente completa, sino simplemente un ejemplo de llamada a un método ICU).

En el siguiente ejemplo pequeño se supone que hay métodos **errorMessage** y **OutputMessage** que envían las cadenas al usuario de alguna manera.

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

 

 



