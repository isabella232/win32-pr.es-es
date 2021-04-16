---
title: Elemento HelpButton
description: Representa el control de botón de ayuda.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- HelpButton cinta de opciones de Windows
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be084ff6fc92d4eac4bbaffb3c507142f91eba8
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "105695522"
---
# <a name="helpbutton-element"></a>Elemento HelpButton

Representa el control de [botón de ayuda](windowsribbon-controls-helpbutton.md) .

## <a name="usage"></a>Uso

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Tipo</th>
<th>Obligatorio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Ribbon. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse una vez como máximo para cada cinta de opciones [**. HelpButton**](windowsribbon-element-ribbon-helpbutton.md).

Inicia un cuadro de diálogo de ayuda de la aplicación al hacer clic en él.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico necesario para implementar un control de [botón de ayuda](windowsribbon-controls-helpbutton.md) de la cinta de opciones.

En esta sección de código se muestra la declaración del comando **HelpButton** .


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



En esta sección de código se muestra la declaración de control **HelpButton** .


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | Sí       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control de botón de ayuda](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





