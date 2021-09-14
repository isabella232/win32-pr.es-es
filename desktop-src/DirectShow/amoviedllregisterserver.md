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
ms.openlocfilehash: 81b6e73b1988d3eb97abdf9a5d2415ecbd62d8c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162325"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones de instalación de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




