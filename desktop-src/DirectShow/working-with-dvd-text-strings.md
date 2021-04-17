---
description: Trabajar con cadenas de texto de DVD
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: Trabajar con cadenas de texto de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d04a786e46c795f028edbe2b955e71715aaefb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666762"
---
# <a name="working-with-dvd-text-strings"></a><span data-ttu-id="ce3eb-103">Trabajar con cadenas de texto de DVD</span><span class="sxs-lookup"><span data-stu-id="ce3eb-103">Working with DVD Text Strings</span></span>

<span data-ttu-id="ce3eb-104">Algunos discos DVD, especialmente los discos de karaoke, pueden contener una lista de cadenas de texto para complementar el contenido de vídeo o audio.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-104">Some DVD discs, especially karaoke discs, might contain a list of text strings to supplement the video or audio content.</span></span> <span data-ttu-id="ce3eb-105">Estas cadenas de texto contienen metadatos sobre el contenido, como títulos de canciones, nombres de intérpretes, información de género, etc.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-105">These text strings contain metadata about the content, such as song titles, artist names, genre information, and so on.</span></span> <span data-ttu-id="ce3eb-106">Las cadenas de texto pueden estar presentes en más de un idioma.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-106">Text strings can be present in more than one language.</span></span> <span data-ttu-id="ce3eb-107">Estas cadenas son opcionales y muchos discos no las tienen.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-107">These strings are optional, and many discs do not have them.</span></span>

<span data-ttu-id="ce3eb-108">Para recuperar cadenas de texto de un DVD, use la interfaz [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , que se expone mediante el [navegador de DVD](dvd-navigator-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ce3eb-108">To retrieve text strings from a DVD, use the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interface, which is exposed by the [DVD Navigator](dvd-navigator-filter.md).</span></span> <span data-ttu-id="ce3eb-109">En realidad, no es necesario crear un gráfico de reproducción de DVD para recuperar las cadenas de texto.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-109">You do not actually need to build a DVD playback graph to retrieve the text strings.</span></span> <span data-ttu-id="ce3eb-110">Simplemente puede crear el navegador de DVD, establecer el volumen de DVD y, a continuación, llamar a los métodos de cadena de texto pertinentes:</span><span class="sxs-lookup"><span data-stu-id="ce3eb-110">You can simply create the DVD Navigator, set the DVD volume, and then call the relevant text-string methods:</span></span>



| <span data-ttu-id="ce3eb-111">Método</span><span class="sxs-lookup"><span data-stu-id="ce3eb-111">Method</span></span>                                                                                  | <span data-ttu-id="ce3eb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce3eb-112">Description</span></span>                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce3eb-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="ce3eb-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | <span data-ttu-id="ce3eb-114">Obtiene el número de idiomas para los que hay cadenas de texto.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-114">Gets the number of languages for which there are text strings.</span></span>                                                                                                                                  |
| [<span data-ttu-id="ce3eb-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span><span class="sxs-lookup"><span data-stu-id="ce3eb-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | <span data-ttu-id="ce3eb-116">Obtiene información acerca de las cadenas de texto para un idioma.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-116">Gets information about the text strings for one language.</span></span>                                                                                                                                       |
| [<span data-ttu-id="ce3eb-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span><span class="sxs-lookup"><span data-stu-id="ce3eb-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | <span data-ttu-id="ce3eb-118">Obtiene una cadena de texto para un idioma especificado, por índice.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-118">Gets a text string for a specified language, by index.</span></span>                                                                                                                                          |
| [<span data-ttu-id="ce3eb-119">**IDvdInfo2::GetDVDTextStringAsNative**</span><span class="sxs-lookup"><span data-stu-id="ce3eb-119">**IDvdInfo2::GetDVDTextStringAsNative**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | <span data-ttu-id="ce3eb-120">Obtiene una cadena de texto como una matriz de bytes sin formato.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-120">Gets a text string as a raw byte array.</span></span> <span data-ttu-id="ce3eb-121">Use este método si la cadena de texto utiliza una codificación de caracteres no admitida por [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span><span class="sxs-lookup"><span data-stu-id="ce3eb-121">Use this method if the text string uses a character encoding not supported by [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span></span> |



 

<span data-ttu-id="ce3eb-122">Este es el procedimiento básico para obtener cadenas de texto:</span><span class="sxs-lookup"><span data-stu-id="ce3eb-122">Here is the basic procedure for getting text strings:</span></span>

1.  <span data-ttu-id="ce3eb-123">Llame a [**IDvdInfo2:: GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) para buscar el número total de idiomas en los que aparecen las cadenas de texto.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-123">Call [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) to find the total number of languages in which the text strings appear.</span></span> <span data-ttu-id="ce3eb-124">Si el número es cero, significa que el DVD no tiene ninguna cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-124">If the number is zero, it means the DVD does not have any text strings.</span></span> <span data-ttu-id="ce3eb-125">(Es posible que, de hecho, este sea el caso más común).</span><span class="sxs-lookup"><span data-stu-id="ce3eb-125">(This is perhaps the most common case, in fact.)</span></span>
2.  <span data-ttu-id="ce3eb-126">Si el número de idiomas es al menos uno, llame a [**IDvdInfo2:: GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) para obtener información sobre cada idioma.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-126">If the number of languages is at least one, call [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) to get information about each language.</span></span> <span data-ttu-id="ce3eb-127">El idioma se especifica mediante el índice.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-127">The language is specified by index.</span></span> <span data-ttu-id="ce3eb-128">El método devuelve el número total de cadenas de texto en ese idioma, el identificador de configuración regional (**LCID**) del idioma y la codificación de caracteres (Unicode u otros).</span><span class="sxs-lookup"><span data-stu-id="ce3eb-128">The method returns the total number of text strings in that language, the locale identifier (**LCID**) for the language, and the character encoding (Unicode or other).</span></span> <span data-ttu-id="ce3eb-129">Las cadenas de texto de DVD pueden utilizar varios juegos de caracteres diferentes; se muestran en la [**\_ enumeración TextCharSet de DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span><span class="sxs-lookup"><span data-stu-id="ce3eb-129">DVD text strings can use several different character sets; these are listed in [**DVD\_TextCharSet Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span></span>
3.  <span data-ttu-id="ce3eb-130">Para obtener una cadena de texto, llame a [**IDvdInfo2:: GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) o [**IDvdInfo2:: GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span><span class="sxs-lookup"><span data-stu-id="ce3eb-130">To get a text string, call [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) or [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span></span> <span data-ttu-id="ce3eb-131">El primer método devuelve una cadena de caracteres anchos, pero no admite cada juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-131">The first method returns a wide-character string, but does not support every character set.</span></span> <span data-ttu-id="ce3eb-132">El segundo método devuelve una matriz de bytes que contiene los datos de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-132">The second method returns a byte array containing the raw text data.</span></span> <span data-ttu-id="ce3eb-133">En ambos métodos, puede llamar al método con un puntero de búfer **null** para buscar el tamaño de la cadena y el tipo de texto.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-133">For both methods, you can call the method with a **NULL** buffer pointer to find the size of the string and the text type.</span></span> <span data-ttu-id="ce3eb-134">A continuación, asigne un búfer y llame de nuevo al método para obtener la cadena.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-134">Then allocate a buffer and call the method again to get the string.</span></span>

<span data-ttu-id="ce3eb-135">Cada cadena de texto tiene un código de identificador asociado, que indica el significado de la cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-135">Each text string has an associated identifier code, which indicates the meaning of the text string.</span></span> <span data-ttu-id="ce3eb-136">El identificador se devuelve como un valor [**de \_ TextStringType de DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) .</span><span class="sxs-lookup"><span data-stu-id="ce3eb-136">The identifier is returned as a [**DVD\_TextStringType**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) value.</span></span> <span data-ttu-id="ce3eb-137">Hay dos categorías de identificador: *identificadores de estructura* e *identificadores de contenido*.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-137">There are two categories of identifier: *structure identifiers* and *content identifiers*.</span></span> <span data-ttu-id="ce3eb-138">Los identificadores de estructura tienen códigos numéricos en el intervalo de 0x00 a 0x02F.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-138">Structure identifiers have numeric codes in the range 0x00–0x02F.</span></span> <span data-ttu-id="ce3eb-139">Los identificadores de contenido tienen un intervalo de 0x30 y superior.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-139">Content identifiers have a range of 0x30 and higher.</span></span> <span data-ttu-id="ce3eb-140">(La enumeración **\_ TextStringType de DVD** define un subconjunto de los identificadores más comunes, pero los métodos [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) pueden devolver cualquier código de identificador). Un identificador de estructura describe una parte lógica del DVD, como el volumen, el título o la parte del título (PTT).</span><span class="sxs-lookup"><span data-stu-id="ce3eb-140">(The **DVD\_TextStringType** enumeration defines a subset of the most common identifiers, but the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods can return any identifier code.) A structure identifier describes a logical portion of the DVD, such as volume, title, or part of title (PTT).</span></span> <span data-ttu-id="ce3eb-141">Un identificador de contenido indica el significado de una cadena de texto determinada, como el título de la película, el título de la canción o el género.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-141">A content identifier indicates the meaning of a particular text string, such as movie title, song title, or genre.</span></span>

<span data-ttu-id="ce3eb-142">Los identificadores de estructura no tienen cadenas de texto asociadas.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-142">Structure identifiers do not have associated text strings.</span></span> <span data-ttu-id="ce3eb-143">Cuando aparece un identificador de estructura en los datos de la cadena de texto, indica que las siguientes cadenas de texto se aplican a esa parte lógica del DVD, hasta el siguiente identificador de estructura.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-143">When a structure identifier appears in the text-string data, it signals that the following text strings apply to that logical portion of the DVD, up until the next structure identifier.</span></span> <span data-ttu-id="ce3eb-144">La posición de los identificadores de estructura dentro de los datos de texto corresponde a la jerarquía lógica del volumen del DVD.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-144">The position of the structure identifiers within the text data corresponds to the logical hierarchy of the DVD volume.</span></span> <span data-ttu-id="ce3eb-145">Por ejemplo, la primera aparición del identificador de título de la estructura de DVD \_ \_ (0x02) representa el primer título del volumen y la siguiente repetición representa el segundo título.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-145">For example, the first occurrence of the DVD\_Struct\_Title identifier (0x02) represents the first title in the volume, and the next occurrence represents the second title.</span></span>

<span data-ttu-id="ce3eb-146">En la tabla siguiente se muestra cómo se pueden definir las cadenas de texto para un DVD con dos títulos.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-146">The following table shows how the text strings might be defined for a DVD with two titles.</span></span>



| <span data-ttu-id="ce3eb-147">DVD \_ TextStringType</span><span class="sxs-lookup"><span data-stu-id="ce3eb-147">DVD\_TextStringType</span></span>        | <span data-ttu-id="ce3eb-148">Cadena de texto</span><span class="sxs-lookup"><span data-stu-id="ce3eb-148">Text string</span></span>  | <span data-ttu-id="ce3eb-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce3eb-149">Description</span></span>                                    |
|----------------------------|--------------|------------------------------------------------|
| <span data-ttu-id="ce3eb-150">Volumen de la estructura de DVD \_ \_ (0x01)</span><span class="sxs-lookup"><span data-stu-id="ce3eb-150">DVD\_Struct\_Volume (0x01)</span></span> | <span data-ttu-id="ce3eb-151">""</span><span class="sxs-lookup"><span data-stu-id="ce3eb-151">""</span></span>           | <span data-ttu-id="ce3eb-152">Identificador de estructura para todo el disco.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-152">Structure identifier for the entire disc side.</span></span> |
| <span data-ttu-id="ce3eb-153">\_Nombre general de DVD \_ (0x30)</span><span class="sxs-lookup"><span data-stu-id="ce3eb-153">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="ce3eb-154">"Volumen de DVD"</span><span class="sxs-lookup"><span data-stu-id="ce3eb-154">"DVD Volume"</span></span> | <span data-ttu-id="ce3eb-155">Nombre del volumen del DVD.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-155">DVD volume name.</span></span>                               |
| <span data-ttu-id="ce3eb-156">Título de la estructura de DVD \_ \_ (0x02)</span><span class="sxs-lookup"><span data-stu-id="ce3eb-156">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="ce3eb-157">""</span><span class="sxs-lookup"><span data-stu-id="ce3eb-157">""</span></span>           | <span data-ttu-id="ce3eb-158">Identificador de estructura del primer título.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-158">Structure identifier for the first title.</span></span>      |
| <span data-ttu-id="ce3eb-159">\_Nombre general de DVD \_ (0x30)</span><span class="sxs-lookup"><span data-stu-id="ce3eb-159">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="ce3eb-160">"Título 1"</span><span class="sxs-lookup"><span data-stu-id="ce3eb-160">"Title 1"</span></span>    | <span data-ttu-id="ce3eb-161">Nombre del primer título.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-161">Name of the first title.</span></span>                       |
| <span data-ttu-id="ce3eb-162">Título de la estructura de DVD \_ \_ (0x02)</span><span class="sxs-lookup"><span data-stu-id="ce3eb-162">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="ce3eb-163">""</span><span class="sxs-lookup"><span data-stu-id="ce3eb-163">""</span></span>           | <span data-ttu-id="ce3eb-164">Identificador de la estructura del segundo título.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-164">Structure identifier for the second title.</span></span>     |
| <span data-ttu-id="ce3eb-165">\_Nombre general de DVD \_ (0x30)</span><span class="sxs-lookup"><span data-stu-id="ce3eb-165">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="ce3eb-166">"Título 2"</span><span class="sxs-lookup"><span data-stu-id="ce3eb-166">"Title 2"</span></span>    | <span data-ttu-id="ce3eb-167">Nombre del segundo título.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-167">Name of the second title.</span></span>                      |



 

<span data-ttu-id="ce3eb-168">Los métodos [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) y [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) tratan los identificadores de estructura y los identificadores de contenido de la misma.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-168">The [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) and [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) methods treat structure identifiers and content identifiers the same.</span></span> <span data-ttu-id="ce3eb-169">La única diferencia es que para los identificadores de estructura, el búfer de texto asociado está vacío.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-169">The only difference is that for structure identifiers, the associated text buffer is empty.</span></span> <span data-ttu-id="ce3eb-170">Depende de la aplicación realizar un seguimiento de la relación entre las cadenas de texto y las partes lógicas del DVD.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-170">It is up to the application to keep track of the relationship between the text strings and the logical portions of the DVD.</span></span>

<span data-ttu-id="ce3eb-171">En el ejemplo siguiente se muestra cómo obtener cadenas de texto de un DVD.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-171">The following example shows how to get text strings from a DVD.</span></span> <span data-ttu-id="ce3eb-172">En este ejemplo se omiten algunos detalles que requerirá una aplicación real.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-172">This example ignores some details that a real application would require.</span></span> <span data-ttu-id="ce3eb-173">(Por ejemplo, omite los identificadores de estructura). El ejemplo solo está pensado para mostrar la secuencia correcta de llamadas.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-173">(For example, it ignores structure identifiers.) The example is only meant to show the correct sequence of calls.</span></span>


```C++
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }
#define SAFE_ARRAY_DELETE(x) { if (x != NULL) { delete [] x; x = NULL; } }

HRESULT GetDVDTextStrings()
{
    HRESULT hr = S_OK;
    ULONG cLangs = 0;       // Number of languages.
    ULONG cStrings = 0;     // Number of text strings.
    ULONG cchBuffer = 0;    // Buffer size.
    ULONG cchActual = 0;    // Actual string size.

    LCID lcid;              // Locale identifier.
    DVD_TextCharSet     characterSet;
    DVD_TextStringType  stringType;

    WCHAR *pszBuffer = NULL;

    CComPtr<IBaseFilter> pFilter;
    CComPtr<IDvdInfo2> pInfo;
    CComPtr<IDvdControl2> pControl;

    // Set up the DVD Navigator.
    CHECK_HR(hr = pFilter.CoCreateInstance(CLSID_DVDNavigator));
    CHECK_HR(hr = pFilter.QueryInterface(&pInfo));
    CHECK_HR(hr = pFilter.QueryInterface(&pControl));
    CHECK_HR(hr = pControl->SetDVDDirectory(NULL));

    // Find the number of text-string languages.
    CHECK_HR(hr = pInfo->GetDVDTextNumberOfLanguages(&cLangs));
    if (cLangs == 0)
    {
        return S_FALSE; // No text strings.
    }

    // Get information about the 0'th language.
    CHECK_HR(hr = pInfo->GetDVDTextLanguageInfo(
        0, &cStrings, &lcid, &characterSet));

    // First check if this character set is compatible with the 
    // GetDVDTextStringAsUnicode method.

    if (characterSet == DVD_CharSet_Unicode || 
        characterSet == DVD_CharSet_ISO646)
    {
        // Loop through all of the strings.
        for (ULONG i = 0; i < cStrings; i++)
        {
            // Get the i'th string for the 0'th language.

            // Find the required buffer size and the string type.
            CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                0,            // Language index.
                i,            // String index.
                NULL,         // Pass NULL pointer to get the buffer size.
                0,            // Size of the buffer we are passing in.
                &cchBuffer,   // Receives the required buffer size.
                &stringType   // Receives the identifier code.
                ));

            // Skip structure identifiers (0x00 - 0x2F).
            if ((cchBuffer > 0) && (stringType >= 0x30))
            {
                // Allocate a buffer and get the text string.
                pszBuffer = new WCHAR[cchBuffer];
                if (pszBuffer == NULL)
                {
                    CHECK_HR(hr = E_OUTOFMEMORY);
                }

                CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                    0, i, pszBuffer, cchBuffer, &cchActual, &stringType));

                // TODO: Display the text string.

                SAFE_ARRAY_DELETE(pszBuffer);
            }
        }
    }

done:
    SAFE_ARRAY_DELETE(pszBuffer);
    return hr;
}
```



<span data-ttu-id="ce3eb-174">Para obtener información sobre las cadenas de texto de DVD, consulte el [sitio web del Foro de DVD](https://go.microsoft.com/fwlink/?LinkId=8677).</span><span class="sxs-lookup"><span data-stu-id="ce3eb-174">For information on DVD text strings, see the [DVD Forum's Web site](https://go.microsoft.com/fwlink/?LinkId=8677).</span></span>

<span data-ttu-id="ce3eb-175">El método **CDvdCore:: GetDvdText** de la aplicación DVDSample muestra los pasos básicos para enumerar y mostrar cadenas de texto en DVD.</span><span class="sxs-lookup"><span data-stu-id="ce3eb-175">The **CDvdCore::GetDvdText** method in the DVDSample application demonstrates the basic steps in enumerating and displaying DVD text strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce3eb-176">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce3eb-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce3eb-177">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="ce3eb-177">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



