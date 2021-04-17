---
description: Obtiene la dirección de una función de un archivo DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: _GetProcAddress_ (función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 0d717036b92e79056fd3b1bf69f1fd17784db713
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661158"
---
# <a name="_getprocaddress_-function"></a>\_GetProcAddress ( \_ función)

\[Esta función es un contenedor de la función **GetProcAddress** . Esta función puede modificarse o no estar disponible en el futuro. Las aplicaciones deben llamar a **GetProcAddress** directamente.\]

Obtiene la dirección de una función de un archivo DLL. Vea [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).

## <a name="syntax"></a>Sintaxis


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
