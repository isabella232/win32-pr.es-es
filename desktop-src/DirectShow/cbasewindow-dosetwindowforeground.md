---
description: El método DoSetWindowForeground pone la ventana en primer plano.
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: Método CBaseWindow.DoSetWindowForeground (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f0d0dd99f5e2c5e5afffb78066a9380c56f744a4ba54b64bf987df15ea58862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658024"
---
# <a name="cbasewindowdosetwindowforeground-method"></a>CBaseWindow.DoSetWindowForeground (método)

El `DoSetWindowForeground` método pone la ventana en primer plano.

## <a name="syntax"></a>Sintaxis


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bFocus* 
</dt> <dd>

Valor booleano que especifica si se debe dar el foco a la ventana. Si el valor es **TRUE,** la ventana obtiene el foco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




