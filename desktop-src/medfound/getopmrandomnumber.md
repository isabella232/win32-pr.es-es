---
description: Obtiene un número aleatorio seguro criptográficamente de 128 bits de un objeto de salida protegido.
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: Función GetOPMRandomNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMRandomNumber
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 522cb1ea1ff44e83bdb77e63d30edf6e0cf892a5918db76aad4076e4c67f0fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879392"
---
# <a name="getopmrandomnumber-function"></a>Función GetOPMRandomNumber

> [!IMPORTANT]
> El Administrador de [](output-protection-manager.md) protección de salida (OPM) usa esta función para acceder a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Obtiene un número aleatorio seguro criptográficamente de 128 bits de un objeto de salida protegido.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI GetOPMRandomNumber(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput,
  _Out_ DXGKMDT_OPM_RANDOM_NUMBER   *prnRandomNumber
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*opoOPMProtectedOutput* \[ En\]
</dt> <dd>

Identificador del objeto de salida protegido. Este identificador se obtiene mediante una llamada a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*prnRandomNumber* \[ out\]
</dt> <dd>

Puntero a una **estructura DXGKMDT \_ OPM \_ RANDOM \_ NUMBER** que recibe el número aleatorio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Comentarios

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe usar las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 
