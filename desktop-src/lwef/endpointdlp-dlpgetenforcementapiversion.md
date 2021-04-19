---
description: Recupera la versión de la API de prevención de pérdida de datos (DLP) del punto de conexión en el dispositivo actual.
title: Función DlpGetEnforcementApiVersion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495949"
---
# <a name="dlpgetenforcementapiversion-function"></a>Función DlpGetEnforcementApiVersion

Recupera la versión de la API de prevención de pérdida de datos (DLP) del punto de conexión en el dispositivo actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MajorVersion* \[ En\]
</dt> <dd>

DWORD **que** especifica el número de versión principal.

</dd> </dl>

<dl> <dt>

*MajorVersion* \[ En\]
</dt> <dd>

DWORD **que** especifica el número de versión secundaria.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve un valor HRESULT que incluye, entre otros, los valores siguientes.

| HRESULT | Descripción |
|---------|-------------|
| S_OK | La función se completó correctamente |




## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |