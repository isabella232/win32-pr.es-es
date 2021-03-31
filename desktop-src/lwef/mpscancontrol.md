---
title: Función MpScanControl (MpClient. h)
description: Permite el control de un examen que se inició de forma asincrónica a través de MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Función MpScanControl características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490390"
---
# <a name="mpscancontrol-function"></a>MpScanControl función)

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

*hScanHandle* \[ de\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de una operación de examen asincrónico. La función [**MpScanStart**](mpscanstart.md) devuelve este identificador. Este parámetro también se puede establecer en el identificador de la interfaz del administrador de protección contra malware devuelto por la función [**MpManagerOpen**](mpmanageropen.md) para controlar un examen iniciado por el sistema, en cuyo caso el llamador debe tener privilegios administrativos.

</dd> <dt>

*ScanControl* \[ de\]
</dt> <dd>

Tipo: **MPCONTROL**

Especifica una opción de control de exploración. Este parámetro debe ser una de las siguientes opciones de control:



| Value                                                                                                                                                                  | Significado                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**\_anulación de MPCONTROL**</dt> </dl>    | Anular la operación de examen.<br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**pausar MPCONTROL \_**</dt> </dl>    | Pausar la operación de examen.<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**\_reanudación de MPCONTROL**</dt> </dl> | Reanude la operación de examen en pausa.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.

Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo. El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





