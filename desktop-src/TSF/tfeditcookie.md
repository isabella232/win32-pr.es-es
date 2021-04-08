---
title: TfEditCookie (msctf. h)
description: El tipo de datos TfEditCookie identifica una sesión de edición que tiene un bloqueo.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078824"
---
# <a name="tfeditcookie"></a>TfEditCookie

El tipo de datos **TfEditCookie** identifica una sesión de edición que tiene un bloqueo.


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a>Observaciones

El tipo de datos **TfEditCookie** es proporcionado por el administrador de TSF y lo usa un cliente (servicio de aplicación o texto) para identificar una sesión de edición con un bloqueo de solo lectura o de lectura y escritura en varios métodos.

Un valor **TfEditCookie** se obtiene de una de las siguientes maneras.

-   El cliente llama a [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).
-   El administrador de TSF llama al método ITfEditSession de cliente [::D oeditsession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) .
-   El administrador de TSF llama al método [ITfCompositionSink:: OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) del cliente.
-   El administrador de TSF llama al método [ITfCleanupContextSink:: OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) del cliente.
-   El administrador de TSF llama al método [ITfTextEditSink:: OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) del cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                    |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                          |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITfCleanupContextSink::OnCleanupContext**](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[**ITfCompositionSink::OnCompositionTerminated**](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[**ITfDocumentMgr:: CreateContext**](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[**ITfEditSession::D oEditSession**](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[**ITfTextEditSink::OnEndEdit**](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





