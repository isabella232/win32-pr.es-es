---
title: Mensaje EM_SETOPTIONS (RichEdit. h)
description: Establece las opciones de un control Rich Edit.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- EM_SETOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150199"
---
# <a name="em_setoptions-message"></a>\_Mensaje SETOPTIONS em

Establece las opciones de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica la operación, que puede ser uno de estos valores.



| Value                                                                                                                                             | Significado                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**conjunto de ECOOP \_**</dt> </dl> | Establece las opciones en las especificadas por *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ o**</dt> </dl>    | Combina las opciones especificadas con las opciones actuales.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ y**</dt> </dl> | Conserva solo las opciones actuales que también especifica *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | Lógicamente exclusivas o las opciones actuales con las especificadas por *lParam*.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica uno o varios de los valores siguientes.



| Value                                                                                                                                                                                 | Significado                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <dt>**AUTOWORDSELECTION de ECO \_**</dt> </dl> | Selección automática de palabra al hacer doble clic.<br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <dt>**AUTOVSCROLL de ECO \_**</dt> </dl>                   | Igual que el estilo [**\_ AUTOVSCROLL**](rich-edit-control-styles.md) .<br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <dt>**AUTOHSCROLL de ECO \_**</dt> </dl>                   | Igual que el estilo [**\_ AUTOHSCROLL**](rich-edit-control-styles.md) .<br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <dt>**NOHIDESEL de ECO \_**</dt> </dl>                         | Igual que el estilo [**\_ NOHIDESEL**](rich-edit-control-styles.md) .<br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <dt>**\_solo lectura de eco**</dt> </dl>                            | Igual que el estilo de [**\_ solo lectura**](rich-edit-control-styles.md) .<br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <dt>**WANTRETURN de ECO \_**</dt> </dl>                      | Igual que el estilo [**\_ WANTRETURN**](rich-edit-control-styles.md) .<br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <dt>**SELECTIONBAR de ECO \_**</dt> </dl>                | Igual que el estilo [**\_ SELECTIONBAR**](rich-edit-control-styles.md) .<br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <dt>**\_vertical ecológica**</dt> </dl>                            | Igual que el estilo [**\_ vertical**](rich-edit-control-styles.md) . Disponible solo en versiones de idioma asiático.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve las opciones actuales del control de edición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estilos de control Rich Edit**](rich-edit-control-styles.md)
</dt> </dl>

 

 





