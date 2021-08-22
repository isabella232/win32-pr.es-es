---
description: Inicializa el seguimiento.
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: Función InitAsyncTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: d64fcf9f787587165c12e675d79cfca641b0ab5086a5cce6b13029da46def974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956304"
---
# <a name="initasynctrace-function"></a>Función InitAsyncTrace

Inicializa el seguimiento.

## <a name="syntax"></a>Sintaxis


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** la función se realiza correctamente; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

Exstrace.dll es un componente opcional que se instala con el Protocolo simple de transferencia de correo (SMTP) y el Protocolo de transferencia de noticias de red (NNTP).

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
