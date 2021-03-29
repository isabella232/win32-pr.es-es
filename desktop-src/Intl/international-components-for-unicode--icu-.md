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
# <a name="international-components-for-unicode-icu"></a><span data-ttu-id="85b07-103">Componentes internacionales para Unicode (ICU)</span><span class="sxs-lookup"><span data-stu-id="85b07-103">International Components for Unicode (ICU)</span></span>

<span data-ttu-id="85b07-104">International Components for Unicode (ICU) es un conjunto de API de globalización de código abierto que se usa ampliamente.</span><span class="sxs-lookup"><span data-stu-id="85b07-104">International Components for Unicode (ICU) is a mature, widely used set of open-source globalization APIs.</span></span> <span data-ttu-id="85b07-105">ICU emplea el amplio repositorio de datos de configuración regional común (CLDR) de Unicode como su biblioteca de datos, lo que proporciona compatibilidad de globalización con las aplicaciones de software.</span><span class="sxs-lookup"><span data-stu-id="85b07-105">ICU utilizes Unicode's vast Common Locale Data Repository (CLDR) as its data library, providing globalization support for software applications.</span></span> <span data-ttu-id="85b07-106">Las ICU son muy portátiles y proporcionan a las aplicaciones los mismos resultados en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="85b07-106">ICU is widely portable and gives applications the same results across on all platforms.</span></span>

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a><span data-ttu-id="85b07-107">Aspectos destacados de los servicios de API de globalización proporcionados por ICU</span><span class="sxs-lookup"><span data-stu-id="85b07-107">Highlights of the Globalization API services provided by ICU</span></span>

-   <span data-ttu-id="85b07-108">**Conversión de páginas de códigos**: Convierta datos de texto a o desde Unicode y prácticamente cualquier otro juego de caracteres o codificación.</span><span class="sxs-lookup"><span data-stu-id="85b07-108">**Code Page Conversion**: Convert text data to or from Unicode and nearly any other character set or encoding.</span></span> <span data-ttu-id="85b07-109">Las tablas de conversión de ICU se basan en los datos de juego de caracteres recopilados por IBM en el transcurso de muchas décadas y es el más completo disponible en cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="85b07-109">ICU's conversion tables are based on charset data collected by IBM over the course of many decades, and is the most complete available anywhere.</span></span>
-   <span data-ttu-id="85b07-110">**Intercalación**: Compare cadenas según las convenciones y los estándares de un determinado idioma, región o país.</span><span class="sxs-lookup"><span data-stu-id="85b07-110">**Collation**: Compare strings according to the conventions and standards of a particular language, region or country.</span></span> <span data-ttu-id="85b07-111">La intercalación de ICU se basa en el algoritmo de intercalación Unicode más las reglas de comparación específicas de la configuración regional de CLDR.</span><span class="sxs-lookup"><span data-stu-id="85b07-111">ICU's collation is based on the Unicode Collation Algorithm plus locale-specific comparison rules from CLDR.</span></span>
-   <span data-ttu-id="85b07-112">**Formato**: dar formato a números, fechas, horas y importes de divisa según las convenciones de una configuración regional elegida.</span><span class="sxs-lookup"><span data-stu-id="85b07-112">**Formatting**: Format numbers, dates, times and currency amounts according the conventions of a chosen locale.</span></span> <span data-ttu-id="85b07-113">Esto incluye la traducción de los nombres de mes y día en el idioma seleccionado, la elección de las abreviaturas adecuadas, el orden correcto de los campos, etc. Estos datos también proceden del repositorio de datos de configuración regional común.</span><span class="sxs-lookup"><span data-stu-id="85b07-113">This includes translating month and day names into the selected language, choosing appropriate abbreviations, ordering fields correctly, etc. This data also comes from the Common Locale Data Repository.</span></span>
-   <span data-ttu-id="85b07-114">**Cálculos de tiempo**: se proporcionan varios tipos de calendarios más allá del gregoriano tradicional.</span><span class="sxs-lookup"><span data-stu-id="85b07-114">**Time Calculations**: Multiple types of calendars are provided beyond the traditional Gregorian.</span></span> <span data-ttu-id="85b07-115">Se proporciona un conjunto completo de API de cálculo de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="85b07-115">A thorough set of time zone calculation APIs are provided.</span></span>
-   <span data-ttu-id="85b07-116">**Compatibilidad con Unicode**: ICU realiza un seguimiento estrechamente del estándar Unicode, lo que proporciona un acceso fácil a todas las muchas propiedades de caracteres Unicode, normalización Unicode, doblado de cajas y otras operaciones fundamentales, tal como se especifica en el [estándar Unicode](https://www.unicode.org/).</span><span class="sxs-lookup"><span data-stu-id="85b07-116">**Unicode Support**: ICU closely tracks the Unicode standard, providing easy access to all of the many Unicode character properties, Unicode Normalization, Case Folding, and other fundamental operations as specified by the [Unicode Standard](https://www.unicode.org/).</span></span>
-   <span data-ttu-id="85b07-117">**Expresión regular**: las expresiones regulares de ICU admiten totalmente Unicode a la vez que proporcionan un rendimiento muy competitivo.</span><span class="sxs-lookup"><span data-stu-id="85b07-117">**Regular Expression**: ICU's regular expressions fully support Unicode while providing very competitive performance.</span></span>
-   <span data-ttu-id="85b07-118">**Bidi**: compatibilidad con el control de texto que contiene una combinación de datos de izquierda a derecha (Inglés) y de derecha a izquierda (árabe o hebreo).</span><span class="sxs-lookup"><span data-stu-id="85b07-118">**Bidi**: Support for handling text containing a mixture of left to right (English) and right to left (Arabic or Hebrew) data.</span></span>

<span data-ttu-id="85b07-119">Para obtener más información, puede visitar el sitio web de ICU: <http://site.icu-project.org/></span><span class="sxs-lookup"><span data-stu-id="85b07-119">For more information, you can visit the ICU website: <http://site.icu-project.org/></span></span>

## <a name="overview"></a><span data-ttu-id="85b07-120">Información general</span><span class="sxs-lookup"><span data-stu-id="85b07-120">Overview</span></span>

<span data-ttu-id="85b07-121">En Windows 10 Creators Update, se integró en Windows, lo que permite que las API y los datos de C sean accesibles públicamente.</span><span class="sxs-lookup"><span data-stu-id="85b07-121">In Windows 10 Creators Update, ICU was integrated into Windows, making the C APIs and data publicly accessible.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85b07-122">La versión de ICU en Windows solo expone las API de C.</span><span class="sxs-lookup"><span data-stu-id="85b07-122">The version of ICU in Windows only exposes the C APIs.</span></span> <span data-ttu-id="85b07-123">No expone ninguna de las API de C++.</span><span class="sxs-lookup"><span data-stu-id="85b07-123">It does not expose any of the C++ APIs.</span></span> <span data-ttu-id="85b07-124">Desafortunadamente, es imposible exponer nunca las API de C++ debido a la falta de una ABI estable en C++.</span><span class="sxs-lookup"><span data-stu-id="85b07-124">Unfortunately, it is impossible to ever expose the C++ APIs due to the lack of a stable ABI in C++.</span></span>

<span data-ttu-id="85b07-125">Para obtener documentación sobre las API de ICU C, consulte la página de documentación de ICU oficial aquí: <http://icu-project.org/apiref/icu4c/index.html#Module></span><span class="sxs-lookup"><span data-stu-id="85b07-125">For documentation on the ICU C APIs, please refer to the official ICU documentation page here: <http://icu-project.org/apiref/icu4c/index.html#Module></span></span>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a><span data-ttu-id="85b07-126">Historial de cambios en la biblioteca ICU en Windows</span><span class="sxs-lookup"><span data-stu-id="85b07-126">History of changes to the ICU library in Windows</span></span>

### <a name="version-1703-creators-update"></a><span data-ttu-id="85b07-127">Versión 1703 (Creators Update)</span><span class="sxs-lookup"><span data-stu-id="85b07-127">Version 1703 (Creators Update)</span></span>
<span data-ttu-id="85b07-128">La biblioteca ICU se agregó por primera vez al sistema operativo Windows 10 en esta versión.</span><span class="sxs-lookup"><span data-stu-id="85b07-128">The ICU library was first added to the Windows 10 OS in this version.</span></span>
<span data-ttu-id="85b07-129">Se agregó como:</span><span class="sxs-lookup"><span data-stu-id="85b07-129">It was added as:</span></span>
- <span data-ttu-id="85b07-130">Dos archivos DLL del sistema:</span><span class="sxs-lookup"><span data-stu-id="85b07-130">Two system DLLs:</span></span>
    -   <span data-ttu-id="85b07-131">**icuuc.dll** (esta es la biblioteca "común" de ICU)</span><span class="sxs-lookup"><span data-stu-id="85b07-131">**icuuc.dll** (this is the ICU "common" library)</span></span>
    -   <span data-ttu-id="85b07-132">**icuin.dll** (es la biblioteca "i18n" de ICU)</span><span class="sxs-lookup"><span data-stu-id="85b07-132">**icuin.dll** (this is the ICU "i18n" library)</span></span>
- <span data-ttu-id="85b07-133">Dos archivos de encabezado en el SDK de Windows 10:</span><span class="sxs-lookup"><span data-stu-id="85b07-133">Two header files in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="85b07-134">**icucommon. h**</span><span class="sxs-lookup"><span data-stu-id="85b07-134">**icucommon.h**</span></span>
    -   <span data-ttu-id="85b07-135">**icui18n. h**</span><span class="sxs-lookup"><span data-stu-id="85b07-135">**icui18n.h**</span></span>
- <span data-ttu-id="85b07-136">Dos bibliotecas de importación en el SDK de Windows 10:</span><span class="sxs-lookup"><span data-stu-id="85b07-136">Two import libs in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="85b07-137">**icuuc. lib**</span><span class="sxs-lookup"><span data-stu-id="85b07-137">**icuuc.lib**</span></span>
    -   <span data-ttu-id="85b07-138">**icuin. lib**</span><span class="sxs-lookup"><span data-stu-id="85b07-138">**icuin.lib**</span></span>

### <a name="version-1709-fall-creators-update"></a><span data-ttu-id="85b07-139">Versión 1709 (Fall Creators Update)</span><span class="sxs-lookup"><span data-stu-id="85b07-139">Version 1709 (Fall Creators Update)</span></span>
<span data-ttu-id="85b07-140">Se ha agregado un archivo de encabezado combinado, **ICU. h**, que incluye el contenido de los dos archivos de encabezado anteriores (icucommon. h y icui18n. h), y también cambia el tipo de `UCHAR` a `char16_t` .</span><span class="sxs-lookup"><span data-stu-id="85b07-140">A combined header file, **icu.h**, was added, which contains the contents of both header files above (icucommon.h and icui18n.h), and also changes the type of `UCHAR` to `char16_t`.</span></span>

### <a name="version-1903-may-2019-update"></a><span data-ttu-id="85b07-141">Versión 1903 (actualización de mayo de 2019)</span><span class="sxs-lookup"><span data-stu-id="85b07-141">Version 1903 (May 2019 Update)</span></span>
<span data-ttu-id="85b07-142">Se ha agregado una nueva DLL combinada, **icu.dll**, que contiene las bibliotecas "Common" y "i18n".</span><span class="sxs-lookup"><span data-stu-id="85b07-142">A new combined DLL, **icu.dll**, was added, which contains both the "common" and "i18n" libraries.</span></span> <span data-ttu-id="85b07-143">Además, se ha agregado una nueva biblioteca de importación al SDK de Windows 10: **ICU. lib**.</span><span class="sxs-lookup"><span data-stu-id="85b07-143">Also, a new import library was added to the Windows 10 SDK: **icu.lib**.</span></span>

<span data-ttu-id="85b07-144">En el futuro, no se agregarán nuevas API a los encabezados antiguos (icucommon. h y icui18n. h) o a las bibliotecas de importación anteriores (icuuc. lib y icuin. lib).</span><span class="sxs-lookup"><span data-stu-id="85b07-144">Going forward, no new APIs will be added to the old headers (icucommon.h and icui18n.h) or to the old import libs (icuuc.lib and icuin.lib).</span></span> <span data-ttu-id="85b07-145">Las nuevas API solo se agregarán al encabezado combinado (ICU. h) y a la biblioteca de importación combinada (ICU. lib).</span><span class="sxs-lookup"><span data-stu-id="85b07-145">New APIs will only be added to the combined header (icu.h) and the combined import lib (icu.lib).</span></span>

## <a name="getting-started"></a><span data-ttu-id="85b07-146">Introducción</span><span class="sxs-lookup"><span data-stu-id="85b07-146">Getting Started</span></span>

<span data-ttu-id="85b07-147">Hay tres pasos principales que debe seguir: (Windows 10 Creators Update o posterior)</span><span class="sxs-lookup"><span data-stu-id="85b07-147">There are three main steps to follow: (Windows 10 Creators Update or higher)</span></span>

<dl>

1. <span data-ttu-id="85b07-148">La aplicación debe tener como destino la versión 1703 de Windows 10 (Creators Update) o posterior.</span><span class="sxs-lookup"><span data-stu-id="85b07-148">Your application needs to target Windows 10 Version 1703 (Creators Update) or higher.</span></span>

2. <span data-ttu-id="85b07-149">Agregue los encabezados:</span><span class="sxs-lookup"><span data-stu-id="85b07-149">Add in the headers:</span></span>

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   <span data-ttu-id="85b07-150">En Windows 10 versión 1709 y versiones posteriores, debe incluir el encabezado combinado en su lugar:</span><span class="sxs-lookup"><span data-stu-id="85b07-150">On Windows 10 Version 1709 and above, you should include the combined header instead:</span></span>

   ``` syntax
   #include <icu.h>
   ```
  
3. <span data-ttu-id="85b07-151">Vínculo a las dos bibliotecas:</span><span class="sxs-lookup"><span data-stu-id="85b07-151">Link to the two libraries:</span></span>

   -   <span data-ttu-id="85b07-152">icuuc. lib</span><span class="sxs-lookup"><span data-stu-id="85b07-152">icuuc.lib</span></span>
   -   <span data-ttu-id="85b07-153">icuin. lib</span><span class="sxs-lookup"><span data-stu-id="85b07-153">icuin.lib</span></span>

   <span data-ttu-id="85b07-154">En Windows 10 versión 1903 y versiones posteriores, debe usar en su lugar la biblioteca combinada:</span><span class="sxs-lookup"><span data-stu-id="85b07-154">On Windows 10 Version 1903 and above, you should use the combined library instead:</span></span>

   -   <span data-ttu-id="85b07-155">ICU. lib</span><span class="sxs-lookup"><span data-stu-id="85b07-155">icu.lib</span></span>

</dl>

<span data-ttu-id="85b07-156">A continuación, puede llamar a cualquier API de la C de las bibliotecas que quiera.</span><span class="sxs-lookup"><span data-stu-id="85b07-156">Then, you can call whatever ICU C API from these libraries you want.</span></span> <span data-ttu-id="85b07-157">(No se exponen las API de C++).</span><span class="sxs-lookup"><span data-stu-id="85b07-157">(No C++ APIs are exposed.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85b07-158">Si usa las bibliotecas de importación heredadas, icuuc. lib y icuin. lib, asegúrese de que estén enumeradas antes de las bibliotecas de paraguas, como onecoreuap. lib o WindowsApp. lib, en la configuración del enlazador de dependencias adicionales (vea la imagen siguiente).</span><span class="sxs-lookup"><span data-stu-id="85b07-158">If you are using the legacy import libraries, icuuc.lib and icuin.lib, ensure they're listed before the umbrella libraries, like onecoreuap.lib or WindowsApp.lib, in the Additional Dependencies Linker setting (see the image below).</span></span> <span data-ttu-id="85b07-159">De lo contrario, el vinculador se vinculará a ICU. lib, lo que provocará un intento de cargar icu.dll en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="85b07-159">Otherwise, the linker will link to icu.lib, which will result in an attempt to load icu.dll during run time.</span></span> <span data-ttu-id="85b07-160">Ese archivo DLL está presente solo a partir de la versión 1903.</span><span class="sxs-lookup"><span data-stu-id="85b07-160">That DLL is present only starting with version 1903.</span></span> <span data-ttu-id="85b07-161">Por lo tanto, si un usuario actualiza el SDK de Windows 10 en una máquina de Windows anterior a la versión 1903, la aplicación no podrá cargarse ni ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="85b07-161">So, if a user upgrades the Windows 10 SDK on a pre-version 1903 Windows machine, the app will fail to load and run.</span></span> <span data-ttu-id="85b07-162">Para ver un historial de las bibliotecas de ICU en Windows, consulte [historial de cambios en la biblioteca ICU en Windows](#history-of-changes-to-the-icu-library-in-windows).</span><span class="sxs-lookup"><span data-stu-id="85b07-162">For a history of the ICU libraries in Windows, see [History of changes to the ICU library in Windows](#history-of-changes-to-the-icu-library-in-windows).</span></span>

![ejemplo de ICU](images/icu-example.png)

> [!Note]  
>
> - <span data-ttu-id="85b07-164">Esta es la configuración de "todas las plataformas".</span><span class="sxs-lookup"><span data-stu-id="85b07-164">This is the configuration for “All Platforms”.</span></span>
> - <span data-ttu-id="85b07-165">Para que las aplicaciones Win32 usen ICU, deben llamar primero a [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="85b07-165">For Win32 apps to use ICU, they need to call [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) first.</span></span>
> - <span data-ttu-id="85b07-166">No todos los datos devueltos por las API de ICU se alinearán con el sistema operativo Windows, ya que este trabajo de alineación todavía está en curso.</span><span class="sxs-lookup"><span data-stu-id="85b07-166">Not all data returned by ICU APIs will align with the Windows OS, as this alignment work is still in progress.</span></span> 

## <a name="icu-example-app"></a><span data-ttu-id="85b07-167">Aplicación de ejemplo de ICU</span><span class="sxs-lookup"><span data-stu-id="85b07-167">ICU Example App</span></span>

### <a name="example-code-snippet"></a><span data-ttu-id="85b07-168">Fragmento de código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="85b07-168">Example code snippet</span></span>

<span data-ttu-id="85b07-169">A continuación se muestra un ejemplo que ilustra el uso de las API de ICU desde una aplicación de C++ UWP.</span><span class="sxs-lookup"><span data-stu-id="85b07-169">The following is an example illustrating the use of ICU APIs from within a C++ UWP application.</span></span> <span data-ttu-id="85b07-170">(No pretende ser una aplicación independiente completa, sino simplemente un ejemplo de llamada a un método ICU).</span><span class="sxs-lookup"><span data-stu-id="85b07-170">(It is not intended to be a full stand-alone application, rather it is just an example of calling an ICU method.)</span></span>

<span data-ttu-id="85b07-171">En el siguiente ejemplo pequeño se supone que hay métodos **errorMessage** y **OutputMessage** que envían las cadenas al usuario de alguna manera.</span><span class="sxs-lookup"><span data-stu-id="85b07-171">The following small example assumes that there are methods **ErrorMessage** and **OutputMessage** that output the strings to the user in some manner.</span></span>

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

 

 



