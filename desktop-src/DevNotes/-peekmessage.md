---
description: Envía los mensajes enviados entrantes, comprueba la cola de mensajes del subproceso en busca de un mensaje publicado y recupera el mensaje (si existe alguno).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: _PeekMessage función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 2a2fbfcf1903fcafba77227a6b2b9f51b9c6a45ef2e8a20f7482db1f3ec2a7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538895"
---
# <a name="_peekmessage-function"></a>\_Función PeekMessage

\[Esta función es un contenedor sobre la **función PeekMessage.** Esta función puede modificarse o no estar disponible en el futuro. Las aplicaciones deben llamar **directamente a PeekMessage.**\]

Envía los mensajes enviados entrantes, comprueba la cola de mensajes del subproceso en busca de un mensaje publicado y recupera el mensaje (si existe alguno). Vea [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).

## <a name="syntax"></a>Sintaxis


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
