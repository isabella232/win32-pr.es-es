---
description: Se envía a una aplicación que ha iniciado una tarjeta de entrenamiento con Windows Ayuda.
title: WM_TCARD mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85435c5674ad6a2ac4e05edaa5d450dc61de9eac6dae05d3b19662aec91a61f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856990"
---
# <a name="wm_tcard-message"></a>Mensaje \_ de TCARD de WM

Se envía a una aplicación que ha iniciado una tarjeta de entrenamiento con Windows Ayuda. El mensaje informa a la aplicación cuando el usuario hace clic en un botón que se puede crear. Una aplicación inicia una tarjeta de entrenamiento especificando el comando \_ HELP TCARD en una llamada a la [**función WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*idAction* 
</dt> <dd>

Valor que indica la acción que ha realizado el usuario. Puede ser uno de los siguientes valores.

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span id="IDABORT"></span><span id="idabort"></span>**IDABORT**


</dt> <dd>

El usuario hizo clic en un botón **Anular que se puede** crear.

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**


</dt> <dd>

El usuario hizo clic en un botón **Cancelar que se puede** crear.

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**


</dt> <dd>

El usuario cerró la tarjeta de entrenamiento.

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**


</dt> <dd>

El usuario hizo clic en un elemento Windows **botón Ayuda.**

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**


</dt> <dd>

El usuario hizo clic en un botón Omitir que **se puede** crear.

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span id="IDOK"></span><span id="idok"></span>**IDOK**


</dt> <dd>

El usuario hizo clic en un botón **Aceptar que se puede** crear.

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span id="IDNO"></span><span id="idno"></span>**Idno**


</dt> <dd>

El usuario hizo clic en un botón No que **se puede** crear.

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**


</dt> <dd>

El usuario hizo clic en un botón **Reintentar** que se puede crear.

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**DATOS \_ DE LA TARJETA DE \_ AYUDA**


</dt> <dd>

El usuario hizo clic en un botón que se puede crear. El *parámetro dwActionData* contiene un entero largo especificado por el autor de la Ayuda.

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**AYUDA \_ PARA TARJETAR \_ A OTRO AUTOR DE LA \_ LLAMADA**


</dt> <dd>

Otra aplicación ha solicitado tarjetas de entrenamiento.

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span id="IDYES"></span><span id="idyes"></span>**IDYES**


</dt> <dd>

El usuario hizo clic en un botón Sí que **se puede** crear.

</dd> </dl> </dd> <dt>

*dwActionData* 
</dt> <dd>

Si *idAction* especifica HELP TCARD DATA, el autor de la Ayuda especifica este \_ \_ parámetro.  De lo contrario, este parámetro es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto; use cero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

 




