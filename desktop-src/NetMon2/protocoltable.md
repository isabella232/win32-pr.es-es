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
ms.openlocfilehash: a30d890fa5b6dcbbca1797a53722b97b2109cc9943ce07260c7f47514cfeb7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036985"
---
# <a name="protocoltable-structure"></a>Estructura PROTOCOLTABLE

La **estructura PROTOCOLTABLE** contiene una lista de protocolos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a>Miembros

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



 

 




