---
description: La función GetDllVersion recupera el número de versión de Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: GetDllVersion función)
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
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660408"
---
# <a name="getdllversion-function"></a>GetDllVersion función)

\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento. \]

La función **GetDllVersion** recupera el número de versión de Cabinet.dll.

## <a name="syntax"></a>Sintaxis


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El número de versión del archivo (consulte el [recurso versionInfo](../menurc/versioninfo-resource.md)).

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 
