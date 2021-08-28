---
description: La aplicación puede admitir un conjunto diferente de idiomas de interfaz de usuario de los admitidos por el sistema operativo de destino. En este tema se describe este tipo de compatibilidad mediante fragmentos de código de ejemplos completos.
ms.assetid: cb9f2a5f-3bb8-4287-a542-c71d20b37194
title: Compatibilidad con Application-Specific language Configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c934ea2f01c37eb2f9e846382447a50ccbedcd9b69fe20069216fa46521b02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130065"
---
# <a name="supporting-application-specific-language-settings"></a>Compatibilidad con Application-Specific language Configuración

La aplicación puede admitir un conjunto diferente de idiomas de interfaz de usuario de los admitidos por el sistema operativo de destino. En este tema se describe este tipo de compatibilidad mediante fragmentos de código de ejemplos completos.

## <a name="interpret-users-language-preference"></a>Interpretación de las preferencias de idioma del usuario

La aplicación debe determinar primero qué idioma de la interfaz de usuario mostrar, en función de las preferencias del usuario. El código puede leer la configuración de un archivo de configuración o de la configuración del Registro.

En el ejemplo siguiente se definen dos funciones que se usan para interpretar la preferencia de idioma del usuario. La primera función muestra la lectura de una lista delimitada de idiomas de un archivo, representada en el código como "langs.txt". Los delimitadores admitidos en el ejemplo son ",",";";"." y " ". La segunda función convierte la cadena leída del archivo en un valor de varias cadenas. Esta operación es necesaria porque las funciones DEA que se usan para establecer idiomas solo aceptan valores de varias cadenas.


```C++
BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
{
    BOOL rtnVal = FALSE;
    // Very simple implementation - assumes that first 'langStrSize' characters of the
    // L".\\langs.txt" file comprises a string of one or more languages.
    HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0,
                                    NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    if(langConfigFileHandle != INVALID_HANDLE_VALUE)
    {
        // Clear the input variables.
        DWORD bytesActuallyRead = 0;
        if(ReadFile(langConfigFileHandle, langStr, langStrSize*sizeof(WCHAR), &bytesActuallyRead, NULL)
           && bytesActuallyRead > 0)
        {
            rtnVal = TRUE;
            DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize)
                              ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
            langStr[nullIndex] = L'\0';
        }
        CloseHandle(langConfigFileHandle);
    }
    return rtnVal;
}
BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
{
    BOOL rtnVal = FALSE;
    size_t strLen = 0;
    rtnVal = SUCCEEDED(StringCchLengthW(langStr, USER_CONFIGURATION_STRING_BUFFER*2, &strLen));
    if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
    {
        WCHAR * langMultiStrPtr = langMultiStr;
        WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
        WCHAR * context = last;
        WCHAR * next = wcstok_s(last,L",; :",&context);
        while(next && rtnVal)
        {
            // Make sure you validate the user input.
            if(SUCCEEDED(StringCchLengthW(last, LOCALE_NAME_MAX_LENGTH, &strLen))
               && IsValidLocaleName(next))
            {
                langMultiStrPtr[0] = L'\0';
                rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,
                                    (langMultiStrSize - (langMultiStrPtr - langMultiStr)), next));
                langMultiStrPtr += strLen + 1;
            }
            next = wcstok_s(NULL, L",; :", &context);
            if(next)
                last = next;
        }
        // Make sure there is a double null term for the multi-string.
        if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr)))
        {
            langMultiStrPtr[0] = L'\0';
        }
        else // Fail and guard anyone whom might use the multi-string.
        {
            langMultiStr[0] = L'\0';
            langMultiStr[1] = L'\0';
        }
    }
    return rtnVal;
}
```



## <a name="set-the-application-language"></a>Establecer el idioma de la aplicación

Después de leer la información de preferencias de idioma, el código de aplicación debe usar la configuración recuperada para establecer el idioma de la aplicación. En Windows 7 y versiones posteriores, la aplicación puede establecer el idioma en el nivel de proceso llamando a la [**función SetProcessPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)


```C++
DWORD langCount = 0;
// Using SetProcessPreferredUILanguages is recommended for new applications (esp. multi-threaded applications).
if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
```



En Windows Vista y versiones posteriores, el lenguaje de aplicación se establece en el nivel de subproceso mediante una llamada a la [**función SetThreadPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)


```C++
DWORD langCount = 0;
// The following line of code is supported on Windows Vista and later.
if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
return 1;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer las preferencias de idioma de la aplicación](setting-application-language-preferences.md)
</dt> <dt>

[MUI: Application-Specific Configuración ejemplo (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI: Application-Specific Configuración de datos (Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



