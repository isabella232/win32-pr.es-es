---
description: La función DllGetMonitorObject debe ser implementada por el monitor. MCSVC llama a esta función para crear una instancia del monitor.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Función de devolución de llamada DllGetMonitorObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912841"
---
# <a name="dllgetmonitorobject-callback-function"></a>Función de devolución de llamada DllGetMonitorObject

La función **DllGetMonitorObject** debe ser implementada por el monitor. MCSVC llama a esta función para crear una instancia del monitor.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* \[ de\]
</dt> <dd>

UUID de monitores, que se muestra a continuación, tal como se define en el archivo de encabezado IMonitor. h. Si se proporciona un UUID no válido, se produce un error en la función y el monitor debe devolver E \_ nointerface.

``` syntax
IID_IMonitor
```

</dd> <dt>

*ppObj* \[ enuncia\]
</dt> <dd>

Puntero a un puntero que recibe la interfaz solicitada en *riid*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError).

Si la función no es correcta, el valor devuelto es un código de error. Cuando se devuelve un código de error, MCSVC no crea el objeto de supervisión y no se llama al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero de interfaz.

## <a name="remarks"></a>Observaciones

Se llama a la función **DllGetMonitorObject** cada vez que MCSVC intenta crear una instancia del monitor. Esta función tiene un gran similitud con la función [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) más común. La principal diferencia es que un CLSID no se pasa a **DllGetMonitorObject**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

