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
ms.openlocfilehash: 782d5ebf3e7fe0850b89d9f52f0dc5c406dbd41c9bdad694b41b8ae9ea4c8b0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985455"
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

## <a name="remarks"></a>Comentarios

En un asistente de Aero, este mensaje se puede usar para cambiar dinámicamente el título de una página interior; por ejemplo, al controlar la [notificación \_ SETACTIVE de PSN.](psn-setactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **PSM \_ SETTITLEW** (Unicode) y **PSM \_ SETTITLEA** (ANSI)<br/>              |



 

