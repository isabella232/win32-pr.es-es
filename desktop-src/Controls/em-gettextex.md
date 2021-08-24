---
title: EM_GETTEXTEX mensaje (Richedit.h)
description: Obtiene el texto de un control de edición enriquecido.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- EM_GETTEXTEX controles de Windows mensaje
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
ms.openlocfilehash: 1b116ea27aaff217f949fbd6286a7d8278075486f14f9b9fcec21cf49af2edfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006607"
---
# <a name="em_gettextex-message"></a>Mensaje \_ GETTEXTEX EM

Obtiene el texto de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una [**estructura GETTEXTEX,**](/windows/desktop/api/Richedit/ns-richedit-gettextex) que indica cómo traducir el texto antes de colocarlo en el búfer de salida.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer para recibir el texto. El miembro **cb** de la estructura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) especifica el tamaño de este búfer, en bytes. Use el [**mensaje EM \_ GETTEXTLENGTHEX**](em-gettextlengthex.md) para obtener el tamaño necesario del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de **TCHAR** copiados en el búfer de salida, incluido el terminador nulo.

## <a name="remarks"></a>Comentarios

Si el tamaño del búfer de salida es menor que el tamaño del texto del control , el control de edición copiará texto desde su principio y lo colocará en el búfer hasta que el búfer esté lleno. Se seguirá colocando un carácter nulo de terminación al final del búfer.

Si se solicita texto ANSI, **EM \_ GETTEXTEX** usa la función [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para traducir los caracteres Unicode a ANSI. Permite pasar de Unicode a ANSI mediante una página de códigos determinada. La [**estructura GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) contiene miembros (**lpDefaultChar** y **lpUsedDefChar**) que se usan en la traducción de Unicode a ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETTEXTEX**](em-settextex.md)
</dt> <dt>

[**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

