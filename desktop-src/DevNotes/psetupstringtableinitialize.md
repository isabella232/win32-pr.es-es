---
description: Inicializa una tabla de cadenas.
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: pSetupStringTableInitialize función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 67436dd0befbef01c5b6f55a68082b9e23870592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670515"
---
# <a name="psetupstringtableinitialize-function"></a>pSetupStringTableInitialize función)

\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]

Inicializa una tabla de cadenas.

## <a name="syntax"></a>Sintaxis


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
