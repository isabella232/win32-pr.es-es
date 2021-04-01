---
title: Mensaje de CBEM_GETEDITCONTROL (commctrl. h)
description: Obtiene el identificador de la parte del control de edición de un control ComboBoxEx. Un control ComboBoxEx usa un cuadro de edición cuando se establece en el \_ estilo de lista desplegable CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150925"
---
# <a name="cbem_geteditcontrol-message"></a>CBEM \_ GETEDITCONTROL

Obtiene el identificador de la parte del control de edición de un control ComboBoxEx. Un control ComboBoxEx usa un cuadro de edición cuando se establece en el estilo de [**\_ lista desplegable CBS**](combo-box-styles.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de edición dentro del control ComboBoxEx si usa el estilo [**de \_ lista desplegable CBS**](combo-box-styles.md) . De lo contrario, el mensaje devuelve **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





