---
description: Los datos de rendimiento contienen valores de índice que se usan para buscar los nombres y el texto de ayuda de cada objeto y contador registrados.
ms.assetid: 9ddd1672-61cf-41c2-bec0-0d2b775bf970
title: Recuperar nombres de contadores y texto de ayuda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b49f852e6af22dc2ec31d341ee6176913f98e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720528"
---
# <a name="retrieving-counter-names-and-help-text"></a><span data-ttu-id="f2130-103">Recuperar nombres de contadores y texto de ayuda</span><span class="sxs-lookup"><span data-stu-id="f2130-103">Retrieving Counter Names and Help Text</span></span>

<span data-ttu-id="f2130-104">Los datos de rendimiento contienen valores de índice que se usan para buscar los nombres y el texto de ayuda de cada objeto y contador registrados.</span><span class="sxs-lookup"><span data-stu-id="f2130-104">The performance data contains index values that you use to locate the names and help text for each registered object and counter.</span></span> <span data-ttu-id="f2130-105">Los miembros **ObjectNameTitleIndex** y **ObjectHelpTitleIndex** de la estructura de [**\_ \_ tipo de objeto Perf**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) contienen los valores de índice para el nombre de objeto y el texto de ayuda, respectivamente, y los miembros **CounterNameTitleIndex** y **CounterHelpTitleIndex** de la estructura de [**\_ \_ definición de contadores de rendimiento**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) contienen los valores de índice en el nombre de contador y el texto de ayuda, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f2130-105">The **ObjectNameTitleIndex** and **ObjectHelpTitleIndex** members of the [**PERF\_OBJECT\_TYPE**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) structure contain the index values to the object name and help text, respectively, and the **CounterNameTitleIndex** and **CounterHelpTitleIndex** members of the [**PERF\_COUNTER\_DEFINITION**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) structure contain the index values to the counter name and help text, respectively.</span></span>

<span data-ttu-id="f2130-106">Para recuperar los nombres o el texto de ayuda, llame a la función [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) .</span><span class="sxs-lookup"><span data-stu-id="f2130-106">To retrieve the names or help text, call the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function.</span></span> <span data-ttu-id="f2130-107">Establezca el parámetro *hKey* en una de las siguientes claves predefinidas.</span><span class="sxs-lookup"><span data-stu-id="f2130-107">Set the *hKey* parameter to one of the following predefined keys.</span></span> <span data-ttu-id="f2130-108">Normalmente, se usaría la clave **HKEY \_ performance \_ NLSTEXT** , por lo que no es necesario determinar el identificador de idioma del usuario.</span><span class="sxs-lookup"><span data-stu-id="f2130-108">Typically, you would use the **HKEY\_PERFORMANCE\_NLSTEXT** key, so you do not have to determine the user's language identifier.</span></span>



| <span data-ttu-id="f2130-109">Clave</span><span class="sxs-lookup"><span data-stu-id="f2130-109">Key</span></span>                            | <span data-ttu-id="f2130-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2130-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2130-111">**\_datos de rendimiento de HKEY \_**</span><span class="sxs-lookup"><span data-stu-id="f2130-111">**HKEY\_PERFORMANCE\_DATA**</span></span>    | <span data-ttu-id="f2130-112">Las cadenas de consulta se basan en el valor del identificador de idioma que se especifica en el parámetro *lpValueName* .</span><span class="sxs-lookup"><span data-stu-id="f2130-112">Query strings based on the language identifier value that you specify in the *lpValueName* parameter.</span></span> <span data-ttu-id="f2130-113">Establezca el parámetro *lpValueName* en "Counter &lt; langid &gt; " o "Help &lt; langid &gt; " para recuperar los nombres o el texto de ayuda, respectivamente, donde " &lt; langid &gt; " es el identificador de idioma del sistema con formato de **número hexadecimal de 3 dígitos rellenado con ceros**.</span><span class="sxs-lookup"><span data-stu-id="f2130-113">Set *lpValueName* parameter to either "Counter &lt;langid&gt;" or "Help &lt;langid&gt;" to retrieve the names or help text, respectively, where "&lt;langid&gt;" is the system language identifier formatted as **zero-padded 3-digit hex number**.</span></span> <span data-ttu-id="f2130-114">El identificador de idioma es opcional.</span><span class="sxs-lookup"><span data-stu-id="f2130-114">The language identifier is optional.</span></span> <span data-ttu-id="f2130-115">Si no especifica un identificador de idioma, la función devuelve cadenas en inglés.</span><span class="sxs-lookup"><span data-stu-id="f2130-115">If you do not specify a language identifier, the function returns English strings.</span></span> <span data-ttu-id="f2130-116">Compruebe la `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` clave del registro para obtener la lista de idiomas disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f2130-116">Check the `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` registry key for the list of languages available on your system.</span></span><br/><span data-ttu-id="f2130-117">Para recuperar texto en la mayoría de los idiomas, especifique solo el identificador de idioma principal.</span><span class="sxs-lookup"><span data-stu-id="f2130-117">To retrieve text in most languages, specify the primary language identifier only.</span></span> <span data-ttu-id="f2130-118">Por ejemplo, para recuperar cadenas en inglés, especifique el identificador de idioma como 009, no 1033 para inglés (EE. UU.).</span><span class="sxs-lookup"><span data-stu-id="f2130-118">For example, to retrieve English strings, specify the language identifier as 009, not 1033 for English-US.</span></span><br/><span data-ttu-id="f2130-119">Para recuperar el texto en chino y portugués, especifique los identificadores principal y de subidioma.</span><span class="sxs-lookup"><span data-stu-id="f2130-119">To retrieve Chinese and Portuguese text, specify both the primary and sublanguage identifiers.</span></span><br/><span data-ttu-id="f2130-120">**Windows Server 2003 y Windows XP:** Especifique solo el identificador de idioma principal para portugués.</span><span class="sxs-lookup"><span data-stu-id="f2130-120">**Windows Server 2003 and Windows XP:** Specify only the primary language identifier for Portuguese.</span></span><br/><span data-ttu-id="f2130-121">**Windows 10**: el texto "Help &lt; langid &gt; " con el identificador de idioma personalizado siempre devuelve cadenas en inglés, aunque el valor localizado todavía se puede recuperar del registro mediante la clave mencionada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f2130-121">**Windows 10**: "Help &lt;langid&gt;" text with custom language identifier always returns strings in English, although localized value can still be retrieved from the registry using the aforementioned key.</span></span><br/><br/> |
| <span data-ttu-id="f2130-122">**HKEY \_ performance \_ NLSTEXT**</span><span class="sxs-lookup"><span data-stu-id="f2130-122">**HKEY\_PERFORMANCE\_NLSTEXT**</span></span> | <span data-ttu-id="f2130-123">Cadenas de consulta basadas en el idioma predeterminado de la interfaz de usuario del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="f2130-123">Query strings based on the default UI language of the current user.</span></span> <span data-ttu-id="f2130-124">Establezca el parámetro *lpValueName* en "Counter" o "Help" para recuperar los nombres o el texto de ayuda, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f2130-124">Set the *lpValueName* parameter to either "Counter" or "Help" to retrieve the names or help text, respectively.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f2130-125">**HKEY \_ - \_ texto de rendimiento**</span><span class="sxs-lookup"><span data-stu-id="f2130-125">**HKEY\_PERFORMANCE\_TEXT**</span></span>    | <span data-ttu-id="f2130-126">Consultar cadenas en inglés.</span><span class="sxs-lookup"><span data-stu-id="f2130-126">Query English strings.</span></span> <span data-ttu-id="f2130-127">Establezca el parámetro *lpValueName* en "Counter" o "Help" para recuperar los nombres o el texto de ayuda, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f2130-127">Set the *lpValueName* parameter to either "Counter" or "Help" to retrieve the names or help text, respectively.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |





<span data-ttu-id="f2130-128">La función devuelve los datos como una lista de cadenas.</span><span class="sxs-lookup"><span data-stu-id="f2130-128">The function returns the data as a list of strings.</span></span> <span data-ttu-id="f2130-129">Cada cadena termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="f2130-129">Each string is null-terminated.</span></span> <span data-ttu-id="f2130-130">La última cadena va seguida de un terminador nulo adicional.</span><span class="sxs-lookup"><span data-stu-id="f2130-130">The last string is followed by an additional null terminator.</span></span> <span data-ttu-id="f2130-131">Las cadenas se enumeran en pares.</span><span class="sxs-lookup"><span data-stu-id="f2130-131">The strings are listed in pairs.</span></span> <span data-ttu-id="f2130-132">La primera cadena de cada par es el índice y la segunda cadena es el texto asociado con el índice.</span><span class="sxs-lookup"><span data-stu-id="f2130-132">The first string of each pair is the index, and the second string is the text associated with the index.</span></span> <span data-ttu-id="f2130-133">Los datos del contador solo usan índices con números pares, mientras que los datos de ayuda usan índices impares.</span><span class="sxs-lookup"><span data-stu-id="f2130-133">The counter data uses only even-numbered indexes, while the help data uses odd-numbered indexes.</span></span> <span data-ttu-id="f2130-134">Los pares se devuelven en el orden de índice creciente.</span><span class="sxs-lookup"><span data-stu-id="f2130-134">The pairs are returned in increasing index order.</span></span>

<span data-ttu-id="f2130-135">En las listas siguientes se muestran ejemplos de datos de contadores y de ayuda.</span><span class="sxs-lookup"><span data-stu-id="f2130-135">The following lists show examples of counter and help data.</span></span> <span data-ttu-id="f2130-136">Al incrementar el valor de índice de un contador dado en uno, se obtiene el índice del texto de ayuda del contador.</span><span class="sxs-lookup"><span data-stu-id="f2130-136">Incrementing a given counter's index value by one gives you the index to the counter's help text.</span></span> <span data-ttu-id="f2130-137">Por ejemplo, 7 es el índice de ayuda asociado al contador index 6.</span><span class="sxs-lookup"><span data-stu-id="f2130-137">For example, 7 is the help index associated with counter index 6.</span></span>

<span data-ttu-id="f2130-138">Pares de datos del contador.</span><span class="sxs-lookup"><span data-stu-id="f2130-138">Counter data pairs.</span></span>

<dl> <span data-ttu-id="f2130-139">2 sistema 4 memoria 6% de tiempo de procesador</span><span class="sxs-lookup"><span data-stu-id="f2130-139">2 System 4 Memory 6 % Processor Time</span></span>
</dl>

<span data-ttu-id="f2130-140">Pares de datos de la ayuda.</span><span class="sxs-lookup"><span data-stu-id="f2130-140">Help data pairs.</span></span>

<dl> <span data-ttu-id="f2130-141">3 el tipo de objeto del sistema incluye los contadores que... 5 el tipo de objeto de memoria incluye los contadores que... 7 el tiempo del procesador se expresa como un porcentaje de...</span><span class="sxs-lookup"><span data-stu-id="f2130-141">3 The System object type includes those counters that ... 5 The Memory object type includes those counters that ... 7 Processor Time is expressed as a percentage of the ...</span></span>
</dl>

<span data-ttu-id="f2130-142">Tenga en cuenta que el primer par de cadenas de los datos del contador no identifica un nombre de contador y se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="f2130-142">Note that the first pair of strings in the counter data do not identify a counter name and can be ignored.</span></span> <span data-ttu-id="f2130-143">El número de índice del primer par es 1 y la cadena es una cadena numérica que representa el valor de índice máximo para los contadores del sistema.</span><span class="sxs-lookup"><span data-stu-id="f2130-143">The index number of the first pair is 1 and the string is a numeric string that represents the maximum index value for system counters.</span></span>

<span data-ttu-id="f2130-144">Para obtener información sobre cómo un proveedor carga el nombre y el texto de ayuda, vea [Agregar nombres y descripciones de contadores al registro](adding-counter-names-and-descriptions-to-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="f2130-144">For information on how a provider loads the name and help text, see [Adding Counter Names and Descriptions to the Registry](adding-counter-names-and-descriptions-to-the-registry.md).</span></span>

<span data-ttu-id="f2130-145">No hay información en el texto que indica si el texto identifica un contador o un objeto de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f2130-145">There is no information in the text that indicates if the text identifies a counter or performance object.</span></span> <span data-ttu-id="f2130-146">La única manera de determinar esto, o la relación entre contadores y objetos, es consultar los datos de rendimiento en sí.</span><span class="sxs-lookup"><span data-stu-id="f2130-146">The only way to determine this, or the relationship between counters and objects, is to query the performance data itself.</span></span> <span data-ttu-id="f2130-147">Por ejemplo, si desea mostrar una lista de objetos y sus contadores en una interfaz de usuario, debe recuperar los datos de rendimiento y, a continuación, utilizar los valores de índice para analizar los datos de texto de las cadenas.</span><span class="sxs-lookup"><span data-stu-id="f2130-147">For example, if you want to display a list of objects and their counters in a user interface, you must retrieve the performance data, and then use the index values to parse the text data for the strings.</span></span> <span data-ttu-id="f2130-148">Para ver un ejemplo que lo hace, vea [Mostrar los nombres de objeto, instancia y contador](displaying-object-instance-and-counter-names.md).</span><span class="sxs-lookup"><span data-stu-id="f2130-148">For an example that does this, see [Displaying Object, Instance, and Counter Names](displaying-object-instance-and-counter-names.md).</span></span>

<span data-ttu-id="f2130-149">En el ejemplo siguiente se muestra cómo usar **HKEY \_ performance \_ NLSTEXT** para recuperar el contador y el texto de ayuda y crear una tabla para el acceso posterior.</span><span class="sxs-lookup"><span data-stu-id="f2130-149">The following example shows how to use **HKEY\_PERFORMANCE\_NLSTEXT** to retrieve the counter and help text and build a table for subsequent access.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

LPWSTR GetText(LPWSTR pwszSource);
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets);
DWORD GetNumberOfTextEntries(LPWSTR pwszSource);
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets);

void wmain(void)
{
    LPWSTR pCounterTextHead = NULL; // Head of the MULTI_SZ buffer that contains the Counter text.
    LPWSTR pHelpTextHead = NULL;    // Head of the MULTI_SZ buffer that contains the Help text.
    LPDWORD pTextOffsets = NULL;    // Array of DWORDS that contain the offsets to the text in
                                    // pCounterTextHead and pHelpTextHead. The text index
                                    // values mirror the array index.
    DWORD dwNumberOfOffsets = 0;    // Number of elements in the pTextOffsets array.


    pCounterTextHead = GetText(L"Counter");
    if (NULL == pCounterTextHead)
    {
        wprintf(L"GetText(L\"Counter\") failed.\n");
        goto cleanup;
    }

    pHelpTextHead = GetText(L"Help");
    if (NULL == pHelpTextHead)
    {
        wprintf(L"GetText(L\"Help\") failed.\n");
        goto cleanup;
    }

    if (BuildTextTable(pCounterTextHead, pHelpTextHead, &pTextOffsets, &dwNumberOfOffsets))
    {
        PrintCounterAndHelpText(pCounterTextHead, pHelpTextHead, pTextOffsets, dwNumberOfOffsets);
    }
    else
    {
        wprintf(L"BuildTextTable failed.\n");
    }

cleanup:

    if (pCounterTextHead)
        free(pCounterTextHead);

    if (pHelpTextHead)
        free(pHelpTextHead);

    if (pTextOffsets)
        free(pTextOffsets);

    // You do not need to call RegCloseKey if you are only
    // retrieving names and help text.
}


// Get the text based on the source value. This function uses the
// HKEY_PERFORMANCE_NLSTEXT key to get the strings.
LPWSTR GetText(LPWSTR pwszSource)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    LONG status = ERROR_SUCCESS;

    // Query the size of the text data so you can allocate the buffer.
    status = RegQueryValueEx(HKEY_PERFORMANCE_NLSTEXT, pwszSource, NULL, NULL, NULL, &dwBufferSize);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed getting required buffer size. Error is 0x%x.\n", status);
        goto cleanup;
    }

    // Allocate the text buffer and query the text.
    pBuffer = (LPWSTR)malloc(dwBufferSize);
    if (pBuffer)
    {
        status = RegQueryValueEx(HKEY_PERFORMANCE_NLSTEXT, pwszSource, NULL, NULL, (LPBYTE)pBuffer, &dwBufferSize);
        if (ERROR_SUCCESS != status)
        {
            wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
            free(pBuffer);
            pBuffer = NULL;
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"malloc failed to allocate memory.\n");
    }

cleanup:

    return pBuffer;
}


// Build a table of offsets into the counter and help text buffers. Use the index
// values from the performance data queries to access the offsets.
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets)
{
    BOOL fSuccess = FALSE;
    LPWSTR pwszCounterText = NULL;  // Used to cycle through the Counter text
    LPWSTR pwszHelpText = NULL;     // Used to cycle through the Help text
    LPDWORD pOffsets = NULL;
    DWORD dwCounterIndex = 0;       // Index value of the Counter text
    DWORD dwHelpIndex = 0;          // Index value of the Help text
    DWORD dwSize = 0;               // Size of the block of memory that holds the offset array


    pwszCounterText = pCounterHead;
    pwszHelpText = pHelpHead;

    *pNumberOfOffsets = GetNumberOfTextEntries(L"Last Help");
    if (0 == *pNumberOfOffsets)
    {
        wprintf(L"GetNumberOfTextEntries failed; returned 0 for number of entries.\n");
        goto cleanup;
    }

    dwSize = sizeof(DWORD) * (*pNumberOfOffsets + 1);  // Add one to make the array one-based

    pOffsets = (LPDWORD)malloc(dwSize);
    if (pOffsets)
    {
        ZeroMemory(pOffsets, dwSize);
        *pOffsetsHead = pOffsets;

        // Bypass first record (pair) of the counter data - contains upper bounds of system counter index.
        pwszCounterText += (wcslen(pwszCounterText)+1);
        pwszCounterText += (wcslen(pwszCounterText)+1);

        for (; *pwszCounterText; pwszCounterText += (wcslen(pwszCounterText)+1))
        {
            dwCounterIndex = _wtoi(pwszCounterText);
            dwHelpIndex = _wtoi(pwszHelpText);

            // Use the counter's index value as an indexer into the pOffsets array.
            // Store the offset to the counter text in the array element.
            pwszCounterText += (wcslen(pwszCounterText)+1);  //Skip past index value
            pOffsets[dwCounterIndex] = (DWORD)(pwszCounterText - pCounterHead);

            // Some help indexes for system counters do not have a matching counter, so loop
            // until you find the matching help index or the index is greater than the corresponding
            // counter index. For example, if the indexes were as follows, you would loop
            // until the help index was 11.
            //
            // Counter index       Help Index
            //   2                    3
            //   4                    5
            //   6                    7
            //                        9   (skip because there is no matching Counter index)
            //   10                   11
            while (*pwszHelpText && dwHelpIndex < dwCounterIndex)
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past index value
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past help text to the next index value
                dwHelpIndex = _wtoi(pwszHelpText);
            }

            // Use the Help index value as an indexer into the pOffsets array.
            // Store the offset to the help text in the array element.
            if (dwHelpIndex == (dwCounterIndex + 1))
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past index value
                pOffsets[dwHelpIndex] = (DWORD)(pwszHelpText - pHelpHead);
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past help text to next index value
            }
        }

        fSuccess = TRUE;
    }

cleanup:

    return fSuccess;
}


// Retrieve the last help index used from the registry. Use this number
// to allocate an array of DWORDs. Note that index values are not contiguous.
DWORD GetNumberOfTextEntries(LPWSTR pwszSource)
{
    DWORD dwEntries = 0;
    LONG status = ERROR_SUCCESS;
    HKEY hkey = NULL;
    DWORD dwSize = sizeof(DWORD);
    LPWSTR pwszMessage = NULL;

    status = RegOpenKeyEx(HKEY_LOCAL_MACHINE,
        L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib",
        0,
        KEY_READ,
        &hkey);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegOpenKeyEx failed with 0x%x.\n", status);
        goto cleanup;
    }

    status = RegQueryValueEx(hkey, pwszSource, NULL, 0, (LPBYTE)&dwEntries, &dwSize);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
    }

cleanup:

    if (hkey)
        RegCloseKey(hkey);

    return dwEntries;
}


// Print the pairs of counter and help text.
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets)
{    UNREFERENCED_PARAMETER(dwNumberOfOffsets);
    // Counter index values are even numbers that start at 2 so begin with
    // the second element of the array of offsets. Many array elements will
    // not contain offset values (index values are not contiguous).

    // There is typically a large number of counters, so this example prints
    // the first 10 counters and help text.
    //for (DWORD i = 2; i < (dwNumberOfOffsets+1); i++)

    for (DWORD i = 2; i < 22; i++)
    {
        if (pTextOffsets[i]) // If index offset is not zero
        {
            if (0 == (i % 2)) // Counter text index (even number)
                wprintf(L"%d %s\n", i, pCounterTextHead+pTextOffsets[i]);
            else
                wprintf(L"%d %s\n\n", i, pHelpTextHead+pTextOffsets[i]);
        }
    }
}
```



<span data-ttu-id="f2130-150">En el ejemplo siguiente se muestra cómo usar los **\_ \_ datos de rendimiento de HKEY** para recuperar el texto del contador.</span><span class="sxs-lookup"><span data-stu-id="f2130-150">The following example shows how to use **HKEY\_PERFORMANCE\_DATA** to retrieve the counter text.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

#pragma comment(lib, "advapi32.lib")

LPWSTR GetText(LPWSTR pwszSource);
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets);
DWORD GetNumberOfTextEntries(LPWSTR pwszSource);
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets);
LANGID GetLanguageId();

void wmain(void)
{
    LPWSTR pCounterTextHead = NULL; // Head of the MULTI_SZ buffer that contains the Counter text.
    LPWSTR pHelpTextHead = NULL;    // Head of the MULTI_SZ buffer that contains the Help text.
    LPDWORD pTextOffsets = NULL;    // Array of DWORDS that contain the offsets to the text in
                                    // pCounterTextHead and pHelpTextHead. The text index
                                    // values mirror the array index.
    DWORD dwNumberOfOffsets = 0;    // Number of elements in the pTextOffsets array.

    pCounterTextHead = GetText(L"Counter");
    if (NULL == pCounterTextHead)
    {
        wprintf(L"GetText(L\"Counter\") failed.\n");
        goto cleanup;
    }

    pHelpTextHead = GetText(L"Help");
    if (NULL == pHelpTextHead)
    {
        wprintf(L"GetText(L\"Help\") failed.\n");
        goto cleanup;
    }

    if (BuildTextTable(pCounterTextHead, pHelpTextHead, &pTextOffsets, &dwNumberOfOffsets))
    {
        PrintCounterAndHelpText(pCounterTextHead, pHelpTextHead, pTextOffsets, dwNumberOfOffsets);
    }
    else
    {
        wprintf(L"BuildTextTable failed.\n");
    }

cleanup:

    if (pCounterTextHead)
        free(pCounterTextHead);

    if (pHelpTextHead)
        free(pHelpTextHead);

    if (pTextOffsets)
        free(pTextOffsets);

    // You do not need to call RegCloseKey if you are only
    // retrieving names and help text.
}


// Get the text based on the source value. This function uses the
// HKEY_PERFORMANCE_DATA key to get the strings.
LPWSTR GetText(LPWSTR pwszSource)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    LONG status = ERROR_SUCCESS;
    LANGID langid = 0;
    WCHAR wszSourceAndLangId[15];   // Identifies the source of the text; either
                                    // "Counter <langid>" or "Help <langid>"


    // Create the lpValueName string for the registry query.
    langid = GetLanguageId();
    if (0 == langid)
    {
        wprintf(L"GetLanguageId failed to get the default language identifier.\n");
        goto cleanup;
    }

    StringCchPrintf(wszSourceAndLangId, 15, L"%s %03x", pwszSource, langid);

    // Query the size of the text data so you can allocate the buffer.
    status = RegQueryValueEx(HKEY_PERFORMANCE_DATA, wszSourceAndLangId, NULL, NULL, NULL, &dwBufferSize);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed getting required buffer size. Error is 0x%x.\n", status);
        goto cleanup;
    }

    // Allocate the text buffer and query the text.
    pBuffer = (LPWSTR)malloc(dwBufferSize);
    if (pBuffer)
    {
        status = RegQueryValueEx(HKEY_PERFORMANCE_DATA, wszSourceAndLangId, NULL, NULL, (LPBYTE)pBuffer, &dwBufferSize);
        if (ERROR_SUCCESS != status)
        {
            wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
            free(pBuffer);
            pBuffer = NULL;
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"malloc failed to allocate memory.\n");
    }

cleanup:

    return pBuffer;
}


// Retrieve the default language identifier of the current user. For most languages,
// you use the primary language identifier only to retrieve the text. In Windows XP and
// Windows Server 2003, you use the complete language identifier to retrieve Chinese
// text. In Windows Vista, you use the complete language identifier to retrieve Portuguese
// text.
LANGID GetLanguageId()
{
    LANGID langid = 0;  // Complete language identifier.
    WORD primary = 0;   // Primary language identifier.
    OSVERSIONINFO osvi;

    ZeroMemory(&osvi, sizeof(OSVERSIONINFO));
    osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFO);

    if (GetVersionEx(&osvi))
    {
        langid = GetUserDefaultUILanguage();
        primary = PRIMARYLANGID(langid);

        if ( (LANG_PORTUGUESE == primary && osvi.dwBuildNumber > 5) || // Windows Vista and later
             (LANG_CHINESE == primary && (osvi.dwMajorVersion == 5 && osvi.dwMinorVersion >= 1)) ) // XP and Windows Server 2003
        {
            ; //Use the complete language identifier.
        }
        else
        {
            langid = primary;
        }
    }
    else
    {
        wprintf(L"GetVersionEx failed with 0x%x.\n", GetLastError());
    }

    return langid;
}


// Build a table of offsets into the counter and help text buffers. Use the index
// values from the performance data queries to access the offsets.
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets)
{
    BOOL fSuccess = FALSE;
    LPWSTR pwszCounterText = NULL;  // Used to cycle through the Counter text
    LPWSTR pwszHelpText = NULL;     // Used to cycle through the Help text
    LPDWORD pOffsets = NULL;
    DWORD dwCounterIndex = 0;       // Index value of the Counter text
    DWORD dwHelpIndex = 0;          // Index value of the Help text
    DWORD dwSize = 0;               // Size of the block of memory that holds the offset array

    pwszCounterText = pCounterHead;
    pwszHelpText = pHelpHead;

    *pNumberOfOffsets = GetNumberOfTextEntries(L"Last Help");
    if (0 == *pNumberOfOffsets)
    {
        wprintf(L"GetNumberOfTextEntries failed; returned 0 for number of entries.\n");
        goto cleanup;
    }

    dwSize = sizeof(DWORD) * (*pNumberOfOffsets + 1);  // Add one to make the array one-based

    pOffsets = (LPDWORD)malloc(dwSize);
    if (pOffsets)
    {
        ZeroMemory(pOffsets, dwSize);
        *pOffsetsHead = pOffsets;

        // Bypass first record (pair) of the counter data - contains upper bounds of system counter index.
        pwszCounterText += (wcslen(pwszCounterText)+1);
        pwszCounterText += (wcslen(pwszCounterText)+1);

        for (; *pwszCounterText; pwszCounterText += (wcslen(pwszCounterText)+1))
        {
            dwCounterIndex = _wtoi(pwszCounterText);
            dwHelpIndex = _wtoi(pwszHelpText);

            // Use the counter's index value as an indexer into the pOffsets array.
            // Store the offset to the counter text in the array element.
            pwszCounterText += (wcslen(pwszCounterText)+1);  //Skip past index value
            pOffsets[dwCounterIndex] = (DWORD)(pwszCounterText - pCounterHead);

            // Some help indexes for system counters do not have a matching counter, so loop
            // until you find the matching help index or the index is greater than the corresponding
            // counter index. For example, if the indexes were as follows, you would loop
            // until the help index was 11.
            //
            // Counter index       Help Index
            //   2                    3
            //   4                    5
            //   6                    7
            //                        9   (skip because there is no matching Counter index)
            //   10                   11
            while (*pwszHelpText && dwHelpIndex < dwCounterIndex)
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past index value
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past help text to the next index value
                dwHelpIndex = _wtoi(pwszHelpText);
            }

            // Use the Help index value as an indexer into the pOffsets array.
            // Store the offset to the help text in the array element.
            if (dwHelpIndex == (dwCounterIndex + 1))
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past index value
                pOffsets[dwHelpIndex] = (DWORD)(pwszHelpText - pHelpHead);
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past help text to next index value
            }
        }

        fSuccess = TRUE;
    }

cleanup:

    return fSuccess;
}


// Retrieve the last help index used from the registry. Use this number
// to allocate an array of DWORDs. Note that index values are not contiguous.
DWORD GetNumberOfTextEntries(LPWSTR pwszSource)
{
    DWORD dwEntries = 0;
    LONG status = ERROR_SUCCESS;
    HKEY hkey = NULL;
    DWORD dwSize = sizeof(DWORD);
    LPWSTR pwszMessage = NULL;

    status = RegOpenKeyEx(HKEY_LOCAL_MACHINE,
        L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib",
        0,
        KEY_READ,
        &hkey);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegOpenKeyEx failed with 0x%x.\n", status);
        goto cleanup;
    }

    status = RegQueryValueEx(hkey, pwszSource, NULL, 0, (LPBYTE)&dwEntries, &dwSize);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
    }

cleanup:

    if (hkey)
        RegCloseKey(hkey);

    return dwEntries;
}


// Print the pairs of counter and help text.
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets)
{   UNREFERENCED_PARAMETER(dwNumberOfOffsets);
    // Counter index values are even numbers that start at 2 so begin with
    // the second element of the array of offsets. Many array elements will
    // not contain offset values (index values are not contiguous).

    // There is typically a large number of counters, so this example prints
    // the first 10 counters and help text.
    //for (DWORD i = 2; i < (dwNumberOfOffsets+1); i++)

    for (DWORD i = 2; i < 22; i++)
    {
        if (pTextOffsets[i]) // If index offset is not zero
        {
            if (0 == (i % 2)) // Counter text index (even number)
                wprintf(L"%d %s\n", i, pCounterTextHead+pTextOffsets[i]);
            else
                wprintf(L"%d %s\n\n", i, pHelpTextHead+pTextOffsets[i]);
        }
    }
}
```
