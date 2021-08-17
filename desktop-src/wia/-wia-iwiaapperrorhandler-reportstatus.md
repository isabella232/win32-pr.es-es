---
description: Controla el estado del dispositivo y los mensajes de error durante las transferencias de datos de imagen y muestra los mensajes al usuario.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: Método IWiaAppErrorHandler::ReportStatus (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 9cc727845489740fae54dcc96bf5bc903bceb0205688c1c60bee3df980f66845
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965754"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a>IWiaAppErrorHandler::ReportStatus (método)

Controla el estado del dispositivo y los mensajes de error durante las transferencias de datos de imagen y muestra los mensajes al usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

No se utiliza. Establecer en 0.

</dd> <dt>

*pWiaItem2* \[ En\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Puntero al elemento que se va a transferir.

</dd> <dt>

*hrStatus* \[ En\]
</dt> <dd>

Tipo: **HRESULT**

Código de estado del dispositivo.

</dd> <dt>

*lPercentComplete* \[ En\]
</dt> <dd>

Tipo: **LONG**

Porcentaje completado de la operación actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve *hrStatus si* no es posible la recuperación del error. De lo contrario, devuelve uno de los valores siguientes.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Si *hrStatus* es un error, se ha realizado la acción adecuada para corregir el error y la transferencia puede continuar. Si *hrStatus* es informativo, se informó al usuario con un cuadro de diálogo no modelo y optó por no cancelar la transferencia.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                  | El usuario canceló la transferencia desde el cuadro de diálogo modeless del controlador de errores. Este valor se puede devolver en cualquier momento, independientemente de *qué sea hrStatus.* <br/>                                                                                      |
| <dl> <dt>**ESTADO DE WIA \_ \_ NO \_ MANIPULADO**</dt> </dl> | No se ha realizado ninguna acción; es decir, no se presentó ningún cuadro de diálogo al usuario. Se invocará el siguiente controlador de errores. El orden de los controladores de errores es: aplicación, controlador y valor predeterminado del sistema.<br/>                                                 |



 

## <a name="remarks"></a>Comentarios

El *parámetro lPercentComplete* permite que una ventana del controlador de errores muestre el progreso. Por ejemplo, un controlador podría proporcionar una estimación del tiempo que tarda el "warming up". El *parámetro lPercentComplete* pasado a **IWiaAppErrorHandler::ReportStatus** es el mismo valor que **lPercentComplete** que el controlador establece en la estructura [**WiaTransferParams.**](-wia-wiatransferparams.md)

Un controlador de errores puede usar las macros SUCCEEDED y FAILED para averiguar si *hrStatus* tiene UN ERROR DE \_ GRAVEDAD o UN ERROR DE GRAVEDAD \_ CORRECTO.

Si *hrStatus* es SEVERITY \_ SUCCESS, el usuario debe tener permiso para cancelar la transferencia.

Si *hrStatus* es SEVERITY ERROR, el controlador de errores debe mostrar un cuadro de \_ diálogo modal propiedad de la ventana primaria de la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




