---
title: FONT (instrucción)
description: Define la fuente con la que el sistema dibujará texto en el cuadro de diálogo. La fuente se debe haber cargado previamente; por ejemplo, mediante una llamada a la función LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menús de la instrucción de fuente y otros recursos
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487687"
---
# <a name="font-statement"></a>FONT (instrucción)

Define la fuente con la que el sistema dibujará texto en el cuadro de diálogo. La fuente se debe haber cargado previamente; por ejemplo, mediante una llamada a la función [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*PointSize*
</dt> <dd>

Tamaño de la fuente, en puntos.

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*tipográfico*
</dt> <dd>

Nombre del tipo de letra. Este parámetro debe ir entre comillas (").

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*media*
</dt> <dd>

Peso de la fuente en el intervalo comprendido entre 0 y 1000. Por ejemplo, 400 es normal y 700 está en negrita. Si este valor es 0, se utiliza el peso predeterminado. Para obtener una lista de valores predefinidos, vea los valores de **FW \_ \*** definidos en WinGDI. h.

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*aplicar*
</dt> <dd>

Indica una fuente cursiva si está establecida en TRUE.

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*charset*
</dt> <dd>

El conjunto de caracteres. Para obtener una lista de valores, vea el miembro **lfCharSet** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el uso de la instrucción **Font** :

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 