---
title: E (menús y otros recursos)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252423"
---
# <a name="e-menus-and-other-resources"></a>E (menús y otros recursos)

[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P P [Q R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z

<dl> <dt>

<span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**No se permiten menús vacíos**
</dt> <dd>

Aparece **una palabra** clave END antes de definir los elementos de menú en la instrucción [**MENU.**](menu-resource.md) Microsoft Windows 32 Resource Compiler (RC) no permite los menús vacíos. Asegúrese de que no tiene comillas de apertura dentro de la **instrucción MENU.**

</dd> <dt>

<span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**Se esperaba END en el cuadro de diálogo**
</dt> <dd>

La **palabra clave END** debe aparecer al final de una instrucción [**DIALOG.**](dialog-resource.md) Asegúrese de que no quedan comillas de apertura de la instrucción anterior.

</dd> <dt>

<span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**Se esperaba END en el menú**
</dt> <dd>

La **palabra clave END** debe aparecer al final de una instrucción [**MENU.**](menu-resource.md) Asegúrese de que no hay instrucciones **BEGIN** y **END** no coincidentes.

</dd> <dt>

<span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Error al crearresource-name**
</dt> <dd>

Microsoft Windows 32 Resource Compiler (RC) no pudo crear el recurso binario especificado (. RES). Asegúrese de que no se crea en una unidad de solo lectura. Use la **opción /v** para averiguar si se está creando el archivo.

</dd> <dt>

<span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Coma esperada en la tabla de aceleradores**
</dt> <dd>

Microsoft Windows 32 Resource Compiler (RC) requiere una coma entre los parámetros *event* e *idvalue* de la [**instrucción ACCELERATORS.**](accelerators-resource.md)

</dd> <dt>

<span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Nombre de clase de control esperado**
</dt> <dd>

El *parámetro* de clase de una [**instrucción CONTROL**](control-control.md) de la instrucción [**DIALOG**](dialog-resource.md) debe ser uno de los siguientes tipos de control: **BUTTON**, [**COMBOBOX**](combobox-control.md), **EDIT**, [**LISTBOX**](listbox-control.md), [**SCROLLBAR,**](scrollbar-control.md) **STATIC** o definidos por el usuario. Asegúrese de que la clase está correctamente deletreada.

</dd> <dt>

<span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Nombre de la cara de fuente esperado**
</dt> <dd>

El *parámetro typeface* de la **instrucción FONT** de la instrucción [**DIALOG**](dialog-resource.md) debe ser una cadena de caracteres entre comillas dobles ("). Este parámetro especifica el nombre de una fuente.

</dd> <dt>

<span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Valor de identificador esperado para Menuitem**
</dt> <dd>

La [**instrucción MENU**](menu-resource.md) debe contener una instrucción [**MENUITEM,**](menuitem-statement.md) que tiene un entero o una constante simbólica en el *parámetro MenuID.*

</dd> <dt>

<span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Cadena de menú esperada**
</dt> <dd>

Cada [**instrucción MENUITEM**](menuitem-statement.md) [**y POPUP**](popup-resource.md) debe contener un parámetro *de* texto. Este parámetro es una cadena entre comillas dobles (") que especifica el nombre del elemento de menú o del menú emergente. Una **instrucción MENUITEM SEPARATOR** no requiere ninguna cadena entre comillas.

</dd> <dt>

<span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Valor de comando numérico esperado**
</dt> <dd>

Microsoft Windows Resource Compiler (RC) esperaba un parámetro *idvalue* numérico en la [**instrucción ACCELERATORS.**](accelerators-resource.md) Asegúrese de que ha usado una instrucción [**\# define**](-define.md) para especificar el valor y de que la constante usada está escrita correctamente.

</dd> <dt>

<span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Constante numérica esperada en la tabla de cadenas**
</dt> <dd>

Una constante numérica, definida en una [**\# instrucción define,**](-define.md) debe seguir inmediatamente la palabra clave **BEGIN** en una [**instrucción STRINGTABLE.**](stringtable-resource.md)

</dd> <dt>

<span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Tamaño de punto numérico esperado**
</dt> <dd>

El *parámetro pointsize* de la [**instrucción FONT**](font-statement.md) de la instrucción [**DIALOG**](dialog-resource.md) debe ser un valor de tamaño de punto entero.

</dd> <dt>

<span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Constante de cuadro de diálogo numérico esperado**
</dt> <dd>

Una [**instrucción DIALOG**](dialog-resource.md) requiere valores enteros para los parámetros *x*, *y*, *width* y *height.* Asegúrese de que estos valores, que se incluyen después de la palabra clave **DIALOG,** no sean negativos.

</dd> <dt>

<span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Cadena esperada en STRINGTABLE**
</dt> <dd>

Se espera una cadena después de cada parámetro *stringid* numérico en una [**instrucción STRINGTABLE.**](stringtable-resource.md)

</dd> <dt>

<span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Comando Cadena esperada o Acelerador de constantes**
</dt> <dd>

Microsoft Windows Resource Compiler (RC) no pudo determinar qué clave se estaba configurando para el acelerador. El *parámetro de* evento de la instrucción [**ACCELERATORS**](accelerators-resource.md) podría no ser válido.

</dd> <dt>

<span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Palabra clave VALUE, BLOCK o END esperada.**
</dt> <dd>

La [**estructura VERSIONINFO**](versioninfo-resource.md) requiere una palabra clave **VALUE,** **BLOCK** **o END.**

</dd> <dt>

<span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Número esperado para el identificador**
</dt> <dd>

Se espera un número para el *parámetro id* de una [**instrucción CONTROL**](control-control.md) en la [**instrucción DIALOG.**](dialog-resource.md) Asegúrese de que tiene un número o una instrucción [**\# define**](-define.md) para el identificador de control.

</dd> <dt>

<span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Esperar cadena entre comillas para la clave**
</dt> <dd>

La cadena de clave que sigue **a la palabra** clave BLOCK o **VALUE** debe ir entre comillas dobles.

</dd> <dt>

<span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Esperar cadena entre comillas en la clase de diálogo**
</dt> <dd>

El *parámetro* de clase de la [**instrucción CLASS**](class-statement.md) de la instrucción [**DIALOG**](dialog-resource.md) debe ser un entero o una cadena entre comillas dobles (").

</dd> <dt>

<span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Esperar cadena entre comillas en el título del cuadro de diálogo**
</dt> <dd>

El *parámetro captiontext* de la [**instrucción CAPTION**](caption-statement.md) de la instrucción [**DIALOG**](dialog-resource.md) debe ser una cadena de caracteres, entre comillas dobles (").

</dd> </dl>

 

 




