---
title: CFSTR_DSOP_DS_SELECTION_LIST (objsel. h)
description: El \_ formato del \_ portapapeles de la lista de selección DS de CFSTR DSOP \_ \_ proporciona un hglobal que contiene una estructura de lista de selección de DS \_ \_ . La estructura de la \_ lista de selección \_ de DS contiene datos sobre los elementos seleccionados en el cuadro de diálogo Selector de objetos de directorio.
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996231"
---
# <a name="cfstr_dsop_ds_selection_list"></a>CFSTR \_ DSOP \_ \_ lista de selección DS \_

<dl> <dt>

<span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR \_ DSOP \_ \_ lista de selección DS \_**
</dt> <dd> <dl> <dt>

"CFSTR \_ DSOP \_ DS \_ Selection \_ List"
</dt> <dt>



El formato del portapapeles de la **lista de \_ \_ \_ selección \_ DS CFSTR DSOP** se proporciona [**mediante la llamada**](/windows/win32/api/objidl/nn-objidl-idataobject) a [**IDsObjectPicker:: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog). El formato del portapapeles de la **\_ \_ \_ \_ lista de selección DS de CFSTR DSOP** proporciona un **HGLOBAL** que contiene una estructura de [**lista de \_ selección \_ de DS**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) . La estructura de la **\_ \_ lista de selección de DS** contiene datos sobre los elementos seleccionados en el cuadro de diálogo Selector de objetos de [directorio](directory-object-picker.md) .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Objsel. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_lista de selección de DS \_**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[Selector de objetos de directorio](directory-object-picker.md)
</dt> </dl>

 

