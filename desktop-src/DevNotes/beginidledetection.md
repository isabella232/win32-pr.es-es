---
description: Comienza la supervisión de inactividad.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: BeginIdleDetection función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671177"
---
# <a name="beginidledetection-function"></a>BeginIdleDetection función)

\[Esta función no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use la función **GetLastInputInfo** .\]

Comienza la supervisión de inactividad.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pfnCallback* 
</dt> <dd>

Función a la que se llama cuando cambia el estado de inactividad. Esta devolución de llamada se define de la siguiente manera:

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

*dwIdleMin* 
</dt> <dd>

El número de minutos de inactividad antes de que se realice la llamada a la función de devolución de llamada.

</dd> <dt>

*dwReserved* 
</dt> <dd>

Este parámetro debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si la función se ejecuta correctamente; de lo contrario, devuelve un código de error. Por ejemplo, si *dwReserved* es distinto de 0, se devuelven los **\_ \_ datos no válidos** .

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Esta función no se exporta por nombre; Especifique el ordinal 3 al llamar a **GetProcAddress**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
