---
description: La función AMovieDllRegisterServer2 registra y anula el registro de filtros.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: Función AMovieDllRegisterServer2 (Dllsetup. h)
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
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661117"
---
# <a name="amoviedllregisterserver2-function"></a>AMovieDllRegisterServer2 función)

La función **AMovieDllRegisterServer2** registra y anula el registro de filtros.

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

**True** indica que se registra el filtro; **false** indica que se anula el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Utilice esta función para configurar los filtros. Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dllsetup. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de instalación de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




