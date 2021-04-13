---
description: Se produce cuando se activa una aplicación de la tienda Windows.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Evento ICoreApplicationView:: Activated (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275412"
---
# <a name="icoreapplicationviewactivated-event"></a>Evento ICoreApplicationView:: Activated

Se produce cuando se activa una aplicación de la tienda Windows.

## <a name="syntax"></a>Sintaxis


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*controlador* \[ de de\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

No llame al método [**Exit**](/previous-versions//hh438368(v=vs.85)) desde dentro del *controlador*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                               |
| Encabezado<br/>                   | <dl> <dt>Windows. ApplicationModel. Core. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. Core. idl</dt> </dl> |



 

 
