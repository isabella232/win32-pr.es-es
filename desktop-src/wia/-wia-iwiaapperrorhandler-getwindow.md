---
description: Obtiene un identificador para el cuadro de diálogo que muestra los mensajes de error y proporciona uno o varios botones para continuar, cancelar o anular la aplicación.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'IWiaAppErrorHandler:: GetWindow (método) (WIA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716057"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a>IWiaAppErrorHandler:: GetWindow (método)

Obtiene un identificador para el cuadro de diálogo que muestra los mensajes de error y proporciona uno o varios botones para continuar, cancelar o anular la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phwnd* \[ enuncia\]
</dt> <dd>

Tipo: **hWnd \** _

HWND usado por el controlador de errores de la aplicación, el controlador de errores del controlador y los cuadros de diálogo de mensajes de dispositivo predeterminados (error e informativo). El valor de salida puede ser _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

*phwnd* apunta a la ventana pasada en [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) por el proxy de adquisición de imágenes de Windows (WIA) 2,0. Esta ventana debe ser válida mientras dure la transferencia de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




