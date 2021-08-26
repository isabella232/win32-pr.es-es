---
description: Comienza a supervisar la inactividad.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: Función BeginIdleDetection
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
ms.openlocfilehash: 1bbb27114177a6f64f471b0122832bc09180988019bc23a63343920eb76221f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002325"
---
# <a name="beginidledetection-function"></a>Función BeginIdleDetection

\[Esta función no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use **la función GetLastInputInfo.**\]

Comienza a supervisar la inactividad.

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

Número de minutos de inactividad antes de realizar la llamada a la función de devolución de llamada.

</dd> <dt>

*dwReserved* 
</dt> <dd>

Este parámetro debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si la función se realiza correctamente; de lo contrario, devuelve un código de error. Por ejemplo, si *dwReserved es distinto* de 0, **se devuelve ERROR INVALID \_ \_ DATA.**

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Esta función no se exporta por nombre; especifique el ordinal 3 al llamar a **GetProcAddress**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
