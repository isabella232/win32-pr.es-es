---
title: Cómo enumerar fuentes
description: En esta información general se muestra cómo enumerar las fuentes de la colección de fuentes del sistema, por nombre de familia.
ms.assetid: c1ec7721-2a30-4de3-b986-932f098228a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9db05deb6b367f1392151ac8c12f2792d6e34f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421001"
---
# <a name="how-to-enumerate-fonts"></a>Cómo enumerar fuentes

En esta información general se muestra cómo enumerar las fuentes de la colección de fuentes del sistema, por nombre de familia.

Esta información general consta de las siguientes partes:

-   [Paso 1: obtener la colección de fuentes del sistema.](#step-1-get-the-system-font-collection)
-   [Paso 2: obtener el recuento de la familia de fuentes.](#step-2-get-the-font-family-count)
-   [Cree un bucle for.](#make-a-for-loop)
    -   [Paso 3: obtener la familia de fuentes.](#step-3-get-the-font-family)
    -   [Paso 4: obtener los nombres de familia.](#step-4-get-the-family-names)
    -   [Paso 5: Busque el nombre de la configuración regional.](#step-5-find-the-locale-name)
    -   [Paso 6: obtener la longitud de la longitud de la cadena de nombre de familia y la cadena.](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [Conclusión](#conclusion)
-   [Código de ejemplo](#example-code)

## <a name="step-1-get-the-system-font-collection"></a>Paso 1: obtener la colección de fuentes del sistema.

Use el método [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) proporcionado por el generador de DirectWrite para devolver una [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) con todas las fuentes del sistema.


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a>Paso 2: obtener el recuento de la familia de fuentes.

A continuación, obtenga el recuento de la familia de fuentes de la colección de fuentes mediante [**IDWriteFontCollection:: GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount). La usaremos para recorrer cada familia de fuentes de la colección.


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a>Cree un bucle for.


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



Ahora que tiene la colección de fuentes y el recuento de fuentes, los pasos restantes se recorren en bucle en cada familia de fuentes, recuperando el objeto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) y consultando.

### <a name="step-3-get-the-font-family"></a>Paso 3: obtener la familia de fuentes.

Obtiene un objeto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) mediante [**IDWriteFontCollection:: GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) y pasándole el índice actual, *i*.


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a>Paso 4: obtener los nombres de familia.

Obtiene los nombres de familia de fuentes mediante [**IDWriteFontFamily:: GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames). Se trata de un objeto [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) . Puede tener varias versiones localizadas del nombre de familia de la familia de fuentes.


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a>Paso 5: Busque el nombre de la configuración regional.

Obtiene el nombre famliy de la fuente en la configuración regional que desee mediante el método [**IDWriteLocalizedStrings:: FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) . En este caso, primero se recupera y se solicita la configuración regional predeterminada. Si eso no funciona, se solicita la configuración regional "en-US". Si no se encuentra ninguna de las configuraciones regionales especificadas, este ejemplo simplemente recurre al índice 0, la primera configuración regional disponible.


```C++
UINT32 index = 0;
BOOL exists = false;

wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

if (SUCCEEDED(hr))
{
    // Get the default locale for this user.
    int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

    // If the default locale is returned, find that locale name, otherwise use "en-us".
    if (defaultLocaleSuccess)
    {
        hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
    }
    if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
    {
        hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
    }
}

// If the specified locale doesn't exist, select the first on the list.
if (!exists)
    index = 0;
```



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a>Paso 6: obtener la longitud de la longitud de la cadena de nombre de familia y la cadena.

Por último, obtenga la longitud de la cadena de nombre de familia mediante [**IDWriteLocalizedStrings:: GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength). Use esta longitud para asignar una cadena lo suficientemente grande como para contener el nombre y, a continuación, obtenga el nombre de la familia de fuentes mediante [**IDWriteLocalizedStrings:: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).


```C++
UINT32 length = 0;

// Get the string length.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetStringLength(index, &length);
}

// Allocate a string big enough to hold the name.
wchar_t* name = new (std::nothrow) wchar_t[length+1];
if (name == NULL)
{
    hr = E_OUTOFMEMORY;
}

// Get the family name.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetString(index, name, length+1);
}
```



## <a name="conclusion"></a>Conclusión

Una vez que tenga el nombre de familia o los nombres de la configuración regional, puede enumerarlos para que los elija el usuario o pasarlos a CreateTextFormat para empezar a dar formato al texto con la familia de fuentes especificada, etc.

## <a name="example-code"></a>Código de ejemplo

Para ver el código fuente completo de este ejemplo, vea el [ejemplo de enumeración de fuentes](/samples/browse/?redirectedfrom=MSDN-samples).

 

 