---
title: E (menús y otros recursos)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149828"
---
# <a name="e-menus-and-other-resources"></a>E (menús y otros recursos)

[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [o](o.md) p Q [R](r.md) s [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z

<dl> <dt>

<span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**No se permiten menús vacíos**
</dt> <dd>

Aparece una palabra clave **End** antes de que se defina algún elemento de menú en la instrucción de [**menú**](menu-resource.md) . El compilador de recursos de Microsoft Windows 32 (RC) no permite menús vacíos. Asegúrese de que no tiene Comillas de apertura dentro de la instrucción de **menú** .

</dd> <dt>

<span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**Se esperaba END en el cuadro de diálogo**
</dt> <dd>

La palabra clave **End** debe aparecer al final de una instrucción [**Dialog**](dialog-resource.md) . Asegúrese de que no quedan comillas de apertura de la instrucción anterior.

</dd> <dt>

<span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**Se esperaba END en el menú**
</dt> <dd>

La palabra clave **End** debe aparecer al final de una instrucción [**Menu**](menu-resource.md) . Asegúrese de que no hay instrucciones **Begin** y **End** no coincidentes.

</dd> <dt>

<span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Creatingresource de error: nombre**
</dt> <dd>

El compilador de recursos de Microsoft Windows 32 (RC) no pudo crear el recurso binario especificado (. RES). Asegúrese de que no se está creando en una unidad de solo lectura. Use la opción **/v** para averiguar si se está creando el archivo.

</dd> <dt>

<span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Coma esperada en la tabla de aceleradores**
</dt> <dd>

El compilador de recursos 32 de Microsoft Windows (RC) requiere una coma entre los parámetros *Event* y *idvalue* de la instrucción [**Accelerators**](accelerators-resource.md) .

</dd> <dt>

<span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Se esperaba un nombre de clase de control**
</dt> <dd>

El parámetro de *clase* de una instrucción de [**control**](control-control.md) en la instrucción [**Dialog**](dialog-resource.md) debe ser uno de los siguientes tipos de control: **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** o definido por el usuario. Asegúrese de que la clase está escrita correctamente.

</dd> <dt>

<span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Se esperaba un nombre de fuente**
</dt> <dd>

El parámetro de tipo de *letra* de la instrucción **Font** de la instrucción [**Dialog**](dialog-resource.md) debe ser una cadena de caracteres entre comillas dobles ("). Este parámetro especifica el nombre de una fuente.

</dd> <dt>

<span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Se esperaba un valor de identificador para MenuItem**
</dt> <dd>

La instrucción [**Menu**](menu-resource.md) debe contener una instrucción [**MenuItem**](menuitem-statement.md) , que tiene un entero o una constante simbólica en el parámetro *menuid* .

</dd> <dt>

<span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Se esperaba una cadena de menú**
</dt> <dd>

Cada instrucción [**MenuItem**](menuitem-statement.md) y [**popup**](popup-resource.md) debe contener un parámetro de *texto* . Este parámetro es una cadena entre comillas dobles (") que especifica el nombre del elemento de menú o menú emergente. Una instrucción **MenuItem separator** no requiere ninguna cadena entrecomillada.

</dd> <dt>

<span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Valor de comando numérico esperado**
</dt> <dd>

El compilador de recursos de Microsoft Windows (RC) esperaba un parámetro *idvalue* numérico en la instrucción [**Accelerators**](accelerators-resource.md) . Asegúrese de que ha usado una instrucción [**\# define**](-define.md) para especificar el valor y que la constante usada está escrita correctamente.

</dd> <dt>

<span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Se esperaba una constante numérica en la tabla de cadenas**
</dt> <dd>

Una constante numérica, definida en una instrucción [**\# define**](-define.md) , debe seguir inmediatamente a la palabra clave **Begin** en una instrucción [**stringtable**](stringtable-resource.md) .

</dd> <dt>

<span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Se esperaba un tamaño de punto numérico**
</dt> <dd>

El parámetro de *puntuación* de la instrucción [**Font**](font-statement.md) en la instrucción [**Dialog**](dialog-resource.md) debe ser un valor entero de tamaño de punto.

</dd> <dt>

<span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Se esperaba una constante de cuadro de diálogo numérica**
</dt> <dd>

Una instrucción [**Dialog**](dialog-resource.md) requiere valores enteros para los parámetros *x*, *y*, *ancho* y *alto* . Asegúrese de que estos valores, que se incluyen después de la palabra clave **Dialog** , no sean negativos.

</dd> <dt>

<span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Se esperaba una cadena en STRINGTABLE**
</dt> <dd>

Se espera una cadena después de cada parámetro *stringid* numérico en una instrucción [**stringtable**](stringtable-resource.md) .

</dd> <dt>

<span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Comando de acelerador de constante o cadena esperado**
</dt> <dd>

El compilador de recursos de Microsoft Windows (RC) no pudo determinar qué clave se estaba configurando para el acelerador. Es posible que el parámetro de *evento* de la instrucción [**Accelerators**](accelerators-resource.md) no sea válido.

</dd> <dt>

<span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Se esperaba la palabra clave VALUE, BLOCK o END.**
</dt> <dd>

La estructura [**versionInfo**](versioninfo-resource.md) requiere una palabra clave **Value**, **Block** o **End** .

</dd> <dt>

<span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Se espera un número para el identificador**
</dt> <dd>

Se espera un número para el parámetro *ID* de una instrucción de [**control**](control-control.md) en la instrucción [**Dialog**](dialog-resource.md) . Asegúrese de que tiene un número o una instrucción de [**\# definición**](-define.md) para el identificador de control.

</dd> <dt>

<span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Se espera una cadena entre comillas para la clave**
</dt> <dd>

La cadena de clave que sigue a la palabra clave **Block** o **Value** se debe incluir entre comillas dobles.

</dd> <dt>

<span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Se espera una cadena entrecomillada en una clase de cuadro de diálogo**
</dt> <dd>

El parámetro *Class* de la instrucción [**Class**](class-statement.md) en la instrucción [**Dialog**](dialog-resource.md) debe ser un entero o una cadena entre comillas dobles (").

</dd> <dt>

<span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Se espera una cadena entrecomillada en el título del cuadro de diálogo**
</dt> <dd>

El parámetro *captiontext* de la instrucción [**Caption**](caption-statement.md) de la instrucción [**Dialog**](dialog-resource.md) debe ser una cadena de caracteres, entre comillas dobles (").

</dd> </dl>

 

 




