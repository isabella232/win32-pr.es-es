---
description: La función AMovieDllRegisterServer2 registra y anula el registro de los filtros.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: Función AMovieDllRegisterServer2 (Dllsetup.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c47b861a47498cc29d80061c6c2da1ffc44e40b7446588cf7c3376e5ed18e837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001988"
---
# <a name="amoviedllregisterserver2-function"></a>Función AMovieDllRegisterServer2

La **función AMovieDllRegisterServer2** registra y anula el registro de los filtros.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bRegister* 
</dt> <dd>

**TRUE** indica registrar el filtro, **FALSE** indica anular el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Use esta función para configurar los filtros. Para obtener más información, [vea How to Register DirectShow Filters](how-to-register-directshow-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dllsetup.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de instalación de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




