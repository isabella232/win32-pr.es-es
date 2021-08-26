---
title: FontDIRENTRY (estructura)
description: Contiene información sobre una fuente individual en un grupo de recursos de fuente. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Menús de estructura FONTDIRENTRY y otros recursos
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e236104730dbbfe79ec0ed3d18cbb465402ed8827c6037a2457bec18faf63024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886745"
---
# <a name="fontdirentry-structure"></a>FontDIRENTRY (estructura)

Contiene información sobre una fuente individual en un grupo de recursos de fuente. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dfVersion**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de versión definido por el usuario para los datos de recursos que las herramientas pueden usar para leer y escribir archivos de recursos.

</dd> <dt>

**dfSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño del archivo, en bytes.

</dd> <dt>

**dfCopyright \[ 60\]**
</dt> <dd>

Tipo: **CHAR**

</dd> <dd>

Información de copyright del proveedor de fuentes.

</dd> <dt>

**dfType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo de archivo de fuente.

</dd> <dt>

**dfPoints**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

El tamaño de punto en el que se ve mejor este juego de caracteres.

</dd> <dt>

**dfVertRes**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Resolución vertical, en puntos por pulgada, en la que se digitalizó este juego de caracteres.

</dd> <dt>

**dfHorizRes**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Resolución horizontal, en puntos por pulgada, en la que se digitalizó este juego de caracteres.

</dd> <dt>

**dfAscent**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Distancia desde la parte superior de una celda de definición de caracteres hasta la línea base de la fuente tipográfica.

</dd> <dt>

**dfInternalLeading**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Cantidad de inicial dentro de los límites establecidos por el **miembro dfPixHeight.** En esta área se pueden producir marcas de acentos y otros caracteres diacríicos.

</dd> <dt>

**dfExternalLeading**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Cantidad de inicial adicional que la aplicación agrega entre filas.

</dd> <dt>

**dfItalic**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Fuente cursiva si no es igual a cero.

</dd> <dt>

**dfUnderline**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Fuente subrayada si no es igual a cero.

</dd> <dt>

**dfStrikeOut**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Fuente de tachado si no es igual a cero.

</dd> <dt>

**dfWeight**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Peso de la fuente en el intervalo de 0 a 1000. Por ejemplo, 400 es román y 700 está en negrita. Si este valor es cero, se usa un peso predeterminado. Para obtener valores definidos adicionales, vea la descripción de la [**estructura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> <dt>

**dfCharSet**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Juego de caracteres de la fuente. Para los valores predefinidos, vea la descripción de la [**estructura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> <dt>

**dfPixWidth**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Ancho de la cuadrícula en la que se digitalizó una fuente vectorial. Para las fuentes de trama, si el miembro no es igual a cero, representa el ancho de todos los caracteres del mapa de bits. Si el miembro es igual a cero, la fuente tiene caracteres de ancho variable.

</dd> <dt>

**dfPixHeight**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Alto del mapa de bits de caracteres para las fuentes de trama o el alto de la cuadrícula en la que se digitalizó una fuente vectorial.

</dd> <dt>

**dfPitchAndFamily**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

El tono y la familia de la fuente. Para obtener más información, vea la descripción de la [**estructura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> <dt>

**dfAvgWidth**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Ancho medio de los caracteres de la fuente (definido generalmente como el ancho de la letra x). Este valor no incluye el sobresalte necesario para los caracteres en negrita o cursiva.

</dd> <dt>

**dfMaxWidth**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

El ancho del carácter más ancho de la fuente.

</dd> <dt>

**dfFirstChar**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Primer código de carácter definido en la fuente.

</dd> <dt>

**dfLastChar**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Último código de carácter definido en la fuente.

</dd> <dt>

**dfDefaultChar**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Carácter que se va a sustituir por los caracteres que no están en la fuente.

</dd> <dt>

**dfBreakChar**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Carácter que se usará para definir los saltos de palabras para la justificación de texto.

</dd> <dt>

**dfWidthBytes**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de bytes de cada fila del mapa de bits. Este valor siempre es par para que las filas comiencen en límites de palabras. Para las fuentes vectoriales, este miembro no tiene ningún significado.

</dd> <dt>

**dfDevice**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Desplazamiento del archivo a una cadena terminada en NULL que especifica un nombre de dispositivo. Para una fuente genérica, este valor es cero.

</dd> <dt>

**dfFace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Desplazamiento del archivo a una cadena terminada en NULL que denomina el tipo de letra.

</dd> <dt>

**dfReserved**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Este miembro está reservado.

</dd> <dt>

**szDeviceName**
</dt> <dd>

Tipo: **CHAR**

</dd> <dd>

Nombre del dispositivo si este archivo de fuente se designa para un dispositivo específico.

</dd> <dt>

**szFaceName**
</dt> <dd>

Tipo: **CHAR**

</dd> <dd>

Nombre del tipo de letra de la fuente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Hay una **estructura FONTDIRENTRY** para cada fuente del archivo .res. Las aplicaciones que generan archivos .res con recursos de fuente también deben agregar al archivo una **estructura FONTDIRENTRY** para cada fuente.

Las declaraciones de fuente se pueden mezclar con otras declaraciones de recursos en . Archivo RC porque las fuentes no necesitan ser contiguas en el archivo .res.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DIRENTRY**](direntry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

