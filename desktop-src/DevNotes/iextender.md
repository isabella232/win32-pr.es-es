---
description: La interfaz IE archiving proporciona un conjunto de propiedades básicas que se agregan a la interfaz de un control . Los programadores pueden usar estas propiedades como si formases parte del control.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: Interfaz IE archiving
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
ms.openlocfilehash: a341f5d8a0ec554f008232f44156486df83d0fd8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625121"
---
# <a name="iextender-interface"></a>Interfaz IE archiving

La **interfaz IE archiving** proporciona un conjunto de propiedades básicas que se agregan a la interfaz de un control . Los programadores pueden usar estas propiedades como si formases parte del control.

## <a name="members"></a>Miembros

La **interfaz IE archiving** hereda de la interfaz [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IE archiving** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IE archiving** tiene estos métodos.



| Método                         | Descripción                                    |
|:-------------------------------|:-----------------------------------------------|
| [**Move**](iextender-move.md) | Mueve un MDIForm, un formulario o un control.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IE archiving** tiene estas propiedades.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Propiedad</th>
<th >Tipo de acceso</th>
<th >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td >Alinear<br/></td>
<td >Lectura/escritura<br/></td>
<td >Devuelve o establece un valor que determina si un objeto se muestra en cualquier tamaño en cualquier lugar de un formulario o si se muestra en la parte superior, inferior, izquierda o derecha del formulario y se ajusta automáticamente para ajustarse al ancho del formulario.<br/> 
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
<td>(Valor predeterminado en un formulario que no es MDI) Ninguno: el tamaño y la ubicación se pueden establecer en tiempo de diseño o en código. La configuración se omite si el objeto está en un formulario MDI.</td>
</tr>
<tr class="even">
<td>vbAlignTop 1</td>
<td>(Valor predeterminado en un formulario MDI) Top: el objeto está en la parte superior del formulario y su ancho es igual al valor de la propiedad ScaleWidth del formulario.</td>
</tr>
<tr class="odd">
<td>vbAlignBottom 2</td>
<td>Bottom: el objeto está en la parte inferior del formulario y su ancho es igual al valor de la propiedad ScaleWidth del formulario.</td>
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
<td ><p>Contenedor</p></td>
<td ><p>Solo lectura</p></td>
<td ><p>Devuelve el contenedor de un control en un formulario.</p></td>
</tr>
<tr class="odd">
<td ><p>habilitado</p></td>
<td ><p>Lectura/escritura</p></td>
<td ><p>Devuelve o establece un valor que determina si un formulario o control puede responder a eventos generados por el usuario.</p></td>
</tr>
<tr class="even">
<td ><p>Alto</p></td>
<td ><p>Lectura/escritura</p></td>
<td ><p>Devuelve o establece el alto de un objeto .</p></td>
</tr>
<tr class="odd">
<td ><p>Hwnd</p></td>
<td ><p>Solo lectura</p></td>
<td ><p>Devuelve un identificador a un formulario o control.</p></td>
</tr>
<tr class="even">
<td ><p>Left</p></td>
<td ><p>Lectura/escritura</p></td>
<td ><p>Devuelve o establece la distancia entre el borde izquierdo interno de un objeto y el borde izquierdo de su contenedor.</p></td>
</tr>
<tr class="odd">
<td ><p>Nombre</p></td>
<td ><p>Solo lectura</p></td>
<td ><p>Devuelve el nombre utilizado en el código para identificar un formulario, un control o un objeto de acceso a datos.</p></td>
</tr>
<tr class="even">
<td ><p>Parent</p></td>
<td ><p>Solo lectura</p></td>
<td ><p>Devuelve el formulario, el objeto o la colección que contiene un control u otro objeto o colección.</p></td>
</tr>
<tr class="odd">
<td ><p>Tabstop</p></td>
<td ><p>Lectura/escritura</p></td>
<td ><p>Devuelve o establece un valor que indica si un usuario puede usar la tecla <strong>Tab</strong> para dar el foco a un objeto.</p></td>
</tr>
<tr class="even">
<td ><p>Superior</p></td>
<td ><p>Lectura/escritura</p></td>
<td ><p>Devuelve o establece la distancia entre el borde superior interno de un objeto y el borde superior de su contenedor.</p></td>
</tr>
<tr class="odd">
<td ><p>Visible</p></td>
<td ><p>Lectura/escritura</p></td>
<td ><p>Devuelve o establece un valor que indica si un objeto está visible u oculto.</p></td>
</tr>
<tr class="even">
<td ><p>Ancho</p></td>
<td ><p>Lectura/escritura</p></td>
<td ><p>Devuelve o establece el ancho de un objeto .</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



 

 
