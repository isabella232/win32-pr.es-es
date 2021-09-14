---
description: La estructura PROTOCOLTABLE contiene una lista de protocolos.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Estructura PROTOCOLTABLE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362130"
---
# <a name="protocoltable-structure"></a>PROTOCOLTABLE (estructura)

La **estructura PROTOCOLTABLE** contiene una lista de protocolos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**nProtocols**
</dt> <dd>

Número de protocolos habilitados.

</dd> <dt>

**hProtocol**
</dt> <dd>

Matriz de identificadores para protocolos habilitados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




