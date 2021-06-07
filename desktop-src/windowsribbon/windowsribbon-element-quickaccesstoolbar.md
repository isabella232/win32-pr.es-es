---
title: QuickAccessToolbar, elemento
description: Representa la barra de herramientas de acceso rápido (QAT), una pequeña barra de herramientas que muestra accesos directos a los comandos de la cinta de opciones.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Cinta de opciones de Windows del elemento QuickAccessToolbar
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ae01f620d66298a5f7200d0be947dbfb3750af4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443306"
---
# <a name="quickaccesstoolbar-element"></a>QuickAccessToolbar, elemento

Representa la [barra de herramientas de acceso rápido (QAT),](windowsribbon-controls-quickaccesstoolbar.md)una pequeña barra de herramientas que muestra accesos directos a los comandos de la cinta de opciones.

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
<th>Requerido</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CustomizeCommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Inserta un elemento Command adicional en el menú QAT.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                                   | Descripción                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | Puede producirse como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Comentarios

Necesario.

Debe producirse exactamente una vez para [**cada ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).

Los elementos del QAT se pueden agregar o quitar en tiempo de ejecución.

Para mantener la coherencia entre las aplicaciones de la cinta de opciones, se recomienda que el controlador de comandos *CustomizeCommandName* inicie un cuadro de diálogo de personalización de QAT.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para **QuickAccessToolbar**.

En esta sección de código se muestra **la declaración QuickAccessToolbar** Command.


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



En esta sección de código se muestra la declaración de control **QuickAccessToolbar.**


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

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





