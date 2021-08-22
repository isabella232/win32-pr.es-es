---
description: La función GetDllVersion recupera el número de versión de Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: Función GetDllVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 14f2da8c6f8c786042c2abd5f41e02bdfab6f33d9b8aa42a5b5f90a6c4357103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390715"
---
# <a name="getdllversion-function"></a>Función GetDllVersion

\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento. \]

La **función GetDllVersion** recupera el número de versión de Cabinet.dll.

## <a name="syntax"></a>Sintaxis


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Número de versión del archivo (vea [Recurso VERSIONINFO](../menurc/versioninfo-resource.md)).

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 
