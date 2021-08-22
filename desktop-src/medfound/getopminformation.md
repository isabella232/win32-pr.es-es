---
description: Envía una solicitud de estado de OPM a un objeto de salida protegido.
ms.assetid: 4b691b20-25de-4b9e-a725-674a57697b56
title: Función GetOPMInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bd9912289d17085bf94f3ef8316869ffb29d3a5adead4e10fc0e6d24844f4ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777305"
---
# <a name="getopminformation-function"></a>Función GetOPMInformation

> [!IMPORTANT]
> Output [Protection Manager](output-protection-manager.md) (OPM) usa esta función para acceder a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Envía una solicitud de estado de OPM a un objeto de salida protegido.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI GetOPMInformation(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE       opoOPMProtectedOutput,
  _In_  const DXGKMDT_OPM_GET_INFO_PARAMETERS   *pParameters,
  _Out_       DXGKMDT_OPM_REQUESTED_INFORMATION *pRequestedInformation
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

Puntero a una estructura **DXGKMDT \_ OPM \_ GET INFO \_ \_ PARAMETERS** que contiene datos de entrada para la solicitud de estado.

</dd> <dt>

*pRequestedInformation* \[ out\]
</dt> <dd>

Puntero a una estructura DE INFORMACIÓN SOLICITADA **DE DXGKMDT \_ OPM \_ \_** que recibe los resultados de la solicitud de estado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Comentarios

Las aplicaciones deben [**llamar a IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) en lugar de llamar a esta función.

El objeto de salida protegido debe crearse con semántica de OPM. Vea [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

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

 

 
