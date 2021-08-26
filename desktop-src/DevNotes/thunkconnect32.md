---
description: Los controladores de dispositivo de 16 bits (para MS-DOS) que llaman al kernel de 32 bits usan la función ThunkConnect32.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: Función ThunkConnect32
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3f754d4c0e88ee860d112a6fb99d15c2690af0014951e77425d425b65ad16e39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929115"
---
# <a name="thunkconnect32-function"></a>Función ThunkConnect32

\[Esta función se admite por compatibilidad con versiones anteriores, pero no está presente en las versiones actuales de Windows. Los nuevos controladores de dispositivo deben ser de 32 o 64 bits y no necesitan esta función.\]

Los controladores de dispositivo de 16 bits (para MS-DOS) que llaman al kernel de 32 bits usan la función **ThunkConnect32.**

## <a name="syntax"></a>Sintaxis


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpThunkData32* 
</dt> <dd>

ignorado.

</dd> <dt>

*pszThunkData16Name* 
</dt> <dd>

ignorado.

</dd> <dt>

*pszDll16* 
</dt> <dd>

ignorado.

</dd> <dt>

*pszDll32* 
</dt> <dd>

ignorado.

</dd> <dt>

*hInstance* 
</dt> <dd>

ignorado.

</dd> <dt>

*dwReason* 
</dt> <dd>

ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




