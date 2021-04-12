---
title: Función MpUpdateControl (MpClient. h)
description: Permite el control de una operación de actualización de firmas que se inició de forma asincrónica a través de MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Función MpUpdateControl características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491548"
---
# <a name="mpupdatecontrol-function"></a>MpUpdateControl función)

Permite el control de una operación de actualización de firmas que se inició de forma asincrónica a través de [**MpUpdateStart**](mpupdatestart.md). La llamada a esta función requiere privilegios de administrador, ya que permite la cancelación de una actualización de firmas en todo el sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hUpdateHandle* \[ de\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de una operación de actualización de firma asincrónica. La función [**MpScanStart**](mpscanstart.md) devuelve este identificador.

</dd> <dt>

*UpdateControl* \[ de\]
</dt> <dd>

Tipo: **MPCONTROL**

Especifica la opción de control de actualización de firmas. Debe ser el siguiente valor:



| Value                                                                                                                                                               | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**\_anulación de MPCONTROL**</dt> </dl> | Anular la operación de actualización de firma.<br/> |



 

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

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





