---
description: El método SetQOSApplicationID establece el identificador de QOS de la aplicación.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'ITQOSApplicationID:: SetQOSApplicationID (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681239"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a>ITQOSApplicationID:: SetQOSApplicationID (método)

\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **SetQOSApplicationID** establece el identificador de QoS de la aplicación.

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

*pApplicationID* \[ de\]
</dt> <dd>

Identificador único para el proceso de aplicación.

</dd> <dt>

*pApplicationGUID* \[ de\]
</dt> <dd>

GUID de la aplicación.

</dd> <dt>

*pSubIDs* \[ de\]
</dt> <dd>

Sub-IDs asociado a la llamada actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITQOSApplicationID**](itqosapplicationid.md)
</dt> </dl>

 

 




