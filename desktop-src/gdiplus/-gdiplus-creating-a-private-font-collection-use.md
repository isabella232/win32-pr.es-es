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
# <a name="creating-a-private-font-collection"></a>Creación de una colección de fuentes privadas

La clase [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) hereda de la clase base abstracta [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) . Puede usar un objeto **PrivateFontCollection** para mantener un conjunto de fuentes específicamente para la aplicación.

Una colección de fuentes privada puede incluir fuentes del sistema instaladas, así como fuentes que no se han instalado en el equipo. Para agregar un archivo de fuente a una colección de fuentes privada, llame al método [**PrivateFontCollection:: AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) de un objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .

> [!Note]  
> Cuando se usa la API GDI+, nunca se debe permitir que la aplicación Descargue fuentes arbitrarias de orígenes que no son de confianza. El sistema operativo requiere privilegios elevados para asegurarse de que todas las fuentes instaladas son de confianza.

 

El método [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) de un objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) devuelve una matriz de objetos [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . Antes de llamar a **FontCollection:: GetFamilies**, debe asignar un búfer lo suficientemente grande como para contener esa matriz. Para determinar el tamaño del búfer necesario, llame al método [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) y multiplique el valor devuelto por **sizeof**(**FontFamily**).

El número de familias de fuentes de una colección de fuentes privadas no es necesariamente el mismo que el número de archivos de fuentes que se han agregado a la colección. Por ejemplo, supongamos que agrega los archivos ArialBd. TFF, Times. TFF y TimesBd. TFF a una colección. Habrá tres archivos, pero solo dos familias en la colección porque Times. TFF y TimesBd. TFF pertenecen a la misma familia.

En el ejemplo siguiente se agregan los siguientes tres archivos de fuente a un objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) :

-   C: \\ \\ fuentes de WinNT \\ Arial. TFF (Arial, normal)
-   C: \\ WinNT \\ Fonts \\ CourBI. TFF (Courier New, Bold Italic cursiva)
-   C: \\ WinNT \\ Fonts \\ TimesBd. TFF (Times New Roman, Bold)

El código llama al método [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) del objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) para determinar el número de familias de la colección privada y, a continuación, llama a [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) para recuperar una matriz de objetos [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .

Para cada objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) de la colección, el código llama al método [**FontFamily:: IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) para determinar si están disponibles varios estilos (normal, negrita, cursiva, negrita cursiva, subrayado y tachado). Los argumentos pasados al método **FontFamily:: IsStyleAvailable** son miembros de la enumeración [**fontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , que se declara en Gdiplusenums. h.

Si una combinación de familia/estilo determinada está disponible, se crea un objeto de [**fuente**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) con esa familia y estilo. El primer argumento pasado al constructor de **fuente** es el nombre de la familia de fuentes (no un objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) como sucede con otras variaciones del constructor de **fuentes** ) y el último argumento es la dirección del objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) . Una vez construido el objeto de **fuente** , su dirección se pasa al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para mostrar el nombre de familia junto con el nombre del estilo.


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



En la ilustración siguiente se muestra la salida del código anterior.

![captura de pantalla de una ventana que muestra nueve nombres de fuente, cada uno de los cuales muestra la fuente con nombre](images/fontstext7.png)

Arial. TFF (que se agregó a la colección de fuentes privada en el ejemplo de código anterior) es el archivo de fuente para el estilo Arial normal. Sin embargo, tenga en cuenta que la salida del programa muestra varios estilos disponibles distintos de regular para la familia de fuentes Arial. Esto se debe a que GDI+ de Windows puede simular los estilos de negrita, cursiva y negrita cursiva a partir del estilo normal. GDI+ también puede generar subrayados y tachados a partir del estilo normal.

De forma similar, GDI+ puede simular el estilo de negrita cursiva desde el estilo negrita o el estilo cursiva. La salida del programa muestra que el estilo de negrita cursiva está disponible para la familia de veces, aunque TimesBd. TFF (Times New Roman, Bold) es el único archivo de horas de la colección.

En esta tabla se especifican las fuentes que no son del sistema compatibles con GDI+.



|                     | GDI | GDI+ en Windows 7 | GDI+ en Windows 8 | DirectWrite |
|---------------------|-----|-------------------|-------------------|-------------|
| . FON                | sí | no                | no                | no          |
| . FNT                | sí | no                | no                | no          |
| . TTF                | sí | sí               | sí               | sí         |
| . OTF con TrueType  | sí | sí               | sí               | sí         |
| . OTF con Adobe CFF | sí | no                | sí               | sí         |
| Adobe tipo 1        | sí | no                | no                | no          |



 

 

 



