---
title: Mensaje de EM_GETSEL (Winuser. h)
description: Obtiene las posiciones de los caracteres inicial y final (en TCHARs) de la selección actual en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079312"
---
# <a name="em_getsel-message"></a>\_Mensaje GETSEL em

Obtiene las posiciones de los caracteres inicial y final (en **TCHAR** s) de la selección actual en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un puntero a un valor **DWORD** que recibe la posición inicial de la selección. Este parámetro puede ser **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un valor **DWORD** que recibe la posición del primer carácter no seleccionado después del final de la selección. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un valor basado en cero con la posición inicial de la selección en [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y la posición del primer **TCHAR** después del último **TCHAR** seleccionado en el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Si alguno de estos valores supera 65.535, el valor devuelto es-1.

Es mejor usar los valores devueltos en *wParam* e *lParam* porque son valores de 32 bits completos.

## <a name="remarks"></a>Observaciones

Si no hay ninguna selección, los valores inicial y final son la posición del símbolo de intercalación.

**Controles Rich Edit:** También puede usar el mensaje [**\_ EXGETSEL em**](em-exgetsel.md) para recuperar la misma información. **Em \_ EXGETSEL** también devuelve las posiciones de caracteres inicial y final como valores de 32 bits.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_EXGETSEL em**](em-exgetsel.md)
</dt> <dt>

[**\_SETSEL em**](em-setsel.md)
</dt> </dl>

 

