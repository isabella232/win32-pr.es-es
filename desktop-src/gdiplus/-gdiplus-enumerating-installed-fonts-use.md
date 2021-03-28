---
description: La clase InstalledFontCollection hereda de la clase base abstracta FontCollection.
ms.assetid: 59598f66-4241-4766-a2f0-5de736de959e
title: Enumeración de fuentes instaladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f41242522c2575ffb08e53f7100380ac9a849d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276392"
---
# <a name="enumerating-installed-fonts"></a><span data-ttu-id="da18d-103">Enumeración de fuentes instaladas</span><span class="sxs-lookup"><span data-stu-id="da18d-103">Enumerating Installed Fonts</span></span>

<span data-ttu-id="da18d-104">La clase [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) hereda de la clase base abstracta [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .</span><span class="sxs-lookup"><span data-stu-id="da18d-104">The [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="da18d-105">Puede usar un objeto **InstalledFontCollection** para enumerar las fuentes instaladas en el equipo.</span><span class="sxs-lookup"><span data-stu-id="da18d-105">You can use an **InstalledFontCollection** object to enumerate the fonts installed on the computer.</span></span> <span data-ttu-id="da18d-106">El método [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) de un objeto **InstalledFontCollection** devuelve una matriz de objetos [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="da18d-106">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of an **InstalledFontCollection** object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="da18d-107">Antes de llamar a **FontCollection:: GetFamilies**, debe asignar un búfer lo suficientemente grande como para contener esa matriz.</span><span class="sxs-lookup"><span data-stu-id="da18d-107">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="da18d-108">Para determinar el tamaño del búfer necesario, llame al método [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) y multiplique el valor devuelto por **sizeof**(**FontFamily**).</span><span class="sxs-lookup"><span data-stu-id="da18d-108">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="da18d-109">En el ejemplo siguiente se enumeran los nombres de todas las familias de fuentes instaladas en el equipo.</span><span class="sxs-lookup"><span data-stu-id="da18d-109">The following example lists the names of all the font families installed on the computer.</span></span> <span data-ttu-id="da18d-110">El código recupera los nombres de familia de fuentes llamando al método [**FontFamily:: GetFamilyName**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) de cada objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) en la matriz devuelta por [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies).</span><span class="sxs-lookup"><span data-stu-id="da18d-110">The code retrieves the font family names by calling the [**FontFamily::GetFamilyName**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) method of each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the array returned by [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies).</span></span> <span data-ttu-id="da18d-111">A medida que se recuperan los nombres de familia, se concatenan para formar una lista separada por comas.</span><span class="sxs-lookup"><span data-stu-id="da18d-111">As the family names are retrieved, they are concatenated to form a comma-separated list.</span></span> <span data-ttu-id="da18d-112">A continuación, el método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) dibuja la lista separada por comas en un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="da18d-112">Then the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class draws the comma-separated list in a rectangle.</span></span>


```
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 8, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 500.0f, 500.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

INT          count = 0;
INT          found = 0;
WCHAR        familyName[LF_FACESIZE];  // enough space for one family name
WCHAR*       familyList = NULL;
FontFamily*  pFontFamily = NULL;

InstalledFontCollection installedFontCollection;

// How many font families are installed?
count = installedFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
installedFontCollection.GetFamilies(count, pFontFamily, &found);

// The loop below creates a large string that is a comma-separated
// list of all font family names.
// Allocate a buffer large enough to hold that string.
familyList = new WCHAR[count*(sizeof(familyName)+ 3)];
StringCchCopy(familyList, 1, L"");

for(INT j = 0; j < count; ++j)
{
   pFontFamily[j].GetFamilyName(familyName);  
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), familyName);
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), L",  ");
}

// Draw the large string (list of all families) in a rectangle.
graphics.DrawString(
   familyList, -1, &font, rectF, NULL, &solidBrush);

delete [] pFontFamily;
delete [] familyList;
            
```



<span data-ttu-id="da18d-113">En la ilustración siguiente se muestra una salida posible del código anterior.</span><span class="sxs-lookup"><span data-stu-id="da18d-113">The following illustration shows a possible output of the preceding code.</span></span> <span data-ttu-id="da18d-114">Si ejecuta el código, la salida podría ser diferente, dependiendo de las fuentes instaladas en el equipo.</span><span class="sxs-lookup"><span data-stu-id="da18d-114">If you run the code, the output might be different, depending on the fonts installed on your computer.</span></span>

![captura de pantalla de una ventana que contiene una lista separada por comas de familias de fuentes instaladas](images/fontstext6.png)

 

 



