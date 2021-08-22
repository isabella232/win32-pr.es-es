---
description: Permite que un depurador examine la información de la tabla de funciones dinámicas.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: Función RtlGetFunctionTableListHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ff41aca0d268083132fd1a45371b0bb1ca026e5e6d693619ba1e2c2f9f2dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666735"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>Función RtlGetFunctionTableListHead

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Permite que un depurador examine la información de la tabla de funciones dinámicas.

## <a name="syntax"></a>Sintaxis


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al final de la lista de tablas de funciones.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que Windows archivo de encabezado Ntdef.h del Kit de controladores de Windows (WDK) es necesario para algunas definiciones. La biblioteca de importación asociada, Ntdll.lib, está disponible en WDK. También puede usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
