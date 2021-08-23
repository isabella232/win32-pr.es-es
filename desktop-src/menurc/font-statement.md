---
title: Instrucción FONT
description: Define la fuente con la que el sistema dibujará texto en el cuadro de diálogo. La fuente se debe haber cargado previamente; por ejemplo, mediante una llamada a la función LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menús de instrucciones FONT y otros recursos
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad289923503866ba2bcd9338bb59a556d0e37cd0a839d4eede0f95a0bec5fd76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972074"
---
# <a name="font-statement"></a>Instrucción FONT

Define la fuente con la que el sistema dibujará texto en el cuadro de diálogo. La fuente se debe haber cargado previamente; por ejemplo, mediante una llamada a [**la función LoadResource.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*
</dt> <dd>

Tamaño de la fuente, en puntos.

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*Tipografía*
</dt> <dd>

Nombre del tipo de letra. Este parámetro debe ir entre comillas (").

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*Peso*
</dt> <dd>

Peso de la fuente en el intervalo de 0 a 1000. Por ejemplo, 400 es normal y 700 está en negrita. Si este valor es 0, se usa el peso predeterminado. Para obtener una lista de valores predefinidos, consulta los **valores fw \_ \*** definidos en WinGDI.h.

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*Cursiva*
</dt> <dd>

Indica una fuente cursiva si se establece en TRUE.

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*Charset*
</dt> <dd>

El conjunto de caracteres. Para obtener una lista de valores, vea el **miembro lfCharSet** de la [**estructura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **instrucción FONT:**

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 