---
title: Parámetros de control comunes
description: A continuación se describe la sintaxis general de una instrucción de definición de recursos de control.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358900"
---
# <a name="common-control-parameters"></a>Parámetros de control comunes

A continuación se describe la sintaxis general de una instrucción de definición de recursos de control. A continuación se proporciona el significado de cada parámetro. En ocasiones, una instrucción usará un parámetro de manera diferente o puede omitir un parámetro. La variación específica de la instrucción se describe en la documentación de la instrucción.

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*negrita*
</dt> <dd>

Texto que se va a mostrar con el control. El texto se coloca dentro del control o junto al control.

Este parámetro debe contener cero o más caracteres entre comillas dobles ("). Las cadenas terminan automáticamente en NULL y se convierten en Unicode en el archivo de recursos resultante.

De forma predeterminada, los caracteres enumerados entre comillas dobles son caracteres ANSI y las secuencias de escape se interpretan como secuencias de escape de bytes. Si la cadena está precedida por el prefijo "L", la cadena es una cadena de caracteres anchos y las secuencias de escape se interpretan como secuencias de escape de 2 bytes que especifican caracteres Unicode. Si se requiere una comilla doble en el texto, debe incluir las comillas dobles dos veces.

Un carácter de y comercial (&) en el texto indica que el siguiente carácter se utiliza como carácter de tecla de mnemotécnico para el control. Cuando se muestra el control, no se muestra el símbolo de y comercial, pero el carácter de la tecla de tecla está subrayado. El usuario puede elegir el control presionando la tecla correspondiente al carácter mnemotécnico subrayado. Para usar la y comercial como carácter en una cadena, inserte dos símbolos de y comercial (&&).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sesión*
</dt> <dd>

Identificador de control. Este valor debe ser un entero sin signo de 16 bits en el intervalo comprendido entre 0 y 65.535 o una expresión aritmética simple que se evalúe como un valor de ese intervalo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*x1*
</dt> <dd>

Coordenada X del lado izquierdo del control en relación con el lado izquierdo del cuadro de diálogo. Este valor debe ser un entero sin signo de 16 bits en el intervalo comprendido entre 0 y 65.535. La coordenada está en unidades de cuadro de diálogo y es relativa al origen del cuadro de diálogo, ventana o control que contiene el control especificado.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*sí*
</dt> <dd>

Coordenada Y del lado superior del control en relación con la parte superior del cuadro de diálogo. Este valor debe ser un entero sin signo de 16 bits en el intervalo comprendido entre 0 y 65.535. La coordenada está en unidades de diálogo relativas al origen del cuadro de diálogo, ventana o control que contiene el control especificado.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Ancho*
</dt> <dd>

Ancho del control. Este valor debe ser un entero sin signo de 16 bits en el intervalo comprendido entre 1 y 65.535. El ancho está en unidades de 1/4 caracteres.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*alto*
</dt> <dd>

Alto del control. Este valor debe ser un entero sin signo de 16 bits en el intervalo comprendido entre 1 y 65.535. El alto está en unidades de 1/8 caracteres.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos de control. Use el operador OR bit \| a bit () para combinar estilos. Para obtener más información, consulte [estilos de ventana](../winmsg/window-styles.md).

</dd> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*estilo extendido*
</dt> <dd>

Estilos de ventana extendidos. Debe especificar el *estilo* para especificar *el estilo extendido*. Para obtener más información, vea [**ExStyle**](exstyle-statement.md).

</dd> <dt>

<span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*
</dt> <dd>

Expresión numérica que indica el identificador usado para identificar el control durante el procesamiento de la [**\_ ayuda de WM**](../shell/wm-help.md) .

</dd> <dt>

<span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*
</dt> <dd>

Datos específicos del control para el control. Cuando se crea un cuadro de diálogo y se crea un control en ese cuadro de diálogo con datos específicos del control, se pasa un puntero a esos datos en el procedimiento de ventana del control a través del *lParam* del mensaje de [**\_ creación de WM**](../winmsg/wm-create.md) para ese control.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las unidades de cuadro de diálogo horizontales son 1/4 de la unidad de ancho base del cuadro de diálogo. Las unidades verticales son 1/8 de la unidad de alto del cuadro de diálogo. Las unidades base de diálogo actuales se calculan a partir del alto y el ancho de la fuente del sistema actual. La función [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) devuelve las unidades base de cuadro de diálogo en píxeles. Las coordenadas son relativas al origen del cuadro de diálogo.

 

 