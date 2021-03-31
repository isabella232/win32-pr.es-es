---
title: TLS_HANDLE
description: Representa un identificador de un servidor de licencias de Escritorio remoto.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801687"
---
# <a name="tls_handle"></a>identificador de TLS \_

Representa un identificador de un servidor de licencias de Escritorio remoto. La función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) devuelve este identificador.

> [!Note]  
> Este tipo de datos no tiene ningún archivo de encabezado asociado. Para usarlo, debe definirlo como se muestra en este tema.

 


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

 

 





