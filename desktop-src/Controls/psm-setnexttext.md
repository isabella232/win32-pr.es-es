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
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167478"
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



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **PSM \_ SETNEXTTEXTW** (Unicode)<br/>                                         |



 

 





