---
description: Envía el mensaje especificado a una ventana o ventanas.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: _SendMessage función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: bdd8a072970d8e6fb5e9af082f6f220531539a1c0061a7688d48be30dd659a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572575"
---
# <a name="_sendmessage-function"></a>\_Función SendMessage

\[Esta función es un contenedor sobre la **función SendMessage.** Esta función puede modificarse o no estar disponible en el futuro. Las aplicaciones deben llamar **directamente a SendMessage.**\]

Envía el mensaje especificado a una ventana o ventanas. Vea [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).

## <a name="syntax"></a>Sintaxis


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
