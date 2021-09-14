---
title: Función MpScanControl (MpClient.h)
description: Permite el control de un examen que se inició de forma asincrónica a través de MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Características heredadas del entorno de Windows mpScanControl
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269468"
---
# <a name="mpscancontrol-function"></a>Función MpScanControl

Permite el control de un examen que se inició de forma asincrónica a través de [**MpScanStart**](mpscanstart.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hScanHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Controlar una operación de examen asincrónica. La función [**MpScanStart**](mpscanstart.md) devuelve este identificador. Este parámetro también se puede establecer en el identificador de interfaz del administrador de protección contra malware devuelto por la función [**MpManagerOpen**](mpmanageropen.md) para controlar un examen iniciado por el sistema, en cuyo caso el autor de la llamada debe tener privilegios administrativos.

</dd> <dt>

*ScanControl* \[ En\]
</dt> <dd>

Tipo: **MPCONTROL**

Especifica una opción de control de examen. Este parámetro debe ser una de las siguientes opciones de control:



| Value                                                                                                                                                                  | Significado                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**MPCONTROL \_ ABORT**</dt> </dl>    | Anule la operación de examen.<br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**MPCONTROL \_ PAUSE**</dt> </dl>    | Pausar la operación de examen.<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**MPCONTROL \_ RESUME**</dt> </dl> | Reanude la operación de examen en pausa.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**.

Si se produce un error en la función, el valor devuelto es un **código HRESULT** con errores. El autor de la llamada puede [**usar la función MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerAbrir**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





