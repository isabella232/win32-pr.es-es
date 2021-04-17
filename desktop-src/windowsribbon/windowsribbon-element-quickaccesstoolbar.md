---
title: Elemento QuickAccessToolbar
description: Representa la barra de herramientas de acceso rápido (QAT), una pequeña barra de herramientas que muestra accesos directos a comandos de la cinta de opciones.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- QuickAccessToolbar cinta de opciones de Windows
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0076890a8d9858d4bf410ecfdd866bf4f48fdbb6
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420197"
---
# <a name="quickaccesstoolbar-element"></a>Elemento QuickAccessToolbar

Representa la [barra de herramientas de acceso rápido (Qat)](windowsribbon-controls-quickaccesstoolbar.md), una pequeña barra de herramientas que muestra accesos directos a comandos de la cinta de opciones.

## <a name="usage"></a>Uso

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
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
<tr class="even">
<td><strong>CustomizeCommandName</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td>Inserta un elemento de comando adicional en el menú QAT.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                                   | Descripción                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | Puede aparecer como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**Ribbon. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Observaciones

Obligatorio.

Debe aparecer exactamente una vez para cada [**cinta. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).

Los elementos de QAT se pueden agregar o quitar en tiempo de ejecución.

Para mantener la coherencia entre las aplicaciones de la cinta de opciones, se recomienda que el controlador de comandos *CustomizeCommandName* inicie un cuadro de diálogo de personalización de Qat.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para **QuickAccessToolbar**.

En esta sección de código se muestra la declaración del comando **QuickAccessToolbar** .


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



En esta sección de código se muestra la declaración de control **QuickAccessToolbar** .


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control de barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





