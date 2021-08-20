---
description: Obtiene el tamaño de la matriz que se debe asignar antes de llamar a CreateOPMProtectedOutputs.
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: Función GetSuggestedOPMProtectedOutputArraySize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: c84738fe37661d2a593432b571c6022b0369e28ee3b2a3cb028b8eb84276a21a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879382"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a>Función GetSuggestedOPMProtectedOutputArraySize

> [!IMPORTANT]
> Output [Protection Manager](output-protection-manager.md) (OPM) usa esta función para acceder a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Obtiene el tamaño de la matriz que se debe asignar antes de llamar a [**CreateOPMProtectedOutputs.**](createopmprotectedoutputs.md)

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pstrDeviceName* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ STRING UNICODE**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo para mostrar, tal y como devuelve la función [**GetMonitorInfo.**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)

</dd> <dt>

*pdwSuggestedOPMProtectedOutputArraySize* \[ out\]
</dt> <dd>

Recibe el tamaño que se debe asignar para la matriz, en número de elementos de matriz.

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

 

 
