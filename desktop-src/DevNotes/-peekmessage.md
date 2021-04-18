---
description: Envía los mensajes enviados entrantes, comprueba la cola de mensajes de subprocesos en busca de un mensaje expuesto y recupera el mensaje (si existe alguno).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: _PeekMessage función)
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
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649587"
---
# <a name="_peekmessage-function"></a>\_PeekMessage (función)

\[Esta función es un contenedor de la función **PeekMessage** . Esta función puede modificarse o no estar disponible en el futuro. Las aplicaciones deben llamar a **PeekMessage** directamente.\]

Envía los mensajes enviados entrantes, comprueba la cola de mensajes de subprocesos en busca de un mensaje expuesto y recupera el mensaje (si existe alguno). Consulte [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).

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

 

 
