---
title: Función MpScanControl (MpClient.h)
description: Permite el control de un examen que se inició de forma asincrónica a través de MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Función MpScanControl Legacy Windows Environment Features
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
ms.openlocfilehash: 893fe1d01f9004c9dc2933a5bbb23c4b13fb8933a6121c41810c6e447e5eebac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114555"
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
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**PAUSA \_ DE MPCONTROL**</dt> </dl>    | Pause la operación de examen.<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**MPCONTROL \_ RESUME**</dt> </dl> | Reanude la operación de examen en pausa.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**.

Si se produce un error en la función, el valor devuelto es un **código HRESULT con** errores. El autor de la llamada puede usar [**la función MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerAbrir**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





