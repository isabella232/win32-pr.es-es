---
description: Permite que un depurador examine la información de la tabla de funciones dinámicas.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: RtlGetFunctionTableListHead función)
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
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671362"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>RtlGetFunctionTableListHead función)

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Permite que un depurador examine la información de la tabla de funciones dinámicas.

## <a name="syntax"></a>Sintaxis


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al encabezado de la lista de la tabla de funciones.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que el archivo de encabezado de Windows Driver Kit (WDK) Ntdef. h es necesario para algunas definiciones. La biblioteca de importación asociada, ntdll. lib, está disponible en el WDK. También puede utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
