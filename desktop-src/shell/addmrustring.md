---
description: Agrega una cadena a la parte superior de la lista de elementos usados más recientemente (MRU).
title: AddMRUStringW función)
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
ms.openlocfilehash: 0d0d65187105f4ad844b349c6ac60b030c464716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082008"
---
# <a name="addmrustringw-function"></a>AddMRUStringW función)

\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows. \]

Agrega una cadena a la parte superior de la lista de elementos usados más recientemente (MRU).

## <a name="syntax"></a>Sintaxis


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMRU* \[ de\]
</dt> <dd>

Tipo: **Handle**

Identificador de la lista MRU.

</dd> <dt>

*szString* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a los datos. Puede ser una cadena o bien, si la lista MRU se creó con la marca **\_ binaria de MRU** , datos binarios. En el caso de los datos binarios, el primer **valor DWORD** indica su tamaño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Devuelve un valor no negativo si es correcto; de lo contrario,-1.

## <a name="remarks"></a>Observaciones

Esta función no está incluida en un encabezado público o una biblioteca. Se puede tener acceso a ella a través de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraer de comctl32.dll por su ordinal, que es 401 para **AddMRUStringW**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5,0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **AddMRUStringW** (Unicode)<br/>                                                                         |



 

