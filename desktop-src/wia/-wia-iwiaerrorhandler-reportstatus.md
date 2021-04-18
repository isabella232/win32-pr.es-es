---
description: Controla el estado y los mensajes de error durante las transferencias de datos de imagen y los muestra al usuario.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'IWiaErrorHandler:: ReportStatus (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667487"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a>IWiaErrorHandler:: ReportStatus (método)

Controla el estado y los mensajes de error durante las transferencias de datos de imagen y los muestra al usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Tipo: **hWnd**

**HWnd** que es la ventana primaria de la ventana de mensaje.

</dd> <dt>

*punkItem* \[ de\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Puntero a la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) del elemento que se va a transferir. Este objeto implementa mínimamente [_ *IWiaItem2* *](-wia-iwiaitem2.md) y [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ de\]
</dt> <dd>

Tipo: **HRESULT**

**HRESULT** que es el código de estado recibido por [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*cbResLength* \[ de\]
</dt> <dd>

Tipo: **Long**

**Long** que es el tamaño de los datos a los que hace referencia *pbData*.

</dd> <dt>

*pbData* \[ de\]
</dt> <dd>

Tipo: **byte \** _

Puntero al búfer de datos tal y como lo recibe [_ *BandedDataCallback* *](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve *hrStatus* si el error no se puede recuperar de. De lo contrario, devuelve uno de los valores siguientes.



| Código devuelto                                                                             | Descripción                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Se realizó la acción adecuada para corregir el error y la transferencia puede continuar. <br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | No se realizó ninguna acción para controlar el estado del error o del informe al usuario. <br/>                |
| <dl> <dt>**E \_ anular**</dt> </dl> | El usuario decidió anular la transferencia en respuesta al cuadro de diálogo que se muestra. <br/>        |



 

## <a name="remarks"></a>Observaciones

La adquisición de imágenes de Windows (WIA) 2,0 llama a **IWiaErrorHandler:: ReportStatus** cuando el controlador envía un mensaje de [](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback) **\_ \_ \_ Estado de dispositivo MSG de ti** a BandedDataCallback. Este método controla el mensaje y muestra información al usuario sobre el estado o el error. Si el mensaje es un error, el método permite al usuario elegir, si es posible, si intenta recuperar el error y continuar con la transferencia o anular la operación.

*hrStatus* se establece en \_ la transferencia de estado de WIA \_ \_ Inicio para informar al controlador de que se ha iniciado una transferencia. Se establece en fin de \_ la transferencia de estado de WIA \_ \_ cuando se completa la transferencia.

Si *hrStatus* es el éxito de la gravedad \_ , se debe permitir que el usuario cancele la transferencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
