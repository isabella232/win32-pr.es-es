---
title: Función FreeFixupInfo (NapUtil. h)
description: Libera una estructura de datos FixupInfo.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- FreeFixupInfo función NAP
topic_type:
- apiref
api_name:
- FreeFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abf1fe07557ac786a9f0cb8e8e06a30408f6d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676890"
---
# <a name="freefixupinfo-function"></a>FreeFixupInfo función)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La función **FreeFixupInfo** libera una estructura de datos [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) .

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fixupInfo* \[ de\]
</dt> <dd>

Puntero a la estructura de datos [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) que se va a liberar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):

-   El autor de la llamada asigna y libera los parámetros **in** .
-   El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.
-   Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.

Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AllocFixupInfo**](allocfixupinfo-func.md)
</dt> </dl>

 

 





