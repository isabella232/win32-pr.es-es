---
description: Obtiene un identificador del cuadro de diálogo que muestra los mensajes de error y proporciona uno o varios botones para continuar, cancelar o anular la aplicación.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: Método IWiaAppErrorHandler::GetWindow (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571381"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a>IWiaAppErrorHandler::GetWindow (método)

Obtiene un identificador del cuadro de diálogo que muestra los mensajes de error y proporciona uno o varios botones para continuar, cancelar o anular la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phwnd* \[ out\]
</dt> <dd>

Tipo: **HWND\***

HWND usado por el controlador de errores de la aplicación, el controlador de errores del controlador y el controlador de errores predeterminado para los cuadros de diálogo de mensaje de dispositivo (tanto de error como informativos). El valor de salida puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

*phwnd apunta* a la ventana pasada a [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) por el proxy Windows Image Acquisition (WIA) 2.0. Esta ventana debe seguir siendo válida mientras dure la transferencia de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




