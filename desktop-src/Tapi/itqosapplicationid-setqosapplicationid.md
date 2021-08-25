---
description: El método SetQOSApplicationID establece el identificador de QOS para la aplicación.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: Método ITQOSApplicationID::SetQOSApplicationID (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e7783efaf8ec30ea8f70fec634eefff0acd2f5df99453fc1958258a5a26597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774595"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a>ItQOSApplicationID::SetQOSApplicationID (método)

\[Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método SetQOSApplicationID** establece el identificador de QOS para la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pApplicationID* \[ En\]
</dt> <dd>

Identificador único para el proceso de aplicación.

</dd> <dt>

*pApplicationGUID* \[ En\]
</dt> <dd>

GUID de aplicación.

</dd> <dt>

*pSubIDs* \[ En\]
</dt> <dd>

Sub-IDs asociada a la llamada actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITQOSApplicationID**](itqosapplicationid.md)
</dt> </dl>

 

 




