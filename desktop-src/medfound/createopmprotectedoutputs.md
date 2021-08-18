---
description: Crea objetos de salida protegidos para un dispositivo de visualización.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: Función CreateOPMProtectedOutputs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: fe2bcc0d190cf94a48b10f3d588ab4acd2d93913552f8ccef9d7eb92fefa598b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829065"
---
# <a name="createopmprotectedoutputs-function"></a>Función CreateOPMProtectedOutputs

> [!IMPORTANT]
> El Administrador de [](output-protection-manager.md) protección de salida (OPM) usa esta función para acceder a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Crea objetos de salida protegidos para un dispositivo de visualización.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pstrDeviceName* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ STRING UNICODE**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo para mostrar, tal y como devuelve la función [**GetMonitorInfo.**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)

</dd> <dt>

*zona de trabajo* \[ En\]
</dt> <dd>

Miembro de la enumeración **DXGKMDT \_ OPM \_ VIDEO OUTPUT \_ \_ SEMANTICS,** que especifica si la salida protegida tendrá semántica del Protocolo de protección de salida certificado (COPP) o semántica de OPM.

</dd> <dt>

*dwOPMProtectedOutputArraySize* \[ En\]
</dt> <dd>

Número de elementos de la matriz *pohOPMProtectedOutputArray.*

</dd> <dt>

*pdwNumOPMProtectedOutputsInArray* \[ out\]
</dt> <dd>

Recibe el número de elementos que la función copia en la *matriz pohOPMProtectedOutputArray.*

</dd> <dt>

*pohOPMProtectedOutputArray* \[ out\]
</dt> <dd>

Matriz que recibe identificadores para los objetos de salida protegidos. Cada identificador debe liberarse llamando a [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Comentarios

En lugar de usar esta función, las aplicaciones deben llamar a una de las siguientes funciones:

-   [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

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

 

 
