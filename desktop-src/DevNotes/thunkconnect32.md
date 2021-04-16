---
description: La función ThunkConnect32 se usa en los controladores de dispositivo de 16 bits (para MS-DOS) que llaman al kernel de 32 bits.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: ThunkConnect32 función)
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
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649531"
---
# <a name="thunkconnect32-function"></a>ThunkConnect32 función)

\[Esta función se admitía por compatibilidad con versiones anteriores, pero no está presente en las versiones actuales de Windows. Los controladores de dispositivos nuevos deben ser de 32 a 64 bits y no necesitan esta función.\]

La función **ThunkConnect32** se usa en los controladores de dispositivo de 16 bits (para MS-dos) que llaman al kernel de 32 bits.

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

Siempre devuelve **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




