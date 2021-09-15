---
description: Representa las opciones disponibles al mostrar un menú emergente.
title: MP_POPUPFLAGS constantes (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360363"
---
# <a name="mp_popupflags-constants"></a>Constantes \_ POPUPFLAGS de MP

Representa las opciones disponibles al mostrar un menú emergente.



| Constante o valor                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <dt>**MPPF \_ SETFOCUS**</dt> <dt>0x00000001</dt> </dl>                | Dé el foco al menú emergente.<br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <dt>**MPPF \_ INITIALSELECT**</dt> <dt>0x00000002</dt> </dl> | Seleccione el primer elemento del menú emergente.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <dt>**MPPF \_ Noanimate**</dt> <dt>0x00000004</dt> </dl>             | No use las animaciones predeterminadas del sistema, por ejemplo, atenuación, al mostrar el menú.<br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <dt>**MPPF \_ Teclado**</dt> <dt>0x00000010</dt> </dl>                | Active el menú mediante un método abreviado de teclado.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <dt>**MPPF \_ REPOSITION**</dt> <dt>0x00000020</dt> </dl>          | Muestre la barra en una posición diferente, en función de los cambios en el menú.<br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <dt>**MPPF \_ ForceZORDER**</dt> <dt>0x00000040</dt> </dl>       | Reservado. No utilizar.<br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <dt>**MPPF \_ FINALSELECT**</dt> <dt>0x00000080</dt> </dl>       | Seleccione el último elemento del menú.<br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <dt>**MPPF \_ ALIGN \_ LEFT**</dt> <dt>0x02000000</dt> </dl>         | **Windows Vista** o posterior: alinee el menú emergente a la izquierda del área especificada en el parámetro *prcExclude* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup). Esta es la alineación predeterminada.<br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <dt>**MPPF \_ ALINEAR \_ A la**</dt> derecha <dt>0x04000000</dt> </dl>      | **Windows Vista** o posterior: alinee el menú emergente a la derecha del área especificada en el parámetro *prcExclude* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <dt>**MPPF \_ TOP**</dt> <dt>0x20000000</dt> </dl>                               | Coloque el menú emergente encima del punto inicial especificado en el parámetro *ppt* [**de ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) [**o IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <dt>**MPPF \_ Left**</dt> <dt>0x40000000</dt> </dl>                            | Coloque el menú emergente a la izquierda del punto inicial.<br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <dt>**MPPF \_ Right**</dt> <dt>0x60000000</dt> </dl>                         | Coloque el menú emergente a la derecha del punto inicial.<br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <dt>**MPPF \_ BOTTOM**</dt> <dt>(int)0x80000000</dt> </dl>                 | Coloque el menú emergente debajo del punto inicial.<br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <dt>**MPPF \_ POS \_ MASK**</dt> <dt>(int)0xE0000000</dt> </dl>          | Máscara de posición del menú.<br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a>Observaciones

Estas constantes se definen en el archivo Shobjidl.h a partir de Windows XP Service Pack 1 (SP1) y Windows Server 2003

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp1\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




