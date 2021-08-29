---
title: Función WsDumpMemory (WebServicesDebug.h)
description: Esta función vuelca todas las asignaciones de memoria en la consola.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Servicios web de la función WsDumpMemory para Windows
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
ms.openlocfilehash: b92941603b78c25db06415fec42524d978a90953d0c15eaea191a8874e6b34fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770895"
---
# <a name="wsdumpmemory-function"></a>Función WsDumpMemory

Esta función vuelca todas las asignaciones de memoria en la consola.

> [!Note]  
> Esta función es para DEBUG ONLY.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*error* \[ in, opcional\]
</dt> <dd>

Puntero a un [objeto ERROR de WS \_ ](ws-error.md) donde se debe almacenar información adicional sobre el error si se produce un error en la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                                |
| Header<br/>                   | <dl> <dt>WebServicesDebug.h</dt> </dl> |



 

 





