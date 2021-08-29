---
description: Trabajar con cadenas de texto de DVD
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: Trabajar con cadenas de texto de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a514ff06047e6a35edb3e10c85e1e88aee9b799255c4108e801f64ea44340941
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696695"
---
# <a name="working-with-dvd-text-strings"></a>Trabajar con cadenas de texto de DVD

Algunos discos DE DVD, especialmente los discos de dvd, pueden contener una lista de cadenas de texto para complementar el contenido de vídeo o audio. Estas cadenas de texto contienen metadatos sobre el contenido, como títulos de canciones, nombres de intérpretes, información de género, entre otros. Las cadenas de texto pueden estar presentes en más de un idioma. Estas cadenas son opcionales y muchos discos no las tienen.

Para recuperar cadenas de texto de un DVD, use la [**interfaz IDvdInfo2,**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) que expone el navegador [de DVD.](dvd-navigator-filter.md) En realidad, no es necesario crear un gráfico de reproducción de DVD para recuperar las cadenas de texto. Simplemente puede crear el navegador de DVD, establecer el volumen de DVD y, a continuación, llamar a los métodos de cadena de texto pertinentes:



| Método                                                                                  | Descripción                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | Obtiene el número de idiomas para los que hay cadenas de texto.                                                                                                                                  |
| [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | Obtiene información sobre las cadenas de texto de un idioma.                                                                                                                                       |
| [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | Obtiene una cadena de texto para un idioma especificado, por índice.                                                                                                                                          |
| [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | Obtiene una cadena de texto como una matriz de bytes sin formato. Use este método si la cadena de texto usa una codificación de caracteres no compatible con [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode). |



 

Este es el procedimiento básico para obtener cadenas de texto:

1.  Llame [**a IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) para buscar el número total de idiomas en los que aparecen las cadenas de texto. Si el número es cero, significa que el DVD no tiene ninguna cadena de texto. (Este es quizás el caso más común, de hecho).
2.  Si el número de idiomas es al menos uno, llame a [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) para obtener información sobre cada idioma. El idioma se especifica por índice. El método devuelve el número total de cadenas de texto en ese idioma, el identificador de configuración regional (**LCID**) del idioma y la codificación de caracteres (Unicode u otro). Las cadenas de texto de DVD pueden usar varios juegos de caracteres diferentes; se enumeran en [**DVD \_ TextCharSet (Enumeración).**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset)
3.  Para obtener una cadena de texto, llame a [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) o [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative). El primer método devuelve una cadena de caracteres anchos, pero no admite todos los juego de caracteres. El segundo método devuelve una matriz de bytes que contiene los datos de texto sin formato. Para ambos métodos, puede llamar al método con un puntero de búfer **NULL** para buscar el tamaño de la cadena y el tipo de texto. A continuación, asigne un búfer y llame al método de nuevo para obtener la cadena.

Cada cadena de texto tiene un código de identificador asociado, que indica el significado de la cadena de texto. El identificador se devuelve como un [**valor \_ TextStringType de DVD.**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) Hay dos categorías de identificador: *identificadores de estructura* e *identificadores de contenido.* Los identificadores de estructura tienen códigos numéricos en el intervalo 0x00–0x02F. Los identificadores de contenido tienen un intervalo de 0x30 y superiores. (La **\_ enumeración TextStringType** de DVD define un subconjunto de los identificadores más comunes, pero los métodos [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) pueden devolver cualquier código de identificador). Un identificador de estructura describe una parte lógica del DVD, como volumen, título o parte del título (PTT). Un identificador de contenido indica el significado de una cadena de texto determinada, como el título de la película, el título de la canción o el género.

Los identificadores de estructura no tienen cadenas de texto asociadas. Cuando aparece un identificador de estructura en los datos de cadena de texto, indica que las siguientes cadenas de texto se aplican a esa parte lógica del DVD, hasta el siguiente identificador de estructura. La posición de los identificadores de estructura dentro de los datos de texto corresponde a la jerarquía lógica del volumen de DVD. Por ejemplo, la primera aparición del identificador de título de la estructura de DVD (0x02) representa el primer título del volumen y la siguiente aparición \_ \_ representa el segundo título.

En la tabla siguiente se muestra cómo se podrían definir las cadenas de texto para un DVD con dos títulos.



| DVD \_ TextStringType        | Cadena de texto  | Descripción                                    |
|----------------------------|--------------|------------------------------------------------|
| Volumen de estructura de DVD \_ \_ (0x01) | ""           | Identificador de estructura para todo el lado del disco. |
| Nombre general de DVD \_ \_ (0x30)  | "Volumen de DVD" | Nombre del volumen de DVD.                               |
| Título de la estructura de DVD \_ \_ (0x02)  | ""           | Identificador de estructura del primer título.      |
| Nombre general de DVD \_ \_ (0x30)  | "Título 1"    | Nombre del primer título.                       |
| Título de la estructura de DVD \_ \_ (0x02)  | ""           | Identificador de estructura del segundo título.     |
| Nombre general de DVD \_ \_ (0x30)  | "Título 2"    | Nombre del segundo título.                      |



 

Los [**métodos GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) y [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) tratan los identificadores de estructura y los identificadores de contenido del mismo modo. La única diferencia es que, para los identificadores de estructura, el búfer de texto asociado está vacío. Es decisión de la aplicación realizar un seguimiento de la relación entre las cadenas de texto y las partes lógicas del DVD.

En el ejemplo siguiente se muestra cómo obtener cadenas de texto de un DVD. En este ejemplo se omiten algunos detalles que requeriría una aplicación real. (Por ejemplo, omite los identificadores de estructura). El ejemplo solo está pensado para mostrar la secuencia correcta de llamadas.


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



Para obtener información sobre las cadenas de texto de DVD, vea el sitio [web del foro de DVD.](https://go.microsoft.com/fwlink/?LinkId=8677)

El **método CDvdCore::GetDvdText** de la aplicación DVDSample muestra los pasos básicos para enumerar y mostrar cadenas de texto de DVD.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



