---
description: Establece la clave de firma y dos números de secuencia en un objeto de salida protegido.
ms.assetid: 278a80f5-198d-4311-aa43-10b6dc33b3a4
title: Función SetOPMSigningKeyAndSequenceNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetOPMSigningKeyAndSequenceNumbers
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: cbd088b83acd4e93cc186e6c7b5635ad1e3d8346
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574800"
---
# <a name="setopmsigningkeyandsequencenumbers-function"></a>Función SetOPMSigningKeyAndSequenceNumbers

> [!IMPORTANT]
> Output [Protection Manager](output-protection-manager.md) (OPM) usa esta función para acceder a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Establece la clave de firma y dos números de secuencia en un objeto de salida protegido.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI SetOPMSigningKeyAndSequenceNumbers(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _Out_ const DXGKMDT_OPM_ENCRYPTED_PARAMETERS *pParameters
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*opoOPMProtectedOutput* \[ En\]
</dt> <dd>

Identificador del objeto de salida protegido. Este identificador se obtiene mediante una llamada a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*pParameters* \[ out\]
</dt> <dd>

Puntero a una estructura [**DXGKMDT \_ OPM \_ ENCRYPTED \_ PARAMETERS**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) que contiene una matriz de 256 bytes. Para obtener más información sobre cómo inicializar esta matriz, vea [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Observaciones

Las aplicaciones deben [**llamar a IOPMVideoOutput::FinishInitialization en**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) lugar de llamar a esta función.

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe usar las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de OPM](opm-functions.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 
