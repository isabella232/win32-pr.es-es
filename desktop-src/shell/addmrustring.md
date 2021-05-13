---
description: Agrega una cadena a la parte superior de la lista usada más recientemente (MRU).
title: Función AddMRUStringW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: b62e23cd0604273559e36e561970dd62f117c11d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841196"
---
# <a name="addmrustringw-function"></a>Función AddMRUStringW

\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows. \]

Agrega una cadena a la parte superior de la lista de mru usada más recientemente.

## <a name="syntax"></a>Sintaxis


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMRU* \[ En\]
</dt> <dd>

Tipo: **HANDLE**

Identificador de la lista de MRU.

</dd> <dt>

*szString* \[ En\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a los datos. Puede ser una cadena o, si se creó la lista de MRU con la **marca \_ BINARY de MRU,** datos binarios. En el caso de los datos binarios, el primer **DWORD** indica su tamaño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Devuelve un valor no negativo si se realiza correctamente; de lo contrario, -1.

## <a name="remarks"></a>Observaciones

Esta función no se incluye en un encabezado o biblioteca públicos. Se puede acceder a él a través de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraerse de comctl32.dll por su ordinal, que es 401 **para AddMRUStringW**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5.0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **AddMRUStringW** (Unicode)<br/>                                                                         |



 

