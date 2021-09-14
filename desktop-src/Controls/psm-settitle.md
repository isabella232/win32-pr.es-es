---
title: PSM_SETTITLE mensaje (Prsht.h)
description: Establece el título de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetTitle.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- PSM_SETTITLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167474"
---
# <a name="psm_settitle-message"></a>Mensaje \_ SETTITLE de PSM

Establece el título de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la [**macro PropSheet \_ SetTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca que indica si se debe incluir el prefijo "Properties for" o el sufijo "Properties" (según la versión) con la cadena de título especificada. Si este valor es PSH \_ PROPTITLE, se incluye el prefijo o sufijo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer que contiene la cadena de título. Si el [**VALOR HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de este parámetro es **NULL,** la hoja de propiedades carga el recurso de cadena especificado en [**loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En un asistente de Aero, este mensaje se puede usar para cambiar dinámicamente el título de una página interior. por ejemplo, al controlar la [notificación \_ SETACTIVE de PSN.](psn-setactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **PSM \_ SETTITLEW** (Unicode) y **PSM \_ SETTITLEA** (ANSI)<br/>              |



 

