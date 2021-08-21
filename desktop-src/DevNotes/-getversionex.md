---
description: Obtiene información sobre la versión del sistema operativo.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: _GetVersionEx función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 2e3047edfaf2dabe591172dd3ca292f41aeefa90774231b417f5405e3aeb18c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956294"
---
# <a name="_getversionex-function"></a>\_Función GetVersionEx

\[Esta función es un contenedor sobre la **función GetVersionEx.** Esta función puede modificarse o no estar disponible en el futuro. Las aplicaciones deben llamar **directamente a GetVersionEx.**\]

Obtiene información sobre la versión del sistema operativo. Vea [**GetVersionEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)

## <a name="syntax"></a>Sintaxis


```C++
BOOL _GetVersionEx(
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

[**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
