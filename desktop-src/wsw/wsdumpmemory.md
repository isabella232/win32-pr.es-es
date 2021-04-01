---
title: Función WsDumpMemory (WebServicesDebug. h)
description: Esta función vuelca todas las asignaciones de memoria en la consola.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Servicios Web de la función WsDumpMemory para Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996866"
---
# <a name="wsdumpmemory-function"></a>WsDumpMemory función)

Esta función vuelca todas las asignaciones de memoria en la consola.

> [!Note]  
> Esta función es solo para depurar.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*error* \[ de en, opcional\]
</dt> <dd>

Un puntero a un objeto de [ \_ error de WS](ws-error.md) en el que se debe almacenar información adicional sobre el error si se produce un error en la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                             |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WebServicesDebug. h</dt> </dl> |



 

 





