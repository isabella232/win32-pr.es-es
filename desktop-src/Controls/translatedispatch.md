---
title: Función de devolución de llamada TranslateDispatch
description: Lo usa el cliente de la función DoReaderMode para interceptar y controlar explícitamente los mensajes de Windows destinados al área de desplazamiento de la ventana de modo lector. Se trata de una función de devolución de llamada definida por la aplicación.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- TranslateDispatch (función de devolución de llamada) controles de Windows
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996281"
---
# <a name="translatedispatch-callback-function"></a>Función de devolución de llamada TranslateDispatch

\[*TranslateDispatch* está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Lo usa el cliente de la función [**DoReaderMode**](doreadermode.md) para interceptar y controlar explícitamente los mensajes de Windows destinados al área de desplazamiento de la ventana de modo lector. Se trata de una función de devolución de llamada definida por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpmsg* \[ de\]
</dt> <dd>

Tipo: **const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \** _

Puntero a una estructura [_ *MSG* *](/windows/win32/api/winuser/ns-winuser-msg) que contiene el mensaje interceptado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** si esta función controla el mensaje; en caso contrario, **false**. Si es **false**, el mensaje se controla mediante la implementación del modo de lectura predeterminada. Esa implementación controla el movimiento y los botones del mouse, así como las pulsaciones de teclas.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se describe una implementación de esta función.


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, \[ solo aplicaciones de escritorio de Windows Vista\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>          |



 

