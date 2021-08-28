---
title: TLS_HANDLE
description: Representa un identificador para un Escritorio remoto de licencias.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04daf14429a5b400267e664a615739fd14e8306e987f50726cfdb341522870a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869455"
---
# <a name="tls_handle"></a>IDENTIFICADOR \_ DE TLS

Representa un identificador para un Escritorio remoto de licencias. La función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) devuelve este identificador.

> [!Note]  
> Este tipo de datos no tiene ningún archivo de encabezado asociado. Para usarlo, debe definirlo usted mismo como se muestra en este tema.

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





