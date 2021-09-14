---
title: Función MpUpdateControl (MpClient.h)
description: Permite el control de una operación de actualización de firma que se inició de forma asincrónica a través de MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Función MpUpdateControl Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168269"
---
# <a name="mpupdatecontrol-function"></a>Función MpUpdateControl

Permite el control de una operación de actualización de firma que se inició de forma asincrónica a través [**de MpUpdateStart**](mpupdatestart.md). Llamar a esta función requiere privilegios de administrador, ya que permite la cancelación de una actualización de firma en todo el sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hUpdateHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Controlar una operación asincrónica de actualización de firma. La función [**MpScanStart**](mpscanstart.md) devuelve este identificador.

</dd> <dt>

*UpdateControl* \[ En\]
</dt> <dd>

Tipo: **MPCONTROL**

Especifica la opción de control de actualización de firma. Debe ser el valor siguiente:



| Value                                                                                                                                                               | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**MPCONTROL \_ ABORT**</dt> </dl> | Anule la operación de actualización de firma.<br/> |



 

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
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





