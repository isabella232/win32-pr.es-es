---
title: Función FreeSoHAttributeValue (NapUtil.h)
description: Libera una estructura de datos SoHAttributeValue.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- Función NAP de FreeSoHAttributeValue
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877a333c7eb43c3921c7727bcc15a958bdcd2565fabe4636a67868f3a27bf473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940409"
---
# <a name="freesohattributevalue-function"></a>Función FreeSoHAttributeValue

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **función FreeSoHAttributeValue** libera una estructura de datos [**SoHAttributeValue.**](sohattributevalue-union.md)

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* \[ En\]
</dt> <dd>

Valor [**SoHAttributeType**](sohattributetype-enum.md) que especifica el tipo de valor del atributo SoH que se liberará.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

Puntero a [**SoHAttributeValue que**](sohattributevalue-union.md) se liberará.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Todas las interfaces COM compatibles con el sistema NAP usan reglas de administración de memoria COM estándar y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):

-   **El** autor de la llamada asigna y libera los parámetros de .
-   **El** destinatario asigna los parámetros out y el autor de la llamada lo libera **mediante CoTaskMem**.
-   **El autor de** la llamada asigna los parámetros de entrada y salida, los libera y reasigna el destinatario y, en última instancia, los libera el autor de la llamada, mediante **CoTaskMem**.

Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 





