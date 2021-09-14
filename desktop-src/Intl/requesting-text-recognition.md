---
description: Solicitud de reconocimiento de texto
ms.assetid: 9db9045d-b289-4c6c-9b17-ddbc2c1d3089
title: Solicitud de reconocimiento de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2442cfa1e26185c4c8d882fe71bb178911f4d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171973"
---
# <a name="requesting-text-recognition"></a>Solicitud de reconocimiento de texto

La aplicación llama a la [**función MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) para solicitar el reconocimiento de texto de un servicio ELS específico. El servicio debe haber sido detectado en una llamada anterior a [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), como se describe en [**Enumeración y liberar servicios**](enumerating-and-freeing-services.md).

> [!Note]  
> La plataforma puede procesar [**las llamadas a MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) de forma sincrónica o asincrónica.

 

[**MappingRecognizeText controla**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) los siguientes tipos de texto:

-   Detección de idioma de Microsoft. UTF-16, formato de normalización C, texto para el que se va a determinar el idioma.
-   Detección de scripts de Microsoft. Texto UTF-16 para el que se van a determinar los intervalos de script.
-   Servicios de transliteración. Texto UTF-16 escrito en script de origen (sistema de escritura).

## <a name="use-synchronous-text-recognition"></a>Uso del reconocimiento de texto sincrónico

En esta sección se proporcionan instrucciones para varias maneras de realizar el reconocimiento de texto sincrónico.

**Reconocimiento de texto sincrónico con Microsoft Detección de idioma Service**

En el ejemplo siguiente se muestra el uso de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) con el servicio microsoft Detección de idioma e imprime todos los resultados recuperados por el servicio. El formato de salida de este servicio es una única estructura [**MAPPING \_ DATA \_ RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) con su miembro **pData** que apunta a una matriz de cadenas con formato de registro terminada en doble null Unicode. Cada cadena de la matriz termina en NULL y se usa una cadena vacía para especificar el final de la matriz. El contenido de la matriz son nombres de idioma ordenados por confianza.


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    WCHAR * p;

    // The return format of the Language Auto-Detection is a
    // double null-terminated registry-formatted array of strings.
    // Every string of the array is null-terminated and there's an
    // empty string specifying the end of the array.
    for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
    {
        printf("%ws\n", p);
    }
}
```



**Reconocimiento de texto sincrónico con el servicio de detección de scripts de Microsoft**

En el ejemplo siguiente se muestra el uso de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) con el servicio de detección de scripts de Microsoft e imprime todos los resultados recuperados. El formato de salida de este servicio es una matriz de estructuras [**MAPPING \_ DATA \_ RANGE,**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) cada una de las que especifica el texto escrito en el mismo script. Los caracteres comunes (Zyyy) se agregan al intervalo anterior o al intervalo siguiente si el intervalo anterior no existe. El **miembro pData** de cada estructura apunta a una cadena terminada en null Unicode que contiene el nombre Unicode estándar del script para el intervalo determinado.

> [!Note]  
> A partir Windows 7, el servicio de detección de scripts de Microsoft cumple con Unicode 5.1.

 


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Script Detection GUID to enumerate SD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_SCRIPT_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData);
    }
}
```



**Reconocimiento de texto sincrónico con Microsoft Cyrillic to Latin Transliteration Service**

En el ejemplo siguiente se muestra el uso de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) con el servicio de transliteración cirílico a latino de Microsoft e imprime los resultados recuperados. Tenga en cuenta las dos maneras diferentes de enumerar este servicio, ya sea por GUID o por categoría y script de entrada.

El formato de salida es el mismo para todos los servicios de transliteración disponibles. Es una única estructura [**MAPPING \_ DATA \_ RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) con su miembro **pData** que apunta a una matriz de caracteres Unicode que representa el texto original transliterado en el script de salida aplicando solo las reglas del servicio de transliteración específico. Este servicio no finaliza null en su salida si la entrada no contiene el carácter nulo de terminación.


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT (L"Skip The russian word for 'yes' is transliterated to Latin as '\x0434\x0430'.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices;
    DWORD                   dwServicesCount;
    HRESULT                 hResult;

    // 1. Enumerate by GUID:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Use the Cyrl->Latn Transliteration GUID to enumerate only this service:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    printf("--\n");

    // 2. Enumerate by input script and category:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    EnumOptions.pszCategory = L"Transliteration";
    EnumOptions.pszInputScript = L"Cyrl";
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    // We want the result to be null-terminated for display.
    // That's why we will also pass the input null terminator:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT) + 1, USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[0].pData);
}
```



**Reconocimiento de texto sincrónico con una llamada a todos los servicios disponibles**

En el ejemplo siguiente se muestra el uso de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) con todos los servicios disponibles e imprime los resultados recuperados para todos los servicios. En este ejemplo se proporciona una buena ilustración del funcionamiento de cada servicio. Al ver la salida de la aplicación de ejemplo, es fácil averiguar lo que sucede internamente con los servicios. En este ejemplo también se muestra que casi todo el código usado para llamar a cualquiera de los servicios de ELS es el mismo.


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    DWORD i;

    // Get all installed ELS services:
    hResult = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service:
            // ... prgServices[i] ...
            if (i > 0)
            {
                printf("--\n");
            }
            hResult = CallMappingRecognizeText(&prgServices[i]);
            if (SUCCEEDED(hResult))
            {
                printf("Calling the service %ws has succeeded!\n",
                    prgServices[i].pszDescription);
            }
            else
            {
                printf("Calling the service %ws has failed, failure = 0x%x!\n",
                    prgServices[i].pszDescription, hResult);
            }
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;
    DWORD dwDataIndex;
    WCHAR c;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        // Currently, we can treat all results as arrays of unicode WCHAR
        // characters, but there can be services in the future
        // that use different formatting, i.e. XML, HTML, etc.
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"");
        for (dwDataIndex = 0; dwDataIndex < pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2; ++dwDataIndex)
        {
            c = ((WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData)[dwDataIndex];
            if (c >= 32 && c < 128 && c != '"') printf("%wc", c);
            else printf("#%x", (unsigned)c);
        }
        printf("\"\n");
    }
}

void CallRecognizeText(LPCWSTR Category, LPCWSTR Text)
{
    HRESULT               Result;
    PMAPPING_SERVICE_INFO rgServices;
    DWORD                 ServicesCount;
    MAPPING_ENUM_OPTIONS  options = {sizeof(MAPPING_ENUM_OPTIONS), (LPWSTR) Category, 0};

    Result = MappingGetServices(&options, &rgServices, &ServicesCount);
    if (Result == S_OK && ServicesCount > 0)
    {
        MAPPING_PROPERTY_BAG bag = { sizeof(MAPPING_PROPERTY_BAG), 0};
        Result = MappingRecognizeText(&rgServices[0], Text, wcslen(Text), 0, NULL, &bag);
        if (Result == S_OK)
        {
            MappingFreePropertyBag(&bag);
        }

        MappingFreeServices(rgServices);
    }
}
int _tmain(int argc, _TCHAR* argv[])
{
    CallRecognizeText(L"Language Detection", L"Text to be recognized");
  
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    return 0;
}
```



## <a name="use-asynchronous-text-recognition"></a>Uso del reconocimiento de texto asincrónico

En el ejemplo siguiente se muestra el uso [**de MappingRecognizeText para**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) el reconocimiento de texto asincrónico. Cuando se usa la devolución de llamada, la aplicación debe asegurarse de que el bolsa de propiedades, el texto de entrada, las opciones y el servicio sean válidos hasta que la devolución de llamada haya terminado de ejecutarse.

La aplicación debe llamar a [**MappingFreePropertyBag inmediatamente**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) después de que la función de devolución de llamada consuma el bolsa. Para obtener más información, vea [Proporcionar devoluciones de llamada para los servicios de ELS.](providing-callbacks-for-els-services.md)


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG    bag;
    MAPPING_OPTIONS         Options;
    HRESULT                 hResult;
    HANDLE                  SyncEvent;
    DWORD                   dwWaitResult;

    SyncEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

    if (SyncEvent == NULL)
    {
        hResult = E_FAIL;
    }
    else
    {
        ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
        bag.Size = sizeof (MAPPING_PROPERTY_BAG);

        ZeroMemory(&Options, sizeof (MAPPING_OPTIONS));
        Options.Size = sizeof (MAPPING_OPTIONS);
        Options.pfnRecognizeCallback = (PFN_MAPPINGCALLBACKPROC)RecognizeCallback;
        Options.pRecognizeCallerData = &SyncEvent;
        Options.dwRecognizeCallerDataSize = sizeof (HANDLE);

        // MappingRecognizeText's dwIndex parameter specifies the first
        // index inside the text from where the recognition should start.
        // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
        // of the input string.
        hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, &Options, &bag);
        if (SUCCEEDED(hResult))
        {
            // We are using an event to synchronize our waiting for the call to end,
            // because some objects have to be valid till the end of the callback call:
            // - the input text
            // - the property bag
            // - the options
            // - the service
            dwWaitResult = WaitForSingleObject(SyncEvent, INFINITE);
            if (dwWaitResult != WAIT_OBJECT_0)
            {
                hResult = E_FAIL;
            }
        }
        CloseHandle(SyncEvent);
    }
    return hResult;
}

void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result)
{
    HANDLE SyncEvent;
    WCHAR * p;

    UNREFERENCED_PARAMETER(dwDataSize);

    if (SUCCEEDED(Result))
    {
        for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
        {
            printf("%ws\n", p);
        }
        MappingFreePropertyBag(pBag);
    }

    SyncEvent = *((HANDLE *)data);
    SetEvent(SyncEvent);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de servicios lingüísticos extendidos](using-extended-linguistic-services.md)
</dt> <dt>

[Proporcionar devoluciones de llamada para los servicios DE ELS](providing-callbacks-for-els-services.md)
</dt> <dt>

[**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> <dt>

[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 



