---
description: La interfaz IExtender proporciona un conjunto de propiedades básicas que se agregan a la interfaz de un control. Los programadores pueden utilizar estas propiedades como si formaran parte del control.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: Interfaz IExtender
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: fd600de816889e1c644a0e6074d9b8a97e0ec80c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660196"
---
# <a name="iextender-interface"></a>Interfaz IExtender

La interfaz **IExtender** proporciona un conjunto de propiedades básicas que se agregan a la interfaz de un control. Los programadores pueden utilizar estas propiedades como si formaran parte del control.

## <a name="members"></a>Miembros

La interfaz **IExtender** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IExtender** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IExtender** tiene estos métodos.



| Método                         | Descripción                                    |
|:-------------------------------|:-----------------------------------------------|
| [**Move**](iextender-move.md) | Mueve un control MDIForm, Form o.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IExtender** tiene estas propiedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propiedad</th>
<th style="text-align: left;">Tipo de acceso</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Alinear<br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Devuelve o establece un valor que determina si un objeto se muestra en cualquier tamaño de un formulario o si se muestra en la parte superior, inferior, izquierda o derecha del formulario y se ajusta automáticamente para ajustarse al ancho del formulario.<br/> 
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vbAlignNone 0</td>
<td>(Valor predeterminado en un formulario no MDI) Ninguno: el tamaño y la ubicación se pueden establecer en tiempo de diseño o en código. La configuración se omite si el objeto está en un formulario MDI.</td>
</tr>
<tr class="even">
<td>vbAlignTop 1</td>
<td>(Valor predeterminado en un formulario MDI) Top: el objeto se encuentra en la parte superior del formulario y su ancho es igual al valor de la propiedad ScaleWidth del formulario.</td>
</tr>
<tr class="odd">
<td>vbAlignBottom 2</td>
<td>Inferior: el objeto se encuentra en la parte inferior del formulario y su ancho es igual al valor de la propiedad ScaleWidth del formulario.</td>
</tr>
<tr class="even">
<td>vbAlignLeft 3</td>
<td>Left: el objeto está a la izquierda del formulario y su ancho es igual al valor de la propiedad ScaleWidth del formulario.</td>
</tr>
<tr class="odd">
<td>vbAlignRight 4</td>
<td>Right: el objeto está a la derecha del formulario y su ancho es igual al valor de la propiedad ScaleWidth del formulario.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Contenedor</p></td>
<td style="text-align: left;"><p>Solo lectura</p></td>
<td style="text-align: left;"><p>Devuelve el contenedor de un control en un formulario.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>habilitado</p></td>
<td style="text-align: left;"><p>Lectura/escritura</p></td>
<td style="text-align: left;"><p>Devuelve o establece un valor que determina si un formulario o un control puede responder a los eventos generados por el usuario.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Alto</p></td>
<td style="text-align: left;"><p>Lectura/escritura</p></td>
<td style="text-align: left;"><p>Devuelve o establece el alto de un objeto.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Identificador</p></td>
<td style="text-align: left;"><p>Solo lectura</p></td>
<td style="text-align: left;"><p>Devuelve un identificador a un formulario o un control.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Left</p></td>
<td style="text-align: left;"><p>Lectura/escritura</p></td>
<td style="text-align: left;"><p>Devuelve o establece la distancia entre el borde izquierdo interno de un objeto y el borde izquierdo de su contenedor.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Nombre</p></td>
<td style="text-align: left;"><p>Solo lectura</p></td>
<td style="text-align: left;"><p>Devuelve el nombre utilizado en el código para identificar un formulario, un control o un objeto de acceso a datos.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Parent</p></td>
<td style="text-align: left;"><p>Solo lectura</p></td>
<td style="text-align: left;"><p>Devuelve el formulario, objeto o colección que contiene un control u otro objeto o colección.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>TabStop</p></td>
<td style="text-align: left;"><p>Lectura/escritura</p></td>
<td style="text-align: left;"><p>Devuelve o establece un valor que indica si un usuario puede usar la tecla <strong>Tab</strong> para dar el foco a un objeto.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Superior</p></td>
<td style="text-align: left;"><p>Lectura/escritura</p></td>
<td style="text-align: left;"><p>Devuelve o establece la distancia entre el borde interno superior de un objeto y el borde superior de su contenedor.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Visible</p></td>
<td style="text-align: left;"><p>Lectura/escritura</p></td>
<td style="text-align: left;"><p>Devuelve o establece un valor que indica si un objeto está visible u oculto.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Ancho</p></td>
<td style="text-align: left;"><p>Lectura/escritura</p></td>
<td style="text-align: left;"><p>Devuelve o establece el ancho de un objeto.</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



 

 
