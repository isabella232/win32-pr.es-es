---
description: Crea objetos de salida protegidos para un dispositivo de pantalla.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: CreateOPMProtectedOutputs función)
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
ms.openlocfilehash: 215cff4a76e7eb36e516e8fd2db312302763198e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539616"
---
# <a name="createopmprotectedoutputs-function"></a>CreateOPMProtectedOutputs función)

> [!IMPORTANT]
> El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Crea objetos de salida protegidos para un dispositivo de pantalla.

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

*pstrDeviceName* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ cadena Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo de pantalla, tal y como lo devuelve la función [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*vos* \[ de\]
</dt> <dd>

Un miembro de la enumeración de **semántica de salida de vídeo de DXGKMDT \_ OPM \_ \_ \_** , que especifica si la salida protegida tendrá semántica de protocolo de protección de salida (COPP) o semántica de OPM.

</dd> <dt>

*dwOPMProtectedOutputArraySize* \[ de\]
</dt> <dd>

Número de elementos de la matriz *pohOPMProtectedOutputArray* .

</dd> <dt>

*pdwNumOPMProtectedOutputsInArray* \[ enuncia\]
</dt> <dd>

Recibe el número de elementos que la función copia en la matriz *pohOPMProtectedOutputArray* .

</dd> <dt>

*pohOPMProtectedOutputArray* \[ enuncia\]
</dt> <dd>

Matriz que recibe los identificadores de los objetos de salida protegidos. Cada identificador se debe liberar llamando a [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**. De lo contrario, devuelve un código de error **NTSTATUS** .

## <a name="remarks"></a>Observaciones

En lugar de usar esta función, las aplicaciones deben llamar a una de las siguientes funciones:

-   [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

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

 

 
