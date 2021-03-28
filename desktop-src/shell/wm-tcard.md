---
description: Se envía a una aplicación que ha iniciado una tarjeta de aprendizaje con la ayuda de Windows.
title: Mensaje de WM_TCARD (Winuser. h)
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
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276734"
---
# <a name="wm_tcard-message"></a>Mensaje de TCARD de WM \_

Se envía a una aplicación que ha iniciado una tarjeta de aprendizaje con la ayuda de Windows. El mensaje informa a la aplicación cuando el usuario hace clic en un botón que se pudo crear. Una aplicación inicia una tarjeta de entrenamiento especificando el comando HELP \_ TCARD en una llamada a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*idAction* 
</dt> <dd>

Valor que indica la acción que ha realizado el usuario. Puede ser uno de los valores siguientes.

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span id="IDABORT"></span><span id="idabort"></span>**IDABORT**


</dt> <dd>

El usuario hizo clic en un botón de **anulación** que se pudo crear.

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**


</dt> <dd>

El usuario hizo clic en un botón **Cancelar** que se pudo crear.

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**


</dt> <dd>

El usuario cerró la tarjeta de entrenamiento.

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**


</dt> <dd>

El usuario hizo clic en un botón **ayuda** de Windows autorizado.

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**


</dt> <dd>

El usuario hizo clic en un botón para **omitir** la creación.

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span id="IDOK"></span><span id="idok"></span>**IDOK**


</dt> <dd>

El usuario hizo clic en un botón **Aceptar** que se pudo crear.

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span id="IDNO"></span><span id="idno"></span>**IDNO**


</dt> <dd>

El usuario hizo clic en un botón **no** autorizado.

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**


</dt> <dd>

El usuario hizo clic en un botón de **reintento** que se pudo crear.

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**\_datos de TCARD de ayuda \_**


</dt> <dd>

El usuario hizo clic en un botón que se pudo crear. El parámetro *dwActionData* contiene un entero largo especificado por el autor de la ayuda.

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**AYUDA \_ TCARD \_ otro \_ llamador**


</dt> <dd>

Otra aplicación ha solicitado tarjetas de entrenamiento.

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span id="IDYES"></span><span id="idyes"></span>**IDYES**


</dt> <dd>

El usuario hizo clic en un botón **sí** que se pudo crear.

</dd> </dl> </dd> <dt>

*dwActionData* 
</dt> <dd>

Si *idAction* especifica \_ \_ los datos de TCARD de ayuda, este parámetro es un **valor largo** especificado por el autor de la ayuda. De lo contrario, este parámetro es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto; Use cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

 




