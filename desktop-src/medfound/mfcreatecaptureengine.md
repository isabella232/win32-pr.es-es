---
description: Crea una instancia del motor de captura.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: Función MFCreateCaptureEngine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: 18d264b30b8f3ed4d06e80f236908dd7bc81dbe96c4eb9c3231fa330331e34f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940255"
---
# <a name="mfcreatecaptureengine-function"></a>Función MFCreateCaptureEngine

\[MFCreateCaptureEngine no se admite y puede modificarse o no estar disponible en el futuro. \]

Crea una instancia del motor de captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppCaptureEngine* \[ out\]
</dt> <dd>

Recibe un puntero a la [**interfaz IMFCaptureEngine.**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) El autor de la llamada debe liberar la interfaz .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve S \_ OK. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función no tiene ninguna biblioteca de importación asociada y no se declara en un archivo de encabezado público. Debe usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a MFCaptureEngine.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                        |
| Archivo DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation Functions](media-foundation-functions.md)
</dt> </dl>

 

 
