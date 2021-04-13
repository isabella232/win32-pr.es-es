---
description: Obtiene un número aleatorio seguro criptográficamente de 128 bits de un objeto de salida protegido.
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: GetOPMRandomNumber función)
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
ms.openlocfilehash: f78b17dcf9ffff7a5fa26ce16e96299e5cf8386c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360089"
---
# <a name="getopmrandomnumber-function"></a>GetOPMRandomNumber función)

> [!IMPORTANT]
> El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

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

*opoOPMProtectedOutput* \[ de\]
</dt> <dd>

Identificador del objeto de salida protegido. Este identificador se obtiene llamando a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*prnRandomNumber* \[ enuncia\]
</dt> <dd>

Puntero a una estructura **de \_ \_ \_ número aleatorio de DXGKMDT OPM** que recibe el número aleatorio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**. De lo contrario, devuelve un código de error **NTSTATUS** .

## <a name="remarks"></a>Observaciones

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

 

 
