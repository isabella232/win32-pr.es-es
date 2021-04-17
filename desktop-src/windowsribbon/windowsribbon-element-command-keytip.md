---
title: Command. KeyTip (propiedad)
description: Representa el KeyTip de un control.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Command. KeyTip (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705177"
---
# <a name="commandkeytip-property"></a>Command. KeyTip (propiedad)

Representa el KeyTip de un control.

## <a name="usage"></a>Uso

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                   | Descripción                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**String@**](windowsribbon-element-string.md)<br/> | Puede aparecer como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse una vez como máximo para cada elemento [**Command**](windowsribbon-element-command.md) .

**Command. KeyTip** puede contener un valor de tipo *xs: String* restringido a cualquier secuencia de caracteres Unicode, incluido el espacio en blanco.

Un **comando. KeyTip** solo puede empezar con un número cuando está asociado a un control en una [pestaña](windowsribbon-controls-tab.md) o en la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md).

Para mostrar las keytips que son válidas para el estado actual de la cinta de opciones, mantenga presionada la tecla ALT. En la captura de pantalla siguiente se muestran las keytips iniciales, o el primer nivel, que se muestran en Microsoft Paint para Windows 7. Una vez que se ha seleccionado un KeyTip de primer nivel, solo se muestran las keytips de segundo nivel.

![keytips de primer nivel en Microsoft Paint para Windows 7](images/properties/ui-pkey-label-keytips.png)

**Command. KeyTip** actúa como la tecla de aceleración de un comando, a menos que ese comando se exponga a través de un elemento de menú. En este caso, el marco de trabajo omite el valor de **Command. KeyTip** y usa un carácter precedido por una y comercial según lo especificado por [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o la [ \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario. Si no se especifica el carácter de y comercial mediante la etiqueta **Command. LabelTitle** o UI \_ PKEY \_ , no se expone ningún KeyTip ni tecla de aceleración.

Si no se proporciona ningún valor para **Command. KeyTip**, se requiere el elemento secundario de [**cadena**](windowsribbon-element-string.md) .

> [!Note]  
> Si **Command. KeyTip** contiene un valor y un elemento secundario de [**cadena**](windowsribbon-element-string.md) , la **cadena** tiene prioridad.

 

De forma predeterminada, el marco de trabajo usa las siguientes letras para generar automáticamente keytips:

-   **F** está asignado al menú de la [aplicación](windowsribbon-controls-applicationmenu.md).
-   **Y** se asigna a cualquier comando que no tenga un KeyTip especificado por la aplicación.
-   **Z** se asigna a cada control de [Grupo](windowsribbon-controls-group.md) y no se puede personalizar. Un KeyTip de grupo solo se muestra cuando el [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) del control especifica una opción de tamaño de **elemento emergente** . Para obtener más información, vea [personalizar una cinta de opciones a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md).

> [!Note]  
> Ninguna de estas letras está reservada por el marco de trabajo. Cada una de ellas se puede asignar a uno o varios comandos, según sea necesario.

 

El marco de trabajo resuelve los conflictos de KeyTip de las siguientes maneras:

-   Si uno o más controles de [ficha](windowsribbon-controls-tab.md) están asociados al mismo KeyTip, se anexa un número a cada KeyTip, empezando por 1 y aumentando secuencialmente (2, 3,...) para cada control en el orden de declaración. Si a algún control de ficha se le asigna la letra F como KeyTip, al [menú aplicación](windowsribbon-controls-applicationmenu.md) se le asigna F1 con las keytips restantes ajustadas como se describe.
-   Cuando se asocia a un solo control dentro de una [pestaña](windowsribbon-controls-tab.md), el KeyTip F es válido para el menú de control y la [aplicación](windowsribbon-controls-applicationmenu.md). El KeyTip del menú de la aplicación predeterminado no cambia, pero se da prioridad al control en la pestaña activa.
-   Si uno o más controles de una [pestaña](windowsribbon-controls-tab.md) están asociados al mismo KeyTip, el marco de trabajo refactoriza automáticamente las keytips de esos controles, como se describió anteriormente.

> [!Note]  
> Una ligera variación en el color del texto se usa para resaltar las keytips refactorizadas en una implementación de la cinta de opciones estándar. En el caso de una implementación de cinta no estándar en la que se ha personalizado el color de la cinta de opciones, este comportamiento del marco de trabajo se invalida y todas las keytips se muestran con el mismo color de texto. Para obtener más información, vea [personalizar los colores de la cinta](ribbon-color.md)de opciones.

 

La longitud máxima es sin límite.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de un elemento [**Command**](windowsribbon-element-command.md) con una declaración **Command. KeyTip** .


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[KeyTip de UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





