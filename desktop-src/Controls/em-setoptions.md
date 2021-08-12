---
title: EM_SETOPTIONS mensaje (Richedit.h)
description: Establece las opciones de un control de edición enriquecido.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- EM_SETOPTIONS controles de Windows mensaje
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
ms.openlocfilehash: a5d5c4b7fd9e92261cedaf0681523ad0a3e25a37aa2814f6c00d0d9460e94bb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672614"
---
# <a name="em_setoptions-message"></a>Mensaje DE EM \_ SETOPTIONS

Establece las opciones de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica la operación , que puede ser uno de estos valores.



| Value                                                                                                                                             | Significado                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ECOOP \_ SET**</dt> </dl> | Establece las opciones en las especificadas por *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ OR**</dt> </dl>    | Combina las opciones especificadas con las opciones actuales.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ AND**</dt> </dl> | Conserva solo las opciones actuales que también se especifican mediante *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | Excluye lógicamente O las opciones actuales con las especificadas *por lParam*.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica uno o varios de los valores siguientes.



| Value                                                                                                                                                                                 | Significado                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <dt>**ECO \_ AUTOWORDSELECTION**</dt> </dl> | Selección automática de palabras al hacer doble clic.<br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <dt>**ECO \_ AUTOVSCROLL**</dt> </dl>                   | Igual que [**el \_ estilo ES AUTOVSCROLL.**](rich-edit-control-styles.md)<br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <dt>**ECO \_ AUTOHSCROLL**</dt> </dl>                   | Igual que [**el \_ estilo ES AUTOHSCROLL.**](rich-edit-control-styles.md)<br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <dt>**ECO \_ NOHIDESEL**</dt> </dl>                         | Igual que [**el \_ estilo ES NOHIDESEL.**](rich-edit-control-styles.md)<br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <dt>**ECO \_ READONLY**</dt> </dl>                            | Igual que [**el \_ estilo ES READONLY.**](rich-edit-control-styles.md)<br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <dt>**ECO \_ WANTRETURN**</dt> </dl>                      | Igual que [**el \_ estilo ES WANTRETURN.**](rich-edit-control-styles.md)<br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <dt>**BARRA \_ DE SELECCIÓN ECO**</dt> </dl>                | Igual que [**el estilo \_ ES SELECTIONBAR.**](rich-edit-control-styles.md)<br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <dt>**ECO \_ VERTICAL**</dt> </dl>                            | Igual que [**el estilo VERTICAL \_ de ES.**](rich-edit-control-styles.md) Disponible solo en versiones en idioma asiático.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve las opciones actuales del control de edición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estilos de control Rich Edit**](rich-edit-control-styles.md)
</dt> </dl>

 

 





