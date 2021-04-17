---
title: Mensaje de PSM_SETHEADERTITLE (Prsht. h)
description: Establece el texto del título para el encabezado de la página interior de un asistente. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet SetHeaderTitle.
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- PSM_SETHEADERTITLE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656470"
---
# <a name="psm_setheadertitle-message"></a>Mensaje de PSM \_ SETHEADERTITLE

Establece el texto del título para el encabezado de la página interior de un asistente. Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
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

 

 





