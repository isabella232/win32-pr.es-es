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
# <a name="how-to-enumerate-fonts"></a><span data-ttu-id="48f7f-103">Cómo enumerar fuentes</span><span class="sxs-lookup"><span data-stu-id="48f7f-103">How to Enumerate Fonts</span></span>

<span data-ttu-id="48f7f-104">En esta información general se muestra cómo enumerar las fuentes de la colección de fuentes del sistema, por nombre de familia.</span><span class="sxs-lookup"><span data-stu-id="48f7f-104">This overview will show how to enumerate the fonts in the system font collection, by family name.</span></span>

<span data-ttu-id="48f7f-105">Esta información general consta de las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="48f7f-105">This overview consists of the following parts:</span></span>

-   [<span data-ttu-id="48f7f-106">Paso 1: obtener la colección de fuentes del sistema.</span><span class="sxs-lookup"><span data-stu-id="48f7f-106">Step 1: Get the System Font Collection.</span></span>](#step-1-get-the-system-font-collection)
-   [<span data-ttu-id="48f7f-107">Paso 2: obtener el recuento de la familia de fuentes.</span><span class="sxs-lookup"><span data-stu-id="48f7f-107">Step 2: Get the Font Family Count.</span></span>](#step-2-get-the-font-family-count)
-   [<span data-ttu-id="48f7f-108">Cree un bucle for.</span><span class="sxs-lookup"><span data-stu-id="48f7f-108">Make a For Loop.</span></span>](#make-a-for-loop)
    -   [<span data-ttu-id="48f7f-109">Paso 3: obtener la familia de fuentes.</span><span class="sxs-lookup"><span data-stu-id="48f7f-109">Step 3: Get the Font Family.</span></span>](#step-3-get-the-font-family)
    -   [<span data-ttu-id="48f7f-110">Paso 4: obtener los nombres de familia.</span><span class="sxs-lookup"><span data-stu-id="48f7f-110">Step 4: Get the Family Names.</span></span>](#step-4-get-the-family-names)
    -   [<span data-ttu-id="48f7f-111">Paso 5: Busque el nombre de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="48f7f-111">Step 5: Find the Locale Name.</span></span>](#step-5-find-the-locale-name)
    -   [<span data-ttu-id="48f7f-112">Paso 6: obtener la longitud de la longitud de la cadena de nombre de familia y la cadena.</span><span class="sxs-lookup"><span data-stu-id="48f7f-112">Step 6: Get the Length of the Family Name String Length and the String.</span></span>](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [<span data-ttu-id="48f7f-113">Conclusión</span><span class="sxs-lookup"><span data-stu-id="48f7f-113">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="48f7f-114">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="48f7f-114">Example Code</span></span>](#example-code)

## <a name="step-1-get-the-system-font-collection"></a><span data-ttu-id="48f7f-115">Paso 1: obtener la colección de fuentes del sistema.</span><span class="sxs-lookup"><span data-stu-id="48f7f-115">Step 1: Get the System Font Collection.</span></span>

<span data-ttu-id="48f7f-116">Use el método [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) proporcionado por el generador de DirectWrite para devolver una [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) con todas las fuentes del sistema.</span><span class="sxs-lookup"><span data-stu-id="48f7f-116">Use the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method provided by the DirectWrite Factory to return an [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) with all of the system fonts in it.</span></span>


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a><span data-ttu-id="48f7f-117">Paso 2: obtener el recuento de la familia de fuentes.</span><span class="sxs-lookup"><span data-stu-id="48f7f-117">Step 2: Get the Font Family Count.</span></span>

<span data-ttu-id="48f7f-118">A continuación, obtenga el recuento de la familia de fuentes de la colección de fuentes mediante [**IDWriteFontCollection:: GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span><span class="sxs-lookup"><span data-stu-id="48f7f-118">Next, get the font family count from the font collection by using [**IDWriteFontCollection::GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span></span> <span data-ttu-id="48f7f-119">La usaremos para recorrer cada familia de fuentes de la colección.</span><span class="sxs-lookup"><span data-stu-id="48f7f-119">We'll use this to loop over each font family in the collection.</span></span>


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a><span data-ttu-id="48f7f-120">Cree un bucle for.</span><span class="sxs-lookup"><span data-stu-id="48f7f-120">Make a For Loop.</span></span>


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



<span data-ttu-id="48f7f-121">Ahora que tiene la colección de fuentes y el recuento de fuentes, los pasos restantes se recorren en bucle en cada familia de fuentes, recuperando el objeto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) y consultando.</span><span class="sxs-lookup"><span data-stu-id="48f7f-121">Now that you have the font collection and the font count, the remaining steps loop over each font family, retrieving the [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object and querying it.</span></span>

### <a name="step-3-get-the-font-family"></a><span data-ttu-id="48f7f-122">Paso 3: obtener la familia de fuentes.</span><span class="sxs-lookup"><span data-stu-id="48f7f-122">Step 3: Get the Font Family.</span></span>

<span data-ttu-id="48f7f-123">Obtiene un objeto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) mediante [**IDWriteFontCollection:: GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) y pasándole el índice actual, *i*.</span><span class="sxs-lookup"><span data-stu-id="48f7f-123">Get a [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object by using [**IDWriteFontCollection::GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) and passing it the current index, *i*.</span></span>


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a><span data-ttu-id="48f7f-124">Paso 4: obtener los nombres de familia.</span><span class="sxs-lookup"><span data-stu-id="48f7f-124">Step 4: Get the Family Names.</span></span>

<span data-ttu-id="48f7f-125">Obtiene los nombres de familia de fuentes mediante [**IDWriteFontFamily:: GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span><span class="sxs-lookup"><span data-stu-id="48f7f-125">Get the font family names by using the [**IDWriteFontFamily::GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span></span> <span data-ttu-id="48f7f-126">Se trata de un objeto [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) .</span><span class="sxs-lookup"><span data-stu-id="48f7f-126">This is an [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) object.</span></span> <span data-ttu-id="48f7f-127">Puede tener varias versiones localizadas del nombre de familia de la familia de fuentes.</span><span class="sxs-lookup"><span data-stu-id="48f7f-127">It can have multiple localized versions of the family name for the font family.</span></span>


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a><span data-ttu-id="48f7f-128">Paso 5: Busque el nombre de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="48f7f-128">Step 5: Find the Locale Name.</span></span>

<span data-ttu-id="48f7f-129">Obtiene el nombre famliy de la fuente en la configuración regional que desee mediante el método [**IDWriteLocalizedStrings:: FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) .</span><span class="sxs-lookup"><span data-stu-id="48f7f-129">Get the font famliy name in the locale you want by using the [**IDWriteLocalizedStrings::FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) method.</span></span> <span data-ttu-id="48f7f-130">En este caso, primero se recupera y se solicita la configuración regional predeterminada.</span><span class="sxs-lookup"><span data-stu-id="48f7f-130">In this case, first the default locale is retrieved and requested.</span></span> <span data-ttu-id="48f7f-131">Si eso no funciona, se solicita la configuración regional "en-US".</span><span class="sxs-lookup"><span data-stu-id="48f7f-131">If that does not work, the "en-us" locale is requested.</span></span> <span data-ttu-id="48f7f-132">Si no se encuentra ninguna de las configuraciones regionales especificadas, este ejemplo simplemente recurre al índice 0, la primera configuración regional disponible.</span><span class="sxs-lookup"><span data-stu-id="48f7f-132">If either of the specified locales are not found, this example simply falls back to index 0, the first available locale.</span></span>


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



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a><span data-ttu-id="48f7f-133">Paso 6: obtener la longitud de la longitud de la cadena de nombre de familia y la cadena.</span><span class="sxs-lookup"><span data-stu-id="48f7f-133">Step 6: Get the Length of the Family Name String Length and the String.</span></span>

<span data-ttu-id="48f7f-134">Por último, obtenga la longitud de la cadena de nombre de familia mediante [**IDWriteLocalizedStrings:: GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span><span class="sxs-lookup"><span data-stu-id="48f7f-134">Finally, get the length of the family name string by using [**IDWriteLocalizedStrings::GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span></span> <span data-ttu-id="48f7f-135">Use esta longitud para asignar una cadena lo suficientemente grande como para contener el nombre y, a continuación, obtenga el nombre de la familia de fuentes mediante [**IDWriteLocalizedStrings:: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span><span class="sxs-lookup"><span data-stu-id="48f7f-135">Use this length to allocate a string large enough to hold the name and then get the font family name by using [**IDWriteLocalizedStrings::GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span></span>


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



## <a name="conclusion"></a><span data-ttu-id="48f7f-136">Conclusión</span><span class="sxs-lookup"><span data-stu-id="48f7f-136">Conclusion</span></span>

<span data-ttu-id="48f7f-137">Una vez que tenga el nombre de familia o los nombres de la configuración regional, puede enumerarlos para que los elija el usuario o pasarlos a CreateTextFormat para empezar a dar formato al texto con la familia de fuentes especificada, etc.</span><span class="sxs-lookup"><span data-stu-id="48f7f-137">Once you have the family name or names in the locale, you can list them for the user to choose from, or pass it to CreateTextFormat to begin formatting text with the specified font family, and so on.</span></span>

## <a name="example-code"></a><span data-ttu-id="48f7f-138">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="48f7f-138">Example Code</span></span>

<span data-ttu-id="48f7f-139">Para ver el código fuente completo de este ejemplo, vea el [ejemplo de enumeración de fuentes](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="48f7f-139">To see the full source code for this example see the [Font Enumeration Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

 

 