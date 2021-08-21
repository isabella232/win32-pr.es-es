---
description: 'Constructor CBaseControlWindow.CBaseControlWindow: método constructor.'
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Constructor CBaseControlWindow.CBaseControlWindow (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4944d121c4fe99ee36c893a4d51ca0cd72344dfa47dde17629f5ca2a1ce3fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660770"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a>Constructor CBaseControlWindow.CBaseControlWindow

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFilter* 
</dt> <dd>

Puntero al objeto de filtro de medios propietario.

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

Puntero a la sección crítica que se usará para el bloqueo.

</dd> <dt>

*pName* 
</dt> <dd>

Puntero a la descripción del objeto.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero a la **interfaz IUnknown de control,** si el objeto forma parte de un agregado; de lo contrario, debe ser **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un valor HRESULT que indica el éxito o error del método constructor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




