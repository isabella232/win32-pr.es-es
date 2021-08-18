---
description: Se produce cuando se activa una Windows store.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: Evento ICoreApplicationView::Activated (Windows. ApplicationModel.Core.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e736d0fb5403fe76d6d402c261e6b7e5336dfc096d8c39d7b3300b93ab1332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560999"
---
# <a name="icoreapplicationviewactivated-event"></a>Evento ICoreApplicationView::Activated

Se produce cuando se activa una Windows store.

## <a name="syntax"></a>Sintaxis


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*controlador* \[ En\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

No llame al método [**Exit**](/previous-versions//hh438368(v=vs.85)) desde dentro del *controlador*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                               |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel.Core.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.Core.idl</dt> </dl> |



 

 
