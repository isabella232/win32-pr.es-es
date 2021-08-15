---
title: PSM_SETNEXTTEXT mensaje (Prsht.h)
description: Establece el texto del botón Siguiente en un asistente. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetNextText.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- PSM_SETNEXTTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d177acb2f2c96e12f5dc4b460ee88149ad81f9b4f79cc3505f776d8f1f92551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410085"
---
# <a name="psm_setnexttext-message"></a>Mensaje PSM \_ SETNEXTTEXT

Establece el texto del botón **Siguiente** en un asistente. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetNextText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer que contiene el texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No hay ningún valor devuelto significativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **PSM \_ SETNEXTTEXTW** (Unicode)<br/>                                         |



 

 





