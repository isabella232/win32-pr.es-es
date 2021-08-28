---
description: Controla los mensajes de estado y error durante las transferencias de datos de imagen y los muestra al usuario.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: Método IWiaErrorHandler::ReportStatus (Wia.h)
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
ms.openlocfilehash: 6604dc8dbf0cad5f31449ff3cc30945c1e6059727d513fa98dbf436eb199f70f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659755"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a>IWiaErrorHandler::ReportStatus (método)

Controla los mensajes de estado y error durante las transferencias de datos de imagen y los muestra al usuario.

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

*hwndParent* \[ En\]
</dt> <dd>

Tipo: **HWND**

**HWND** que es la ventana primaria de la ventana de mensajes.

</dd> <dt>

*itemitem* \[ En\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntero a la [interfaz IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) del elemento que se va a transferir. Este objeto implementa mínimamente [**IWiaItem2**](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ En\]
</dt> <dd>

Tipo: **HRESULT**

**HRESULT** que es el código de estado recibido por [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*cbResLength* \[ En\]
</dt> <dd>

Tipo: **LONG**

**LONG** que es el tamaño de los datos a los que hace referencia *pbData.*

</dd> <dt>

*pbData* \[ En\]
</dt> <dd>

Tipo: **\* BYTE**

Puntero al búfer de datos recibido por [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve *hrStatus si* no se puede recuperar el error. De lo contrario, devuelve uno de los siguientes valores.



| Código devuelto                                                                             | Descripción                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Se ha realizado la acción adecuada para corregir el error y la transferencia puede continuar. <br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | No se ha realizado ninguna acción para controlar el error o el estado del informe al usuario. <br/>                |
| <dl> <dt>**E \_ ABORT**</dt> </dl> | El usuario eligió anular la transferencia en respuesta al cuadro de diálogo mostrado. <br/>        |



 

## <a name="remarks"></a>Comentarios

Windows Adquisición de imágenes (WIA) 2.0 llama a **IWiaErrorHandler::ReportStatus** cuando el controlador envía un mensaje DE ESTADO DEL DISPOSITIVO DE MENSAJES DE TI a [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback). **\_ \_ \_** Este método controla el mensaje y muestra información al usuario sobre el estado o el error. Si el mensaje trata de un error, el método permite al usuario elegir, si es posible, si desea intentar recuperarse del error y continuar con la transferencia o anular.

*hrStatus se* establece en WIA \_ STATUS TRANSFER BEGIN para informar al controlador de que se ha iniciado una \_ \_ transferencia. Se establece en WIA \_ STATUS TRANSFER END cuando se completa la \_ \_ transferencia.

Si *hrStatus* es SEVERITY SUCCESS, se debe permitir al usuario \_ cancelar la transferencia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
