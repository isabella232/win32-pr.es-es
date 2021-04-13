---
description: La clase PrivateFontCollection hereda de la clase base abstracta FontCollection. Puede usar un objeto PrivateFontCollection para mantener un conjunto de fuentes específicamente para la aplicación.
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: Creación de una colección de fuentes privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084e8a2d6f79f60e0719f04fbabb778b9483bd80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276397"
---
# <a name="creating-a-private-font-collection"></a><span data-ttu-id="d55ff-104">Creación de una colección de fuentes privadas</span><span class="sxs-lookup"><span data-stu-id="d55ff-104">Creating a Private Font Collection</span></span>

<span data-ttu-id="d55ff-105">La clase [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) hereda de la clase base abstracta [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .</span><span class="sxs-lookup"><span data-stu-id="d55ff-105">The [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="d55ff-106">Puede usar un objeto **PrivateFontCollection** para mantener un conjunto de fuentes específicamente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d55ff-106">You can use a **PrivateFontCollection** object to maintain a set of fonts specifically for your application.</span></span>

<span data-ttu-id="d55ff-107">Una colección de fuentes privada puede incluir fuentes del sistema instaladas, así como fuentes que no se han instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="d55ff-107">A private font collection can include installed system fonts as well as fonts that have not been installed on the computer.</span></span> <span data-ttu-id="d55ff-108">Para agregar un archivo de fuente a una colección de fuentes privada, llame al método [**PrivateFontCollection:: AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) de un objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .</span><span class="sxs-lookup"><span data-stu-id="d55ff-108">To add a font file to a private font collection, call the [**PrivateFontCollection::AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span>

> [!Note]  
> <span data-ttu-id="d55ff-109">Cuando se usa la API GDI+, nunca se debe permitir que la aplicación Descargue fuentes arbitrarias de orígenes que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="d55ff-109">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="d55ff-110">El sistema operativo requiere privilegios elevados para asegurarse de que todas las fuentes instaladas son de confianza.</span><span class="sxs-lookup"><span data-stu-id="d55ff-110">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

 

<span data-ttu-id="d55ff-111">El método [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) de un objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) devuelve una matriz de objetos [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="d55ff-111">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="d55ff-112">Antes de llamar a **FontCollection:: GetFamilies**, debe asignar un búfer lo suficientemente grande como para contener esa matriz.</span><span class="sxs-lookup"><span data-stu-id="d55ff-112">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="d55ff-113">Para determinar el tamaño del búfer necesario, llame al método [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) y multiplique el valor devuelto por **sizeof**(**FontFamily**).</span><span class="sxs-lookup"><span data-stu-id="d55ff-113">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="d55ff-114">El número de familias de fuentes de una colección de fuentes privadas no es necesariamente el mismo que el número de archivos de fuentes que se han agregado a la colección.</span><span class="sxs-lookup"><span data-stu-id="d55ff-114">The number of font families in a private font collection is not necessarily the same as the number of font files that have been added to the collection.</span></span> <span data-ttu-id="d55ff-115">Por ejemplo, supongamos que agrega los archivos ArialBd. TFF, Times. TFF y TimesBd. TFF a una colección.</span><span class="sxs-lookup"><span data-stu-id="d55ff-115">For example, suppose you add the files ArialBd.tff, Times.tff, and TimesBd.tff to a collection.</span></span> <span data-ttu-id="d55ff-116">Habrá tres archivos, pero solo dos familias en la colección porque Times. TFF y TimesBd. TFF pertenecen a la misma familia.</span><span class="sxs-lookup"><span data-stu-id="d55ff-116">There will be three files but only two families in the collection because Times.tff and TimesBd.tff belong to the same family.</span></span>

<span data-ttu-id="d55ff-117">En el ejemplo siguiente se agregan los siguientes tres archivos de fuente a un objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) :</span><span class="sxs-lookup"><span data-stu-id="d55ff-117">The following example adds the following three font files to a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object:</span></span>

-   <span data-ttu-id="d55ff-118">C: \\ \\ fuentes de WinNT \\ Arial. TFF (Arial, normal)</span><span class="sxs-lookup"><span data-stu-id="d55ff-118">C:\\WINNT\\Fonts\\Arial.tff (Arial, regular)</span></span>
-   <span data-ttu-id="d55ff-119">C: \\ WinNT \\ Fonts \\ CourBI. TFF (Courier New, Bold Italic cursiva)</span><span class="sxs-lookup"><span data-stu-id="d55ff-119">C:\\WINNT\\Fonts\\CourBI.tff (Courier New, bold italic)</span></span>
-   <span data-ttu-id="d55ff-120">C: \\ WinNT \\ Fonts \\ TimesBd. TFF (Times New Roman, Bold)</span><span class="sxs-lookup"><span data-stu-id="d55ff-120">C:\\WINNT\\Fonts\\TimesBd.tff (Times New Roman, bold)</span></span>

<span data-ttu-id="d55ff-121">El código llama al método [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) del objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) para determinar el número de familias de la colección privada y, a continuación, llama a [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) para recuperar una matriz de objetos [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="d55ff-121">The code calls the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object to determine the number of families in the private collection, and then calls [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) to retrieve an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span>

<span data-ttu-id="d55ff-122">Para cada objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) de la colección, el código llama al método [**FontFamily:: IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) para determinar si están disponibles varios estilos (normal, negrita, cursiva, negrita cursiva, subrayado y tachado).</span><span class="sxs-lookup"><span data-stu-id="d55ff-122">For each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the collection, the code calls the [**FontFamily::IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) method to determine whether various styles (regular, bold, italic, bold italic, underline, and strikeout) are available.</span></span> <span data-ttu-id="d55ff-123">Los argumentos pasados al método **FontFamily:: IsStyleAvailable** son miembros de la enumeración [**fontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , que se declara en Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="d55ff-123">The arguments passed to the **FontFamily::IsStyleAvailable** method are members of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="d55ff-124">Si una combinación de familia/estilo determinada está disponible, se crea un objeto de [**fuente**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) con esa familia y estilo.</span><span class="sxs-lookup"><span data-stu-id="d55ff-124">If a particular family/style combination is available, a [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object is constructed using that family and style.</span></span> <span data-ttu-id="d55ff-125">El primer argumento pasado al constructor de **fuente** es el nombre de la familia de fuentes (no un objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) como sucede con otras variaciones del constructor de **fuentes** ) y el último argumento es la dirección del objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .</span><span class="sxs-lookup"><span data-stu-id="d55ff-125">The first argument passed to the **Font** constructor is the font family name (not a [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object as is the case for other variations of the **Font** constructor), and the final argument is the address of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span> <span data-ttu-id="d55ff-126">Una vez construido el objeto de **fuente** , su dirección se pasa al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para mostrar el nombre de familia junto con el nombre del estilo.</span><span class="sxs-lookup"><span data-stu-id="d55ff-126">After the **Font** object is constructed, its address is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to display the family name along with the name of the style.</span></span>


```
#define MAX_STYLE_SIZE 20
#define MAX_FACEANDSTYLE_SIZE (LF_FACESIZE + MAX_STYLE_SIZE + 2)

PointF      pointF(10.0f, 0.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 0));
INT                   count = 0;
INT                   found = 0;
WCHAR                 familyName[LF_FACESIZE];
WCHAR                 familyNameAndStyle[MAX_FACEANDSTYLE_SIZE]; 
FontFamily*           pFontFamily;
PrivateFontCollection privateFontCollection;

// Add three font files to the private collection.
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\Arial.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\CourBI.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\TimesBd.ttf");

// How many font families are in the private collection?
count = privateFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
privateFontCollection.GetFamilies(count, pFontFamily, &found);

// Display the name of each font family in the private collection
// along with the available styles for that font family.
for(INT j = 0; j < count; ++j)
{
   // Get the font family name.
   pFontFamily[j].GetFamilyName(familyName);
   
   // Is the regular style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleRegular))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Regular");

      Font* pFont = new Font(
         familyName, 16, FontStyleRegular, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);      
   }

   // Is the bold style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBold))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Bold");

      Font* pFont = new Font(
         familyName, 16, FontStyleBold, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Italic");

      Font* pFont = new Font(
         familyName, 16, FontStyleItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the bold italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBoldItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" BoldItalic");

      Font* pFont = new Font(familyName, 16, 
         FontStyleBoldItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
    }

   // Is the underline style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleUnderline))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Underline");

      Font* pFont = new Font(familyName, 16, 
         FontStyleUnderline, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0);
      delete(pFont);
   }
 
   // Is the strikeout style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleStrikeout))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Strikeout");

      Font* pFont = new Font(familyName, 16, 
         FontStyleStrikeout, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Separate the families with white space.
   pointF.Y += 10.0f;

} // for

delete pFontFamily;
            
```



<span data-ttu-id="d55ff-127">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="d55ff-127">The following illustration shows the output of the preceding code.</span></span>

![captura de pantalla de una ventana que muestra nueve nombres de fuente, cada uno de los cuales muestra la fuente con nombre](images/fontstext7.png)

<span data-ttu-id="d55ff-129">Arial. TFF (que se agregó a la colección de fuentes privada en el ejemplo de código anterior) es el archivo de fuente para el estilo Arial normal.</span><span class="sxs-lookup"><span data-stu-id="d55ff-129">Arial.tff (which was added to the private font collection in the preceding code example) is the font file for the Arial regular style.</span></span> <span data-ttu-id="d55ff-130">Sin embargo, tenga en cuenta que la salida del programa muestra varios estilos disponibles distintos de regular para la familia de fuentes Arial.</span><span class="sxs-lookup"><span data-stu-id="d55ff-130">Note, however, that the program output shows several available styles other than regular for the Arial font family.</span></span> <span data-ttu-id="d55ff-131">Esto se debe a que GDI+ de Windows puede simular los estilos de negrita, cursiva y negrita cursiva a partir del estilo normal.</span><span class="sxs-lookup"><span data-stu-id="d55ff-131">That is because Windows GDI+ can simulate the bold, italic, and bold italic styles from the regular style.</span></span> <span data-ttu-id="d55ff-132">GDI+ también puede generar subrayados y tachados a partir del estilo normal.</span><span class="sxs-lookup"><span data-stu-id="d55ff-132">GDI+ can also produce underlines and strikeouts from the regular style.</span></span>

<span data-ttu-id="d55ff-133">De forma similar, GDI+ puede simular el estilo de negrita cursiva desde el estilo negrita o el estilo cursiva.</span><span class="sxs-lookup"><span data-stu-id="d55ff-133">Similarly, GDI+ can simulate the bold italic style from either the bold style or the italic style.</span></span> <span data-ttu-id="d55ff-134">La salida del programa muestra que el estilo de negrita cursiva está disponible para la familia de veces, aunque TimesBd. TFF (Times New Roman, Bold) es el único archivo de horas de la colección.</span><span class="sxs-lookup"><span data-stu-id="d55ff-134">The program output shows that the bold italic style is available for the Times family even though TimesBd.tff (Times New Roman, bold) is the only Times file in the collection.</span></span>

<span data-ttu-id="d55ff-135">En esta tabla se especifican las fuentes que no son del sistema compatibles con GDI+.</span><span class="sxs-lookup"><span data-stu-id="d55ff-135">This table specifies the non-system fonts that GDI+ supports.</span></span>



|                     | <span data-ttu-id="d55ff-136">GDI</span><span class="sxs-lookup"><span data-stu-id="d55ff-136">GDI</span></span> | <span data-ttu-id="d55ff-137">GDI+ en Windows 7</span><span class="sxs-lookup"><span data-stu-id="d55ff-137">GDI+ on Windows 7</span></span> | <span data-ttu-id="d55ff-138">GDI+ en Windows 8</span><span class="sxs-lookup"><span data-stu-id="d55ff-138">GDI+ on Windows 8</span></span> | <span data-ttu-id="d55ff-139">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d55ff-139">DirectWrite</span></span> |
|---------------------|-----|-------------------|-------------------|-------------|
| <span data-ttu-id="d55ff-140">. FON</span><span class="sxs-lookup"><span data-stu-id="d55ff-140">.FON</span></span>                | <span data-ttu-id="d55ff-141">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-141">yes</span></span> | <span data-ttu-id="d55ff-142">no</span><span class="sxs-lookup"><span data-stu-id="d55ff-142">no</span></span>                | <span data-ttu-id="d55ff-143">no</span><span class="sxs-lookup"><span data-stu-id="d55ff-143">no</span></span>                | <span data-ttu-id="d55ff-144">no</span><span class="sxs-lookup"><span data-stu-id="d55ff-144">no</span></span>          |
| <span data-ttu-id="d55ff-145">. FNT</span><span class="sxs-lookup"><span data-stu-id="d55ff-145">.FNT</span></span>                | <span data-ttu-id="d55ff-146">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-146">yes</span></span> | <span data-ttu-id="d55ff-147">no</span><span class="sxs-lookup"><span data-stu-id="d55ff-147">no</span></span>                | <span data-ttu-id="d55ff-148">no</span><span class="sxs-lookup"><span data-stu-id="d55ff-148">no</span></span>                | <span data-ttu-id="d55ff-149">no</span><span class="sxs-lookup"><span data-stu-id="d55ff-149">no</span></span>          |
| <span data-ttu-id="d55ff-150">. TTF</span><span class="sxs-lookup"><span data-stu-id="d55ff-150">.TTF</span></span>                | <span data-ttu-id="d55ff-151">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-151">yes</span></span> | <span data-ttu-id="d55ff-152">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-152">yes</span></span>               | <span data-ttu-id="d55ff-153">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-153">yes</span></span>               | <span data-ttu-id="d55ff-154">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-154">yes</span></span>         |
| <span data-ttu-id="d55ff-155">. OTF con TrueType</span><span class="sxs-lookup"><span data-stu-id="d55ff-155">.OTF with TrueType</span></span>  | <span data-ttu-id="d55ff-156">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-156">yes</span></span> | <span data-ttu-id="d55ff-157">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-157">yes</span></span>               | <span data-ttu-id="d55ff-158">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-158">yes</span></span>               | <span data-ttu-id="d55ff-159">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-159">yes</span></span>         |
| <span data-ttu-id="d55ff-160">. OTF con Adobe CFF</span><span class="sxs-lookup"><span data-stu-id="d55ff-160">.OTF with Adobe CFF</span></span> | <span data-ttu-id="d55ff-161">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-161">yes</span></span> | <span data-ttu-id="d55ff-162">no</span><span class="sxs-lookup"><span data-stu-id="d55ff-162">no</span></span>                | <span data-ttu-id="d55ff-163">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-163">yes</span></span>               | <span data-ttu-id="d55ff-164">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-164">yes</span></span>         |
| <span data-ttu-id="d55ff-165">Adobe tipo 1</span><span class="sxs-lookup"><span data-stu-id="d55ff-165">Adobe Type 1</span></span>        | <span data-ttu-id="d55ff-166">sí</span><span class="sxs-lookup"><span data-stu-id="d55ff-166">yes</span></span> | <span data-ttu-id="d55ff-167">no</span><span class="sxs-lookup"><span data-stu-id="d55ff-167">no</span></span>                | <span data-ttu-id="d55ff-168">no</span><span class="sxs-lookup"><span data-stu-id="d55ff-168">no</span></span>                | <span data-ttu-id="d55ff-169">no</span><span class="sxs-lookup"><span data-stu-id="d55ff-169">no</span></span>          |



 

 

 



