---
title: Enumeración de fuentes
description: En esta introducción se muestra cómo enumerar las fuentes de la colección de fuentes del sistema, por nombre de familia.
ms.assetid: c1ec7721-2a30-4de3-b986-932f098228a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6823ef48a596ffff941f61135a42f53f9dc351edd51f16325afb6288f85ac136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048945"
---
# <a name="how-to-enumerate-fonts"></a>Enumeración de fuentes

En esta introducción se muestra cómo enumerar las fuentes de la colección de fuentes del sistema, por nombre de familia.

Esta información general consta de las siguientes partes:

-   [Paso 1: Obtener la colección de fuentes del sistema.](#step-1-get-the-system-font-collection)
-   [Paso 2: Obtener el recuento de familias de fuentes.](#step-2-get-the-font-family-count)
-   [Crear un bucle For.](#make-a-for-loop)
    -   [Paso 3: Obtener la familia de fuentes.](#step-3-get-the-font-family)
    -   [Paso 4: Obtener los nombres de familia.](#step-4-get-the-family-names)
    -   [Paso 5: Buscar el nombre de la configuración regional.](#step-5-find-the-locale-name)
    -   [Paso 6: obtener la longitud de la longitud de la cadena de nombre de familia y la cadena.](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [Conclusión](#conclusion)
-   [Código de ejemplo](#example-code)

## <a name="step-1-get-the-system-font-collection"></a>Paso 1: Obtener la colección de fuentes del sistema.

Use el [**método GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) proporcionado por DirectWrite Factory para devolver [**un IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) con todas las fuentes del sistema.


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a>Paso 2: Obtener el recuento de familias de fuentes.

A continuación, obtenga el recuento de familias de fuentes de la colección de fuentes mediante [**IDWriteFontCollection::GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount). Lo usaremos para recorrer en bucle cada familia de fuentes de la colección.


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a>Crear un bucle For.


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



Ahora que tiene la colección de fuentes y el recuento de fuentes, los pasos restantes recorren en bucle cada familia de fuentes, recuperando el objeto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) y consultandolo.

### <a name="step-3-get-the-font-family"></a>Paso 3: Obtener la familia de fuentes.

Obtenga un [**objeto IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) mediante [**IDWriteFontCollection::GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) y pasarlo al índice actual, *i*.


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a>Paso 4: Obtener los nombres de familia.

Obtenga los nombres de familia de fuentes mediante [**IDWriteFontFamily::GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames). Se trata de [**un objeto IDWriteLocalizedStrings.**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) Puede tener varias versiones localizadas del nombre de familia para la familia de fuentes.


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a>Paso 5: Buscar el nombre de la configuración regional.

Obtenga el nombre de la familia de fuentes en la configuración regional que desee mediante el [**método IDWriteLocalizedStrings::FindLocaleName.**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) En este caso, primero se recupera y se solicita la configuración regional predeterminada. Si esto no funciona, se solicita la configuración regional "en-us". Si no se encuentra ninguna de las configuraciones regionales especificadas, este ejemplo simplemente vuelve al índice 0, la primera configuración regional disponible.


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

Por último, obtenga la longitud de la cadena de nombre de familia mediante [**IDWriteLocalizedStrings::GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength). Use esta longitud para asignar una cadena lo suficientemente grande como para contener el nombre y, a continuación, obtener el nombre de la familia de fuentes mediante [**IDWriteLocalizedStrings::GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).


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

Una vez que tenga el nombre de familia o los nombres en la configuración regional, puede enumerarlos para que el usuario elija, o bien pasarlo a CreateTextFormat para empezar a dar formato al texto con la familia de fuentes especificada, y así sucesivamente.

## <a name="example-code"></a>Código de ejemplo

Para ver el código fuente completo de este ejemplo, vea El ejemplo [de enumeración de fuentes](/samples/browse/?redirectedfrom=MSDN-samples).

 

 