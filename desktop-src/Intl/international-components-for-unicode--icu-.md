---
description: International Components for Unicode (ICU) es un conjunto maduro y ampliamente usado de API de globalización de código abierto.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: Componentes internacionales para Unicode (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560a2f344a3024685e17df0f434f8ffa040b5c8b
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349994"
---
# <a name="international-components-for-unicode-icu"></a><span data-ttu-id="9fd58-103">Componentes internacionales para Unicode (ICU)</span><span class="sxs-lookup"><span data-stu-id="9fd58-103">International Components for Unicode (ICU)</span></span>

<span data-ttu-id="9fd58-104">International Components for Unicode (ICU) es un conjunto maduro y ampliamente usado de API de globalización de código abierto.</span><span class="sxs-lookup"><span data-stu-id="9fd58-104">International Components for Unicode (ICU) is a mature, widely used set of open-source globalization APIs.</span></span> <span data-ttu-id="9fd58-105">ICU utiliza el amplio repositorio de datos de configuración regional (CLDR) común de Unicode como biblioteca de datos, lo que proporciona compatibilidad con la globalización de las aplicaciones de software.</span><span class="sxs-lookup"><span data-stu-id="9fd58-105">ICU utilizes Unicode's vast Common Locale Data Repository (CLDR) as its data library, providing globalization support for software applications.</span></span> <span data-ttu-id="9fd58-106">ICU es ampliamente portátil y proporciona a las aplicaciones los mismos resultados en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="9fd58-106">ICU is widely portable and gives applications the same results across on all platforms.</span></span>

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a><span data-ttu-id="9fd58-107">Aspectos destacados de API de globalización servicios proporcionados por ICU</span><span class="sxs-lookup"><span data-stu-id="9fd58-107">Highlights of the Globalization API services provided by ICU</span></span>

-   <span data-ttu-id="9fd58-108">**Conversión de página de** códigos: convierta datos de texto a Unicode o desde este y casi cualquier otro juego de caracteres o codificación.</span><span class="sxs-lookup"><span data-stu-id="9fd58-108">**Code Page Conversion**: Convert text data to or from Unicode and nearly any other character set or encoding.</span></span> <span data-ttu-id="9fd58-109">Las tablas de conversión de ICU se basan en los datos de juego de caracteres recopilados por IBM a lo largo de muchas décadas y es la más completa disponible en cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="9fd58-109">ICU's conversion tables are based on charset data collected by IBM over the course of many decades, and is the most complete available anywhere.</span></span>
-   <span data-ttu-id="9fd58-110">**Intercalación:** compare las cadenas según las convenciones y estándares de un idioma, región o país determinados.</span><span class="sxs-lookup"><span data-stu-id="9fd58-110">**Collation**: Compare strings according to the conventions and standards of a particular language, region or country.</span></span> <span data-ttu-id="9fd58-111">La intercalación de ICU se basa en el algoritmo de intercalación Unicode más reglas de comparación específicas de la configuración regional de CLDR.</span><span class="sxs-lookup"><span data-stu-id="9fd58-111">ICU's collation is based on the Unicode Collation Algorithm plus locale-specific comparison rules from CLDR.</span></span>
-   <span data-ttu-id="9fd58-112">**Formato:** dar formato a números, fechas, horas y cantidades de moneda según las convenciones de una configuración regional elegida.</span><span class="sxs-lookup"><span data-stu-id="9fd58-112">**Formatting**: Format numbers, dates, times and currency amounts according the conventions of a chosen locale.</span></span> <span data-ttu-id="9fd58-113">Esto incluye traducir nombres de mes y día al idioma seleccionado, elegir las abreviaturas adecuadas, ordenar los campos correctamente, etc. Estos datos también proceden del repositorio de datos de configuración regional común.</span><span class="sxs-lookup"><span data-stu-id="9fd58-113">This includes translating month and day names into the selected language, choosing appropriate abbreviations, ordering fields correctly, etc. This data also comes from the Common Locale Data Repository.</span></span>
-   <span data-ttu-id="9fd58-114">**Cálculos de tiempo:** se proporcionan varios tipos de calendarios más allá del gregoriano tradicional.</span><span class="sxs-lookup"><span data-stu-id="9fd58-114">**Time Calculations**: Multiple types of calendars are provided beyond the traditional Gregorian.</span></span> <span data-ttu-id="9fd58-115">Se proporciona un conjunto exhaustivo de API de cálculo de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9fd58-115">A thorough set of time zone calculation APIs are provided.</span></span>
-   <span data-ttu-id="9fd58-116">**Compatibilidad con Unicode:** ICU realiza un seguimiento del estándar Unicode, lo que proporciona un acceso sencillo a todas las muchas propiedades de caracteres Unicode, normalización Unicode, plegado de mayúsculas y minúsculas y otras operaciones fundamentales, tal y como especifica el estándar [Unicode](https://www.unicode.org/).</span><span class="sxs-lookup"><span data-stu-id="9fd58-116">**Unicode Support**: ICU closely tracks the Unicode standard, providing easy access to all of the many Unicode character properties, Unicode Normalization, Case Folding, and other fundamental operations as specified by the [Unicode Standard](https://www.unicode.org/).</span></span>
-   <span data-ttu-id="9fd58-117">**Expresión regular:** las expresiones regulares de ICU son totalmente compatibles con Unicode, a la vez que proporcionan un rendimiento muy competitivo.</span><span class="sxs-lookup"><span data-stu-id="9fd58-117">**Regular Expression**: ICU's regular expressions fully support Unicode while providing very competitive performance.</span></span>
-   <span data-ttu-id="9fd58-118">**Bidi:** compatibilidad con el control de texto que contiene una mezcla de datos de izquierda a derecha (inglés) y de derecha a izquierda (árabe o hebreo).</span><span class="sxs-lookup"><span data-stu-id="9fd58-118">**Bidi**: Support for handling text containing a mixture of left to right (English) and right to left (Arabic or Hebrew) data.</span></span>

<span data-ttu-id="9fd58-119">Para más información, puede visitar el sitio web de ICU: <http://site.icu-project.org/></span><span class="sxs-lookup"><span data-stu-id="9fd58-119">For more information, you can visit the ICU website: <http://site.icu-project.org/></span></span>

## <a name="overview"></a><span data-ttu-id="9fd58-120">Información general</span><span class="sxs-lookup"><span data-stu-id="9fd58-120">Overview</span></span>

<span data-ttu-id="9fd58-121">En Windows 10 Creators Update, ICU se integraba en Windows, lo que hacía que las API y los datos de C se puedan acceder públicamente.</span><span class="sxs-lookup"><span data-stu-id="9fd58-121">In Windows 10 Creators Update, ICU was integrated into Windows, making the C APIs and data publicly accessible.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fd58-122">La versión de ICU en Windows solo expone las API de C.</span><span class="sxs-lookup"><span data-stu-id="9fd58-122">The version of ICU in Windows only exposes the C APIs.</span></span> <span data-ttu-id="9fd58-123">No expone ninguna de las API de C++.</span><span class="sxs-lookup"><span data-stu-id="9fd58-123">It does not expose any of the C++ APIs.</span></span> <span data-ttu-id="9fd58-124">Desafortunadamente, nunca es imposible exponer las API de C++ debido a la falta de una ABI estable en C++.</span><span class="sxs-lookup"><span data-stu-id="9fd58-124">Unfortunately, it is impossible to ever expose the C++ APIs due to the lack of a stable ABI in C++.</span></span>

<span data-ttu-id="9fd58-125">Para obtener documentación sobre las API de C de ICU, consulte la página oficial de documentación de ICU aquí: <http://icu-project.org/apiref/icu4c/index.html#Module></span><span class="sxs-lookup"><span data-stu-id="9fd58-125">For documentation on the ICU C APIs, please refer to the official ICU documentation page here: <http://icu-project.org/apiref/icu4c/index.html#Module></span></span>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a><span data-ttu-id="9fd58-126">Historial de cambios en la biblioteca de ICU en Windows</span><span class="sxs-lookup"><span data-stu-id="9fd58-126">History of changes to the ICU library in Windows</span></span>

### <a name="version-1703-creators-update"></a><span data-ttu-id="9fd58-127">Versión 1703 (Creators Update)</span><span class="sxs-lookup"><span data-stu-id="9fd58-127">Version 1703 (Creators Update)</span></span>
<span data-ttu-id="9fd58-128">La biblioteca de ICU se agregó por primera vez al sistema operativo Windows 10 en esta versión.</span><span class="sxs-lookup"><span data-stu-id="9fd58-128">The ICU library was first added to the Windows 10 OS in this version.</span></span>
<span data-ttu-id="9fd58-129">Se agregó como:</span><span class="sxs-lookup"><span data-stu-id="9fd58-129">It was added as:</span></span>
- <span data-ttu-id="9fd58-130">Dos archivos DLL del sistema:</span><span class="sxs-lookup"><span data-stu-id="9fd58-130">Two system DLLs:</span></span>
    -   <span data-ttu-id="9fd58-131">**icuuc.dll** (esta es la biblioteca "común" de ICU)</span><span class="sxs-lookup"><span data-stu-id="9fd58-131">**icuuc.dll** (this is the ICU "common" library)</span></span>
    -   <span data-ttu-id="9fd58-132">**icuin.dll** (esta es la biblioteca "i18n" de ICU)</span><span class="sxs-lookup"><span data-stu-id="9fd58-132">**icuin.dll** (this is the ICU "i18n" library)</span></span>
- <span data-ttu-id="9fd58-133">Dos archivos de encabezado en Windows 10 SDK:</span><span class="sxs-lookup"><span data-stu-id="9fd58-133">Two header files in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="9fd58-134">**icucommon.h**</span><span class="sxs-lookup"><span data-stu-id="9fd58-134">**icucommon.h**</span></span>
    -   <span data-ttu-id="9fd58-135">**icui18n.h**</span><span class="sxs-lookup"><span data-stu-id="9fd58-135">**icui18n.h**</span></span>
- <span data-ttu-id="9fd58-136">Dos bibliotecas de importación en Windows 10 SDK:</span><span class="sxs-lookup"><span data-stu-id="9fd58-136">Two import libs in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="9fd58-137">**icuuc.lib**</span><span class="sxs-lookup"><span data-stu-id="9fd58-137">**icuuc.lib**</span></span>
    -   <span data-ttu-id="9fd58-138">**icuin.lib**</span><span class="sxs-lookup"><span data-stu-id="9fd58-138">**icuin.lib**</span></span>

### <a name="version-1709-fall-creators-update"></a><span data-ttu-id="9fd58-139">Versión 1709 (Fall Creators Update)</span><span class="sxs-lookup"><span data-stu-id="9fd58-139">Version 1709 (Fall Creators Update)</span></span>
<span data-ttu-id="9fd58-140">Se ha agregado un archivo de encabezado combinado, **icu.h**, que contiene el contenido de los dos archivos de encabezado anteriores (icucommon.h e icui18n.h), y también cambia el tipo de `UCHAR` a `char16_t` .</span><span class="sxs-lookup"><span data-stu-id="9fd58-140">A combined header file, **icu.h**, was added, which contains the contents of both header files above (icucommon.h and icui18n.h), and also changes the type of `UCHAR` to `char16_t`.</span></span>

### <a name="version-1903-may-2019-update"></a><span data-ttu-id="9fd58-141">Versión 1903 (actualización de mayo de 2019)</span><span class="sxs-lookup"><span data-stu-id="9fd58-141">Version 1903 (May 2019 Update)</span></span>
<span data-ttu-id="9fd58-142">Se ha agregado un nuevo archivo DLL combinado, **icu.dll**, que contiene las bibliotecas "common" e "i18n".</span><span class="sxs-lookup"><span data-stu-id="9fd58-142">A new combined DLL, **icu.dll**, was added, which contains both the "common" and "i18n" libraries.</span></span> <span data-ttu-id="9fd58-143">Además, se ha agregado una nueva biblioteca de importación al SDK de Windows 10: **icu.lib**.</span><span class="sxs-lookup"><span data-stu-id="9fd58-143">Also, a new import library was added to the Windows 10 SDK: **icu.lib**.</span></span>

<span data-ttu-id="9fd58-144">En el futuro, no se agregarán nuevas API a los encabezados antiguos (icucommon.h e icui18n.h) ni a las bibliotecas de importación antiguas (icuuc.lib e icuin.lib).</span><span class="sxs-lookup"><span data-stu-id="9fd58-144">Going forward, no new APIs will be added to the old headers (icucommon.h and icui18n.h) or to the old import libs (icuuc.lib and icuin.lib).</span></span> <span data-ttu-id="9fd58-145">Las nuevas API solo se agregarán al encabezado combinado (icu.h) y a la biblioteca de importación combinada (icu.lib).</span><span class="sxs-lookup"><span data-stu-id="9fd58-145">New APIs will only be added to the combined header (icu.h) and the combined import lib (icu.lib).</span></span>

## <a name="getting-started"></a><span data-ttu-id="9fd58-146">Introducción</span><span class="sxs-lookup"><span data-stu-id="9fd58-146">Getting Started</span></span>

<span data-ttu-id="9fd58-147">Hay tres pasos principales que se deben seguir: (Windows 10 Creators Update o superior)</span><span class="sxs-lookup"><span data-stu-id="9fd58-147">There are three main steps to follow: (Windows 10 Creators Update or higher)</span></span>

<dl>

1. <span data-ttu-id="9fd58-148">La aplicación debe tener como destino Windows 10 versión 1703 (Creators Update) o superior.</span><span class="sxs-lookup"><span data-stu-id="9fd58-148">Your application needs to target Windows 10 Version 1703 (Creators Update) or higher.</span></span>

2. <span data-ttu-id="9fd58-149">Agregue los encabezados:</span><span class="sxs-lookup"><span data-stu-id="9fd58-149">Add in the headers:</span></span>

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   <span data-ttu-id="9fd58-150">En Windows 10 versión 1709 y posteriores, debe incluir el encabezado combinado en su lugar:</span><span class="sxs-lookup"><span data-stu-id="9fd58-150">On Windows 10 Version 1709 and above, you should include the combined header instead:</span></span>

   ``` syntax
   #include <icu.h>
   ```
  
3. <span data-ttu-id="9fd58-151">Vínculo a las dos bibliotecas:</span><span class="sxs-lookup"><span data-stu-id="9fd58-151">Link to the two libraries:</span></span>

   -   <span data-ttu-id="9fd58-152">icuuc.lib</span><span class="sxs-lookup"><span data-stu-id="9fd58-152">icuuc.lib</span></span>
   -   <span data-ttu-id="9fd58-153">icuin.lib</span><span class="sxs-lookup"><span data-stu-id="9fd58-153">icuin.lib</span></span>

   <span data-ttu-id="9fd58-154">En Windows 10 versión 1903 y posteriores, debe usar la biblioteca combinada en su lugar:</span><span class="sxs-lookup"><span data-stu-id="9fd58-154">On Windows 10 Version 1903 and above, you should use the combined library instead:</span></span>

   -   <span data-ttu-id="9fd58-155">icu.lib</span><span class="sxs-lookup"><span data-stu-id="9fd58-155">icu.lib</span></span>

</dl>

<span data-ttu-id="9fd58-156">A continuación, puede llamar a cualquier API de C de ICU desde estas bibliotecas que desee.</span><span class="sxs-lookup"><span data-stu-id="9fd58-156">Then, you can call whatever ICU C API from these libraries you want.</span></span> <span data-ttu-id="9fd58-157">(No se expone ninguna API de C++).</span><span class="sxs-lookup"><span data-stu-id="9fd58-157">(No C++ APIs are exposed.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fd58-158">Si usa las bibliotecas de importación heredadas, icuuc.lib e icuin.lib, asegúrese de que aparecen antes que las bibliotecas paraguas, como onecoreuap.lib o WindowsApp.lib, en la configuración del vinculador de dependencias adicionales (consulte la imagen siguiente).</span><span class="sxs-lookup"><span data-stu-id="9fd58-158">If you are using the legacy import libraries, icuuc.lib and icuin.lib, ensure they're listed before the umbrella libraries, like onecoreuap.lib or WindowsApp.lib, in the Additional Dependencies Linker setting (see the image below).</span></span> <span data-ttu-id="9fd58-159">De lo contrario, el vinculador se vinculará a icu.lib, lo que provocará un intento de icu.dll durante el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="9fd58-159">Otherwise, the linker will link to icu.lib, which will result in an attempt to load icu.dll during run time.</span></span> <span data-ttu-id="9fd58-160">Ese archivo DLL solo está presente a partir de la versión 1903.</span><span class="sxs-lookup"><span data-stu-id="9fd58-160">That DLL is present only starting with version 1903.</span></span> <span data-ttu-id="9fd58-161">Por lo tanto, si un usuario actualiza el SDK de Windows 10 en una máquina Windows anterior a la versión 1903, la aplicación no se podrá cargar y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="9fd58-161">So, if a user upgrades the Windows 10 SDK on a pre-version 1903 Windows machine, the app will fail to load and run.</span></span> <span data-ttu-id="9fd58-162">Para obtener un historial de las bibliotecas de ICU en Windows, consulte Historial de cambios [en la biblioteca de ICU en Windows.](#history-of-changes-to-the-icu-library-in-windows)</span><span class="sxs-lookup"><span data-stu-id="9fd58-162">For a history of the ICU libraries in Windows, see [History of changes to the ICU library in Windows](#history-of-changes-to-the-icu-library-in-windows).</span></span>

![Ejemplo de icu](images/icu-example.png)

> [!Note]  
>
> - <span data-ttu-id="9fd58-164">Esta es la configuración de "Todas las plataformas".</span><span class="sxs-lookup"><span data-stu-id="9fd58-164">This is the configuration for “All Platforms”.</span></span>
> - <span data-ttu-id="9fd58-165">Para que las aplicaciones Win32 usen ICU, primero deben llamar a [CoInitializeEx.](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)</span><span class="sxs-lookup"><span data-stu-id="9fd58-165">For Win32 apps to use ICU, they need to call [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) first.</span></span> <span data-ttu-id="9fd58-166">En Windows 10 versión 1903 y posteriores, donde la biblioteca de ICU combinada (icu.dll/icu.lib) está disponible, puede omitir la llamada a CoInitializeEx mediante la biblioteca combinada.</span><span class="sxs-lookup"><span data-stu-id="9fd58-166">On Windows 10 version 1903 and above, where the combined ICU library (icu.dll/icu.lib) is available, you can omit the CoInitializeEx call by using the combined library.</span></span>
> - <span data-ttu-id="9fd58-167">No todos los datos devueltos por las API de ICU se alinearán con el sistema operativo Windows, ya que este trabajo de alineación todavía está en curso.</span><span class="sxs-lookup"><span data-stu-id="9fd58-167">Not all data returned by ICU APIs will align with the Windows OS, as this alignment work is still in progress.</span></span> 

## <a name="icu-example-app"></a><span data-ttu-id="9fd58-168">Aplicación de ejemplo de ICU</span><span class="sxs-lookup"><span data-stu-id="9fd58-168">ICU Example App</span></span>

### <a name="example-code-snippet"></a><span data-ttu-id="9fd58-169">Fragmento de código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9fd58-169">Example code snippet</span></span>

<span data-ttu-id="9fd58-170">A continuación se muestra un ejemplo que ilustra el uso de las API de ICU desde una aplicación para UWP de C++.</span><span class="sxs-lookup"><span data-stu-id="9fd58-170">The following is an example illustrating the use of ICU APIs from within a C++ UWP application.</span></span> <span data-ttu-id="9fd58-171">(No pretende ser una aplicación independiente completa, sino simplemente un ejemplo de llamada a un método de ICU).</span><span class="sxs-lookup"><span data-stu-id="9fd58-171">(It is not intended to be a full stand-alone application, rather it is just an example of calling an ICU method.)</span></span>

<span data-ttu-id="9fd58-172">En el ejemplo pequeño siguiente se supone que hay métodos **ErrorMessage** y **OutputMessage** que devuelven las cadenas al usuario de alguna manera.</span><span class="sxs-lookup"><span data-stu-id="9fd58-172">The following small example assumes that there are methods **ErrorMessage** and **OutputMessage** that output the strings to the user in some manner.</span></span>

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

 

 



