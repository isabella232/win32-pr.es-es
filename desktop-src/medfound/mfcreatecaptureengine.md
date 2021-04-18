---
description: Crea una instancia del motor de captura.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: MFCreateCaptureEngine función)
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
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715372"
---
# <a name="mfcreatecaptureengine-function"></a>MFCreateCaptureEngine función)

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

*ppCaptureEngine* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) . El llamador debe liberar la interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve S \_ correcto. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función no tiene asociada ninguna biblioteca de importación y no está declarada en un archivo de encabezado público. Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a MFCaptureEngine.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                        |
| Archivo DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
