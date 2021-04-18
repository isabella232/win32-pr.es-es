---
title: Uso de estructuras en WCS 1.0
description: La mayoría de las estructuras utilizadas por WCS 1,0 son muy sencillas y requieren poca explicación. Están documentados en la sección de referencia de WCS 1,0 titulada estructuras.
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Sistema de color de Windows (WCS), estructuras
- WCS (sistema de colores de Windows), estructuras
- Administración del color de imagen, estructuras
- Administración del color, estructuras
- colores, estructuras
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721375"
---
# <a name="using-structures-in-wcs-10"></a>Uso de estructuras en WCS 1.0

La mayoría de las estructuras utilizadas por WCS 1,0 son muy sencillas y requieren poca explicación. Están documentados en la sección de referencia de WCS 1,0 titulada [estructuras](structures.md).

Las excepciones son la estructura [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) que usa la función [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) y las siguientes estructuras de Windows definidas en WinGDI. h:

-   [BITMAPV5HEADER](#windows-bitmap-header-structures)
-   [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [**CIEXYZ**](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [**CIEXYZTRIPLE**](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

Los temas siguientes se describen con mayor longitud:

-   [Estructuras de encabezado de mapa de bits de Windows](#windows-bitmap-header-structures)
-   [Diferencias entre los encabezados V4 y V5](#differences-between-v4-and-v5-headers)
-   [Bitmap.exe: utilidad de Command-Line para convertir encabezados de mapa de bits](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a>Estructuras de encabezado de mapa de bits de Windows

WCS 1,0 permite vincular o incrustar perfiles de color ICC en mapas de bits independientes del dispositivo (DIB). Esto permite que los colores DIB se caracterizan de manera más precisa de lo que era posible con WCS en Windows 95. [BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , la nueva estructura de encabezado de mapa de bits, se define en WinGDI. h en la versión de Windows 98. Para fines de desarrollo, también se incluye en el archivo ICM. h con la referencia de este programador. La estructura **BITMAPV5HEADER** es la siguiente:


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



El miembro **bV5CSType** puede tener el perfil de valores \_ incrustado o el perfil \_ vinculado para especificar si un perfil está incrustado o vinculado con el Dib. El miembro **bV5ProfileData** es el desplazamiento en bytes desde el principio de la estructura **BITMAPV5HEADER** hasta el inicio de los datos del perfil. Si el perfil está incrustado, los datos del perfil son el perfil real y, si está vinculado, los datos del perfil son el nombre de archivo terminado en NULL del perfil. No puede ser una cadena Unicode. Debe estar compuesto exclusivamente por caracteres del juego de caracteres de Windows (página de códigos 1252).

Cuando se carga un DIB en la memoria, los datos del perfil (si están presentes) deben seguir la tabla de colores y **bV5ProfileData** deben proporcionar el desplazamiento de los datos de perfil desde el principio de la estructura **BITMAPV5HEADER** . El valor de este miembro será diferente ahora, ya que los bits de mapa de bits no siguen la tabla de colores en memoria. Las aplicaciones deben modificar el miembro **bV5ProfileData** después de cargar el DIB en la memoria.

En el caso de los archivos DIB empaquetados, los datos del perfil deben seguir los bits de mapa de bits similares al formato de archivo. El miembro **bV5ProfileData** todavía debe proporcionar el desplazamiento de los datos de perfil desde el principio de la estructura **BITMAPV5HEADER** .

Las aplicaciones deben tener acceso a los datos del perfil solo cuando **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** está integrado en el perfil \_ o se vincula el perfil \_ .

Si un perfil está vinculado, la ruta de acceso del perfil puede ser cualquier nombre completo (incluida una ruta de acceso de red) que se puede abrir mediante la función **CreateFile** de Win32.

## <a name="differences-between-v4-and-v5-headers"></a>Diferencias entre los encabezados V4 y V5

Al trabajar con la nueva estructura de mapa de bits, resulta útil reconocer las diferencias en el modo en que se configuran las estructuras **BITMAPV4HEADER** y **BITMAPV5HEADER** :



| Encabezado V4     | Significado                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **bV4CSType** | \_RGB calibrado por LCS \_ . Este valor implica que los extremos y las gamma se proporcionan en los campos correspondientes. Los valores fantasma causan problemas. |
| **bV4CSType** | LCS \_ sRGB. Este valor implica que el mapa de bits está en el espacio de colores sRGB (se omiten las gamma y los puntos de conexión).                                 |
| **bV4CSType** | espacio de colores de Windows de LCS \_ \_ \_ . Este valor implica que el mapa de bits está en el espacio de colores predeterminado de Windows.                                    |



 



| Encabezado V5     | Significado                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bV5CSType** | \_RGB calibrado por LCS \_ . Este valor implica que los extremos y las gamma se proporcionan en los campos correspondientes. Los valores fantasma causan problemas.                         |
| **bV5CSType** | LCS \_ sRGB. Este valor implica que el mapa de bits está en el espacio de colores sRGB (se omiten las gamma y los puntos de conexión).                                                         |
| **bV5CSType** | Perfil \_ incrustado. Este valor implica que **bV5ProfileData** señala a un búfer de memoria que contiene el perfil que se va a usar (las gamma y los puntos de conexión se omiten). |
| **bV5CSType** | Perfil \_ vinculado. Este valor implica que **bV5ProfileData** apunta al nombre de archivo del perfil que se va a usar (se omiten las gamma y los puntos de conexión).                |
| **bV5CSType** | espacio de colores de Windows de LCS \_ \_ \_ . Este valor implica que el mapa de bits está en el espacio de colores predeterminado de Windows.                                                            |



 

Para convertir mapas de bits anteriores a y desde la nueva estructura **BITMAPV5HEADER** , se incluye un archivo de utilidad de conversión de línea de comandos denominado Bitmap.exe en la referencia del programador de WCS 1,0.

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a>BitMap.exe: utilidad de Command-Line para convertir encabezados de mapa de bits

Bitmap.exe es una utilidad de línea de comandos ubicada en la \\ carpeta bin debajo de la carpeta de instalación que especificó. Modifica los encabezados de los mapas de bits de Windows, lo que permite convertir los mapas de bits existentes de las estructuras de encabezado **BITMAPINFOHEADER** y **BITMAPV4HEADER** en la estructura **BITMAPV5HEADER** más reciente y volver de nuevo. La sintaxis de la línea de comandos es la siguiente:


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



Los modificadores de la línea de comandos tienen los siguientes efectos.



| Conmutador | Significado                                                                  |
|--------|--------------------------------------------------------------------------|
| /d     | Los valores predeterminados se especifican automáticamente en los encabezados convertidos.       |
| /1     | Convertir los mapas de bits especificados en **BITMAPINFOHEADER**                    |
| /4     | Convertir los mapas de bits especificados en **BITMAPV4HEADER**                      |
| /5     | Convertir los mapas de bits especificados en **BITMAPV5HEADER**                      |
| /f     | Fuerza la conversión, incluso si el mapa de bits ya tiene el encabezado derecho       |
| /s     | Convierte los mapas de bits de la carpeta especificada y todos sus subdirectorios. |



 

 

 