---
title: TfClientId (Msctf.h)
description: El tipo de datos TfClientId se usa para identificar el cliente.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347784de9014ee300bf6931e4d005c366a0cc9b67f57f82515010ece5b68551e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950422"
---
# <a name="tfclientid"></a>TfClientId

El **tipo de datos TfClientId** se usa para identificar el cliente.


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a>Comentarios

En TSF, las aplicaciones y los servicios de texto se conocen generalmente como clientes. Cada cliente recibe un identificador único que usa para identificarse a sí mismo al llamar a varios métodos de administrador de TSF. Este identificador es del tipo **TfClientId.**

El **tipo de datos TfClientId** lo proporciona el administrador de TSF. Una aplicación obtiene un valor **TfClientId** cuando llama a [ITfThreadMgr::Activate.](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) El valor TfClientId de un servicio de texto se pasa al [método ITfTextInputProcessor::Activate.](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) Cualquier objeto que no se ajuste a las categorías anteriores puede obtener un identificador de cliente llamando a [ITfClientId::GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                    |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                          |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITfClientId::GetClientId**](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[**ITfTextInputProcessor::Activate**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[**ITfThreadMgr::Activate**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





