---
description: La función LoadStringAddr transforma una cadena (como &\# 0034; 157.54.32.45&\# 0034;) y crea una dirección DWORD.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: Función LoadStringAddr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677414"
---
# <a name="loadstringaddr-function"></a>LoadStringAddr función)

La función **LoadStringAddr** transforma una cadena (por ejemplo, "157.54.32.45") y crea una dirección **DWORD** .

## <a name="syntax"></a>Sintaxis


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAddress* 
</dt> <dd>

Puntero a un **valor DWORD**.

</dd> <dt>

*str* 
</dt> <dd>

Puntero a una cadena de caracteres con la representación x. x. x. x de una dirección IP (por ejemplo, 127.0.0.1).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (se encontró el nombre de la dirección); el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




