---
title: Mensaje de EM_GETIMESTATUS (Winuser. h)
description: Obtiene un conjunto de marcas de estado que indican cómo interactúa el control de edición con el editor de métodos de entrada (IME).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- EM_GETIMESTATUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150766"
---
# <a name="em_getimestatus-message"></a>\_Mensaje GETIMESTATUS em

Obtiene un conjunto de marcas de estado que indican cómo interactúa el control de edición con el editor de métodos de entrada (IME).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de estado que se va a recuperar. Este parámetro puede ser el valor siguiente.



| Value                                                                                                                                                                                       | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Establece el comportamiento para controlar la cadena de composición.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Datos específicos del tipo de estado que se va a recuperar. Con el valor de **EMSIS \_ COMPOSITIONSTRING** para *status*, este valor devuelto es uno o varios de los valores siguientes.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>         | Si se establece esta marca, el control de edición enlaza el mensaje de [**\_ \_ composición del IME de WM**](/windows/desktop/Intl/wm-ime-composition) con *fFlags* establecido en los conjuntos de resultados de GC \_ y devuelve la cadena de resultado inmediatamente. Si no se establece esta marca, el control de edición pasa el mensaje de **\_ \_ composición del IME de WM** al procedimiento de ventana predeterminado y procesa la cadena de resultado del mensaje de [**\_ carácter de WM**](/windows/desktop/inputdev/wm-char) ; éste es el comportamiento predeterminado del control de edición.<br/> |
| <dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>     | Si se establece esta marca, el control de edición cancela la cadena de composición cuando recibe el mensaje de [**\_ SETFOCUS de WM**](/windows/desktop/inputdev/wm-setfocus) . Si no se establece esta marca, el control de edición no cancela la cadena de composición; Éste es el comportamiento predeterminado del control de edición.<br/>                                                                                                                                                                       |
| <dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Si se establece esta marca, el control de edición completa la cadena de composición al recibir el mensaje de [**\_ KILLFOCUS de WM**](/windows/desktop/inputdev/wm-killfocus) . Si no se establece esta marca, el control de edición no completa la cadena de composición; Éste es el comportamiento predeterminado del control de edición.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

**Edición enriquecida:** No se admite el mensaje **\_ GETIMESTATUS em** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETIMESTATUS em**](em-setimestatus.md)
</dt> </dl>

 

