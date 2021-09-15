---
description: Envía una solicitud de estado del Protocolo de protección de salida certificado (COPP) a un objeto de salida protegido.
ms.assetid: 24300591-c0c0-48a2-99d3-be98c0c1492a
title: Función GetCOPPCompatibleOPMInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCOPPCompatibleOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7e5eac24dfcf08e45ce414090835792e594d7c37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580004"
---
# <a name="getcoppcompatibleopminformation-function"></a>Función GetCOPPCompatibleOPMInformation

> [!IMPORTANT]
> El Administrador de [](output-protection-manager.md) protección de salida (OPM) usa esta función para acceder a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Envía una solicitud de estado del Protocolo de protección de salida certificado (COPP) a un objeto de salida protegido.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI GetCOPPCompatibleOPMInformation(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE                     opoOPMProtectedOutput,
  _In_  DXGKMDT_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
  _Out_ DXGKMDT_OPM_REQUESTED_INFORMATION               *pRequestedInformation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*opoOPMProtectedOutput* \[ En\]
</dt> <dd>

Identificador del objeto de salida protegido. Este identificador se obtiene mediante una llamada a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*pParameters* \[ En\]
</dt> <dd>

Puntero a una estructura **DXGKMDT \_ OPM \_ COPP \_ COMPATIBLE GET \_ INFO \_ \_ PARAMETERS** que contiene datos de entrada para la solicitud de estado.

</dd> <dt>

*pRequestedInformation* \[ out\]
</dt> <dd>

Puntero a una estructura DE INFORMACIÓN SOLICITADA **DE DXGKMDT \_ OPM \_ \_** que recibe los resultados de la solicitud de estado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Observaciones

Las aplicaciones deben [**llamar a IOPMVideoOutput::COPPCompatibleGetInformation en**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) lugar de llamar a esta función.

El objeto de salida protegido debe crearse con semántica de COPP. Vea [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe usar las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de OPM](opm-functions.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 
