---
description: 'Función pSetupStringTableInitialize: inicializa una tabla de cadenas.'
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: función pSetupStringTableInitialize
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
ms.openlocfilehash: 79638f9f1f80f4b9b3d54a33c7e94234174ffb19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089204"
---
# <a name="psetupstringtableinitialize-function"></a>función pSetupStringTableInitialize

\[Esta función no está disponible en Windows Vista o Windows Server 2008.\]

Inicializa una tabla de cadenas.

## <a name="syntax"></a>Sintaxis


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
