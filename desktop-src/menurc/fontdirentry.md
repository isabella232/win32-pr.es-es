---
title: Estructura FONTDIRENTRY
description: Contiene información sobre una fuente individual de un grupo de recursos de fuentes. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Menús de la estructura FONTDIRENTRY y otros recursos
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cee72a490fd2b94b1c810797f656d81418c0f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489664"
---
# <a name="fontdirentry-structure"></a>Estructura FONTDIRENTRY

Contiene información sobre una fuente individual de un grupo de recursos de fuentes. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

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

Tipo: **Word**

</dd> <dd>

Un número de versión definido por el usuario para los datos de recursos que las herramientas pueden utilizar para leer y escribir archivos de recursos.

</dd> <dt>

**dfSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño del archivo, en bytes.

</dd> <dt>

**dfCopyright \[ 60\]**
</dt> <dd>

Tipo: **Char**

</dd> <dd>

La información de copyright del proveedor de fuentes.

</dd> <dt>

**dfType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

El tipo de archivo de fuente.

</dd> <dt>

**dfPoints**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tamaño de punto en el que este juego de caracteres tiene un aspecto óptimo.

</dd> <dt>

**dfVertRes**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Resolución vertical, en puntos por pulgada, a la que se ha digitalizado este juego de caracteres.

</dd> <dt>

**dfHorizRes**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Resolución horizontal, en puntos por pulgada, a la que se ha digitalizado este juego de caracteres.

</dd> <dt>

**dfAscent**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Distancia desde la parte superior de una celda de definición de caracteres a la línea base de la fuente tipográfica.

</dd> <dt>

**dfInternalLeading**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

La cantidad de espacio que se encuentra dentro de los límites establecidos por el miembro **dfPixHeight** . En esta área pueden aparecer marcas de acento y otros caracteres diacríticos.

</dd> <dt>

**dfExternalLeading**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

La cantidad de espacio adicional que la aplicación agrega entre las filas.

</dd> <dt>

**dfItalic**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Fuente en cursiva si no es igual a cero.

</dd> <dt>

**dfUnderline**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Fuente subrayada si no es igual a cero.

</dd> <dt>

**dfStrikeOut**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Una fuente de tachado si no es igual a cero.

</dd> <dt>

**dfWeight**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Peso de la fuente en el intervalo comprendido entre 0 y 1000. Por ejemplo, 400 es romano y 700 está en negrita. Si este valor es cero, se usa una ponderación predeterminada. Para obtener más valores definidos, vea la descripción de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfCharSet**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Juego de caracteres de la fuente. Para los valores predefinidos, vea la descripción de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfPixWidth**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Ancho de la cuadrícula en la que se ha digitalizado una fuente de vector. En el caso de las fuentes de trama, si el miembro no es igual a cero, representa el ancho de todos los caracteres del mapa de bits. Si el miembro es igual a cero, la fuente tiene caracteres de ancho variable.

</dd> <dt>

**dfPixHeight**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Alto del mapa de bits de caracteres para las fuentes de tramas o el alto de la cuadrícula en la que se ha digitalizado una fuente de vector.

</dd> <dt>

**dfPitchAndFamily**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

El paso y la familia de la fuente. Para obtener más información, vea la descripción de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfAvgWidth**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Ancho medio de los caracteres de la fuente (generalmente definido como el ancho de la letra x). Este valor no incluye el saliente necesario para los caracteres en negrita o cursiva.

</dd> <dt>

**dfMaxWidth**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

El ancho del carácter más ancho de la fuente.

</dd> <dt>

**dfFirstChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

El primer código de carácter definido en la fuente.

</dd> <dt>

**dfLastChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

El último código de carácter definido en la fuente.

</dd> <dt>

**dfDefaultChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Carácter que se va a sustituir para los caracteres que no están en la fuente.

</dd> <dt>

**dfBreakChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Carácter que se usará para definir saltos de palabras para la justificación del texto.

</dd> <dt>

**dfWidthBytes**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Número de bytes de cada fila del mapa de bits. Este valor siempre es par que las filas se inicien en los límites de palabras. En el caso de las fuentes de Vector, este miembro no tiene ningún significado.

</dd> <dt>

**dfDevice**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

El desplazamiento en el archivo en una cadena terminada en null que especifica un nombre de dispositivo. En el caso de una fuente genérica, este valor es cero.

</dd> <dt>

**dfFace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Desplazamiento del archivo en una cadena terminada en null que nombra el tipo de letra.

</dd> <dt>

**dfReserved**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Este miembro está reservado.

</dd> <dt>

**szDeviceName**
</dt> <dd>

Tipo: **Char**

</dd> <dd>

El nombre del dispositivo si este archivo de fuente se designa para un dispositivo específico.

</dd> <dt>

**szFaceName**
</dt> <dd>

Tipo: **Char**

</dd> <dd>

Nombre del tipo de letra de la fuente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Hay una estructura **FONTDIRENTRY** para cada fuente del archivo. res. Las aplicaciones que generan archivos. res con recursos de fuente también deben agregar al archivo una estructura **FONTDIRENTRY** para cada fuente.

Las declaraciones de fuente se pueden mezclar con otras declaraciones de recursos en. Archivo RC porque no es necesario que las fuentes sean contiguas en el archivo. res.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**ARRENDAMIENTO**](direntry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**NDPTECGDI**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

