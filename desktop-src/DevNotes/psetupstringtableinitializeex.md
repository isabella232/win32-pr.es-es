---
description: 'Función pSetupStringTableInitializeEx: inicializa una tabla de cadenas.'
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: Función pSetupStringTableInitializeEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 78ee96e7e366fdff821e8202300ff28de0a14af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096653"
---
# <a name="psetupstringtableinitializeex-function"></a>Función pSetupStringTableInitializeEx

\[Esta función no está disponible en Windows Vista o Windows Server 2008.\]

Inicializa una tabla de cadenas.

## <a name="syntax"></a>Sintaxis


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ExtraDataSize* \[ En\]
</dt> <dd>

Tamaño del objeto de datos adicional.

</dd> <dt>

*Reservado* \[ En\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
