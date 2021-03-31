---
title: Mensaje EM_GETTEXTEX (RichEdit. h)
description: Obtiene el texto de un control Rich Edit.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- EM_GETTEXTEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490372"
---
# <a name="em_gettextex-message"></a>\_Mensaje GETTEXTEX em

Obtiene el texto de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una estructura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) , que indica cómo traducir el texto antes de colocarlo en el búfer de salida.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer para recibir el texto. El miembro **CB** de la estructura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) especifica el tamaño de este búfer, en bytes. Use el [**mensaje \_ GETTEXTLENGTHEX em**](em-gettextlengthex.md) para obtener el tamaño necesario del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de elementos **TCHAR** copiados en el búfer de salida, incluido el terminador null.

## <a name="remarks"></a>Observaciones

Si el tamaño del búfer de salida es menor que el tamaño del texto del control, el control de edición copiará el texto desde el principio y lo colocará en el búfer hasta que el búfer esté lleno. Un carácter nulo de terminación se seguirá colocando al final del búfer.

Si se solicita texto ANSI, **em \_ GETTEXTEX** utiliza la función [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para convertir los caracteres Unicode a ANSI. Permite pasar de Unicode a ANSI mediante una página de códigos determinada. La estructura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) contiene miembros (**lpDefaultChar** y **lpUsedDefChar**) que se usan en la traducción de Unicode a ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_SETTEXTEX em**](em-settextex.md)
</dt> <dt>

[**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[**SETTEXT de WM \_**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

