---
description: 'Función AMovieDllRegisterServer: obsoleta. Use AMovieDllRegisterServer2 en su lugar.'
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: Función AMovieDllRegisterServer (Dllsetup.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d09c566a9a97b1b755c81ca7483251a23dd0b0fed037c38d5e5a5cc06216c155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118002032"
---
# <a name="amoviedllregisterserver-function"></a>Función AMovieDllRegisterServer

Obsoleto. Use [**AMovieDllRegisterServer2 en**](amoviedllregisterserver2.md) su lugar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dllsetup.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de instalación de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




