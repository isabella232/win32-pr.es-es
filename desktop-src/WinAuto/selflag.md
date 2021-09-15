---
title: Constantes SELF CONSTANT (Oleacc.h)
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
ms.openlocfilehash: a3b4d0384b66919a55d55593d2e16c9a187d84ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567384"
---
# <a name="selflag-constants"></a>Constantes SELF CONSTANT

En este tema se describen los valores constantes que se usan para especificar cómo se selecciona un objeto accesible o se toma el foco. Las constantes se definen en oleacc.h y se usan con el [**método IAccessible::accSelect.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

No se permiten las siguientes combinaciones:

-   SELFENSA \_ ADDSELECTION \| SELFSELECTION \_ REMOVESELECTION
-   SELFENSA \_ ADDSELECTION \| SELFSELECTION \_ TAKESELECTION
-   \_REMOVESELECTION \| SELFSELECTION \_ TAKESELECTION DE SELFSELECTION
-   AUTOSELECT \_ EXTENDSELECTION \| \_ SELFSELECTION TAKESELECTION

**Nota para los clientes:** Microsoft Active Accessibility no admite la selección del texto contenido en los controles de edición y edición enriquezca porque el texto se expone como una cadena en la propiedad [Value del objeto](value-property.md).

Para obtener información sobre cómo realizar operaciones de selección complejas, vea [Seleccionar objetos secundarios.](selecting-child-objects.md)




| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl><dt><strong>SELFLAG_NONE</strong></dt><dt>0</dt></dl> | No realiza ninguna acción. Microsoft Active Accessibility no cambia la selección ni el foco.<br /> | 
| <span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl><dt><strong>SELFLAG_TAKEFOCUS</strong></dt><dt>0x1</dt></dl> | Establece el foco en el objeto y lo convierte en el delimitador de selección. Usado por sí mismo, esta marca no modifica la selección. El efecto es similar a mover el foco manualmente presionando una tecla FLECHA mientras se mantiene presionada la tecla CTRL en Windows Explorer o en cualquier cuadro de lista de selección múltiple. <br /> Con los objetos que tienen <a href="object-state-constants.md"><strong>el STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS se combina con los valores siguientes:<br /><ul><li>SELFLAG_TAKESELECTION</li><li>SELFLAG_EXTENDSELECTION</li><li>SELFLAG_ADDSELECTION</li><li>SELFLAG_REMOVESELECTION</li><li>SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</li><li>SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</li></ul>Si llama a <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible::accSelect</strong></a> con la marca SELFLAG_TAKEFOCUS en un objeto que tiene un <strong>HWND</strong>, la marca solo surte efecto si el elemento primario del objeto ya tiene el foco.<br /> | 
| <span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl><dt><strong>SELFLAG_TAKESELECTION</strong></dt><dt>0x2</dt></dl> | Selecciona el objeto y quita la selección de todos los demás objetos del contenedor. <br /> A menos que se combine SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección. El SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a hacer un solo clic en un elemento en Windows Explorer.<br /> Esta marca no debe combinarse con las siguientes marcas:<br /><ul><li>SELFLAG_ADDSELECTION</li><li>SELFLAG_REMOVESELECTION</li><li>SELFLAG_EXTENDSELECTION</li></ul> | 
| <span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt><dt>0x4</dt></dl> | Modifica la selección para que todos los objetos entre el delimitador de selección y este objeto tomen el estado de selección del objeto delimitador. Si el objeto delimitador no está seleccionado, los objetos se quitan de la selección. Si se selecciona el objeto delimitador, la selección se amplía para incluir este objeto y todos los objetos entre ellos. Establezca el estado de selección combinando esta marca con SELFLAG_ADDSELECTION o SELFLAG_REMOVESELECTION. <br /> A menos que se combine SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección. El SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a agregar manualmente un elemento a una selección manteniendo presionada la tecla MAYÚS y haciendo clic en un objeto no seleccionado en Windows Explorer.<br /> Esta marca no se combina con SELFLAG_TAKESELECTION.<br /> | 
| <span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl><dt><strong>SELFLAG_ADDSELECTION</strong></dt><dt>0x8</dt></dl> | Agrega el objeto a la selección actual; el resultado posible es una selección no continua. <br /> A menos que se combine SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección. El SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a agregar manualmente un elemento a una selección manteniendo presionada la tecla CTRL y haciendo clic en un objeto no seleccionado en Windows Explorador.<br /> Esta marca no se combina con SELFLAG_REMOVESELECTION o SELFLAG_TAKESELECTION.<br /> | 
| <span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl><dt><strong>SELFLAG_REMOVESELECTION</strong></dt><dt>0x10</dt></dl> | Quita el objeto de la selección actual; el resultado posible es una selección no continua. <br /> A menos que se combine SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección. El SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a quitar manualmente un elemento de una selección, manteniendo presionada la tecla CTRL al hacer clic en un objeto seleccionado en Windows Explorador.<br /> Esta marca no se combina con SELFLAG_ADDSELECTION o SELFLAG_TAKESELECTION.<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Oleacc.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[Selección de objetos secundarios](selecting-child-objects.md)
</dt> </dl>

 

 





