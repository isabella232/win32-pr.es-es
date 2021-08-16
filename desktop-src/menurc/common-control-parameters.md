---
title: Parámetros de control comunes
description: A continuación se describe la sintaxis general para una instrucción de definición de recursos de control.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbdbf707e1ee72f62c7c08cb7065f4d1a4b8f2f4c000d52f3a28c9806a21a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870566"
---
# <a name="common-control-parameters"></a>Parámetros de control comunes

A continuación se describe la sintaxis general para una instrucción de definición de recursos de control. A continuación se indica el significado de cada parámetro. En ocasiones, una instrucción usará un parámetro de forma diferente o puede omitir un parámetro. La variación específica de la instrucción se describe en la documentación de la instrucción.

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Texto que se va a mostrar con el control . El texto se coloca dentro del control o adyacente al control .

Este parámetro debe contener cero o más caracteres entre comillas dobles ("). Las cadenas finalizan automáticamente en null y se convierten en Unicode en el archivo de recursos resultante.

De forma predeterminada, los caracteres enumerados entre las comillas dobles son caracteres ANSI y las secuencias de escape se interpretan como secuencias de escape de bytes. Si la cadena va precedida del prefijo "L", la cadena es una cadena de caracteres anchos y las secuencias de escape se interpretan como secuencias de escape de 2 bytes que especifican caracteres Unicode. Si se requiere una comilla doble en el texto, debe incluir la comilla doble dos veces.

Un carácter de yand (&) en el texto indica que el carácter siguiente se usa como carácter mnemotécnico para el control. Cuando se muestra el control, no se muestra la yand, pero el carácter mnemotécnico está subrayado. El usuario puede elegir el control presionando la tecla correspondiente al carácter mnemotécnico subrayado. Para usar la y comercial como carácter en una cadena, inserte dos y comercial (&&).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificador de control. Este valor debe ser un entero de 16 bits sin signo en el intervalo comprendido entre 0 y 65 535 o una expresión aritmética simple que se evalúe como un valor de ese intervalo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada X del lado izquierdo del control con respecto al lado izquierdo del cuadro de diálogo. Este valor debe ser un entero de 16 bits sin signo en el intervalo comprendido entre 0 y 65 535. La coordenada está en unidades de diálogo y es relativa al origen del cuadro de diálogo, la ventana o el control que contiene el control especificado.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordenada Y del lado superior del control con respecto a la parte superior del cuadro de diálogo. Este valor debe ser un entero de 16 bits sin signo en el intervalo comprendido entre 0 y 65 535. La coordenada está en unidades de diálogo relativas al origen del cuadro de diálogo, la ventana o el control que contiene el control especificado.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Ancho*
</dt> <dd>

Ancho del control. Este valor debe ser un entero de 16 bits sin signo en el intervalo comprendido entre 1 y 65 535. El ancho está en unidades de 1/4 caracteres.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Altura*
</dt> <dd>

Alto del control. Este valor debe ser un entero de 16 bits sin signo en el intervalo comprendido entre 1 y 65 535. El alto está en unidades de 1/8 caracteres.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de control. Use el operador OR bit a bit ( \| ) para combinar estilos. Para obtener más información, vea [Estilos de ventana.](../winmsg/window-styles.md)

</dd> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*estilo extendido*
</dt> <dd>

Estilos de ventana extendidos. Debe especificar *style para* especificar el estilo *extendido.* Para obtener más información, [**vea EXSTYLE**](exstyle-statement.md).

</dd> <dt>

<span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*
</dt> <dd>

Expresión numérica que indica el identificador utilizado para identificar el control durante el [**procesamiento de WM \_ HELP.**](../shell/wm-help.md)

</dd> <dt>

<span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*
</dt> <dd>

Datos específicos del control para el control. Cuando se crea un diálogo y se crea un control en ese diálogo que tiene datos específicos del control, se pasa un puntero a los datos en el procedimiento de ventana del control a través del *lParam* del mensaje [**WM \_ CREATE**](../winmsg/wm-create.md) para ese control.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las unidades de diálogo horizontales son 1/4 de la unidad de ancho base del diálogo. Las unidades verticales son 1/8 de la unidad de alto base del cuadro de diálogo. Las unidades base del cuadro de diálogo actuales se calculan a partir del alto y ancho de la fuente del sistema actual. La [**función GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) devuelve las unidades base del diálogo en píxeles. Las coordenadas son relativas al origen del cuadro de diálogo.

 

 