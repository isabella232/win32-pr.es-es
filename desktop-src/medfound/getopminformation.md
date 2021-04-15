---
description: Envía una solicitud de estado de OPM a un objeto de salida protegido.
ms.assetid: 4b691b20-25de-4b9e-a725-674a57697b56
title: GetOPMInformation función)
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
ms.openlocfilehash: 450292c0f6352436d7df8c91afff0d08c8c31394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696142"
---
# <a name="getopminformation-function"></a>GetOPMInformation función)

> [!IMPORTANT]
> El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

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

*opoOPMProtectedOutput* \[ de\]
</dt> <dd>

Identificador del objeto de salida protegido. Este identificador se obtiene llamando a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*pParameters* \[ de\]
</dt> <dd>

Un puntero a una estructura de **\_ parámetros de obtención de \_ \_ información \_ de DXGKMDT OPM** que contiene los datos de entrada para la solicitud de estado.

</dd> <dt>

*pRequestedInformation* \[ enuncia\]
</dt> <dd>

Un puntero a una estructura de **información de DXGKMDT \_ OPM \_ solicitada \_** que recibe los resultados de la solicitud de estado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**. De lo contrario, devuelve un código de error **NTSTATUS** .

## <a name="remarks"></a>Observaciones

Las aplicaciones deben llamar a [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) en lugar de llamar a esta función.

El objeto de salida protegido se debe crear con la semántica de OPM. Vea [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de OPM](opm-functions.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 
