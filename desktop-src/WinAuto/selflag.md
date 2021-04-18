---
title: Constantes SELFLAG (oleacc. h)
description: En este tema se describen los valores constantes que se usan para especificar cómo se selecciona un objeto accesible o se toma el foco.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718761"
---
# <a name="selflag-constants"></a>Constantes de SELFLAG

En este tema se describen los valores constantes que se usan para especificar cómo se selecciona un objeto accesible o se toma el foco. Las constantes se definen en oleacc. h y se usan con el método [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) .

No se permiten las siguientes combinaciones:

-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ REMOVESELECTION
-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION

**Nota para los clientes:** Microsoft Active Accessibility no admite la selección del texto contenido en los controles de edición y edición enriquecida porque el texto se expone como una cadena en la [propiedad Value](value-property.md)del objeto.

Para obtener información sobre cómo realizar operaciones de selección complejas, consulte [seleccionar objetos secundarios](selecting-child-objects.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante o valor</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </dl></td>
<td style="text-align: left;">No realiza ninguna acción. Microsoft Active Accessibility no cambia la selección o el foco.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </dl></td>
<td style="text-align: left;">Establece el foco en el objeto y lo convierte en el delimitador de selección. Este marcador, que se usa por sí solo, no modifica la selección. El efecto es similar a mover el foco manualmente presionando una tecla de dirección mientras mantiene presionada la tecla CTRL en el explorador de Windows o en cualquier cuadro de lista de selección múltiple. <br/> Con los objetos que tienen el <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS se combina con los valores siguientes:<br/>
<ul>
<li>SELFLAG_TAKESELECTION</li>
<li>SELFLAG_EXTENDSELECTION</li>
<li>SELFLAG_ADDSELECTION</li>
<li>SELFLAG_REMOVESELECTION</li>
<li>SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</li>
<li>SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</li>
</ul>
Si se llama a <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible:: accSelect</strong></a> con la marca SELFLAG_TAKEFOCUS en un objeto que tiene un <strong>hWnd</strong>, la marca solo tendrá efecto si el elemento primario del objeto ya tiene el foco.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0X2</dt> </dl></td>
<td style="text-align: left;">Selecciona el objeto y quita la selección de todos los demás objetos del contenedor. <br/> A menos que se combine con SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección. El SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a hacer un solo clic en un elemento del explorador de Windows.<br/> Esta marca no debe combinarse con las marcas siguientes:<br/>
<ul>
<li>SELFLAG_ADDSELECTION</li>
<li>SELFLAG_REMOVESELECTION</li>
<li>SELFLAG_EXTENDSELECTION</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </dl></td>
<td style="text-align: left;">Modifica la selección para que todos los objetos entre el delimitador de selección y este objeto tomen el estado de selección del objeto de delimitador. Si el objeto delimitador no está seleccionado, los objetos se quitan de la selección. Si se selecciona el objeto delimitador, la selección se extiende para incluir este objeto y todos los objetos que hay entre ellos. Establezca el estado de selección mediante la combinación de esta marca con SELFLAG_ADDSELECTION o SELFLAG_REMOVESELECTION. <br/> A menos que se combine con SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección. El SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a agregar un elemento a una selección manualmente manteniendo presionada la tecla Mayús y haciendo clic en un objeto no seleccionado en el explorador de Windows.<br/> Esta marca no se combina con SELFLAG_TAKESELECTION.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </dl></td>
<td style="text-align: left;">Agrega el objeto a la selección actual; el resultado posible es una selección no contigua. <br/> A menos que se combine con SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección. El SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a agregar un elemento a una selección manualmente manteniendo presionada la tecla CTRL y haciendo clic en un objeto no seleccionado en el explorador de Windows.<br/> Esta marca no se combina con SELFLAG_REMOVESELECTION o SELFLAG_TAKESELECTION.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </dl></td>
<td style="text-align: left;">Quita el objeto de la selección actual; el resultado posible es una selección no contigua. <br/> A menos que se combine con SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección. El SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a quitar un elemento de una selección manualmente, manteniendo presionada la tecla CTRL mientras hace clic en un objeto seleccionado en el explorador de Windows.<br/> Esta marca no se combina con SELFLAG_ADDSELECTION o SELFLAG_TAKESELECTION.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Oleacc. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[Seleccionar objetos secundarios](selecting-child-objects.md)
</dt> </dl>

 

 





