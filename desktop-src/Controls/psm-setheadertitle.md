---
title: PSM_SETHEADERTITLE mensaje (Prsht.h)
description: Establece el texto del título del encabezado de la página interior de un asistente. Puede enviar este mensaje explícitamente o usar la macro PropSheet \_ SetHeaderTitle.
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- PSM_SETHEADERTITLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167482"
---
# <a name="psm_setheadertitle-message"></a>Mensaje \_ SETHEADERTITLE de PSM

Establece el texto del título del encabezado de la página interior de un asistente. Puede enviar este mensaje explícitamente o usar la macro [**PropSheet \_ SetHeaderTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la página del asistente.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo subtítulo de encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si especifica la página actual, se volverá a dibujar inmediatamente para mostrar el nuevo título.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **PSM \_ SETHEADERTITLEW** (Unicode) y **PSM \_ SETHEADERTITLEA** (ANSI)<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**PSM \_ HWNDTOINDEX**](psm-hwndtoindex.md)
</dt> <dt>

[**PSM \_ IDTOINDEX**](psm-idtoindex.md)
</dt> <dt>

[**PSM \_ PAGETOINDEX**](psm-pagetoindex.md)
</dt> </dl>

 

 





