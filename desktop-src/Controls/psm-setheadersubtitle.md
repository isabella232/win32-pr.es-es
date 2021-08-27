---
title: PSM_SETHEADERSUBTITLE mensaje (Prsht.h)
description: Establece el texto del subtítulo para el encabezado de la página interior de un asistente. Puede enviar este mensaje explícitamente o usar la macro PropSheet \_ SetHeaderSubTitle.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- PSM_SETHEADERSUBTITLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e030b75a933ba7f647f8b3dffa5e45637999d45f3299f8280fd1db3afb9857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088505"
---
# <a name="psm_setheadersubtitle-message"></a>Mensaje \_ SETHEADERSUBTITLE de PSM

Establece el texto del subtítulo para el encabezado de la página interior de un asistente. Puede enviar este mensaje explícitamente o usar la macro [**PropSheet \_ SetHeaderSubTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle)

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

## <a name="remarks"></a>Comentarios

Si especifica la página actual, se volverá a dibujar inmediatamente para mostrar el nuevo subtítulo.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl>      |
| Nombres Unicode y ANSI<br/>   | **PSM \_ SETHEADERSUBTITLEW** (Unicode) y **PSM \_ SETHEADERSUBTITLEA** (ANSI)<br/> |



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

 

 





