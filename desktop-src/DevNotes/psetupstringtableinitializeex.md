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
ms.openlocfilehash: 189bb94b70366ad66f0fe4dd4c4c9d5884e762cf20638f7c3ae2dc9b587f15ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538475"
---
# <a name="psetupstringtableinitializeex-function"></a>Función pSetupStringTableInitializeEx

\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]

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



 

 
