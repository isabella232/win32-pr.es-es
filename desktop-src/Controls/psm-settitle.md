---
title: Mensaje de PSM_SETTITLE (Prsht. h)
description: Establece el título de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetTitle.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- PSM_SETTITLE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995971"
---
# <a name="psm_settitle-message"></a>Mensaje de PSM \_ SETTITLE

Establece el título de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca que indica si se deben incluir el prefijo "propiedades para" o el sufijo "propiedades" (dependiendo de la versión) con la cadena de título especificada. Si este valor es PSH \_ PROPTITLE, se incluye el prefijo o el sufijo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer que contiene la cadena de título. Si el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de este parámetro es **null**, la hoja de propiedades carga el recurso de cadena especificado en [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En un asistente de Aero, este mensaje se puede usar para cambiar dinámicamente el título de una página interior. por ejemplo, al controlar la notificación de [ \_ SETACTIVE de PSN](psn-setactive.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **PSM \_ SETTITLEW** (Unicode) y **PSM \_ SETTITLEA** (ANSI)<br/>              |



 

