---
description: Controla el estado del dispositivo y los mensajes de error durante las transferencias de datos de imagen y muestra los mensajes al usuario.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'IWiaAppErrorHandler:: ReportStatus (método) (WIA. h)'
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
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705779"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a>IWiaAppErrorHandler:: ReportStatus (método)

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

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

No se utiliza. Establecer en 0.

</dd> <dt>

*pWiaItem2* \[ de\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Puntero al elemento que se va a transferir.

</dd> <dt>

_hrStatus * \[ en\]
</dt> <dd>

Tipo: **HRESULT**

Código de estado del dispositivo.

</dd> <dt>

*lPercentComplete* \[ de\]
</dt> <dd>

Tipo: **Long**

Porcentaje completado de la operación actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve *hrStatus* si no es posible la recuperación del error. De lo contrario, devuelve uno de los valores siguientes.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                     | Si *hrStatus* es un error, se realizó la acción adecuada para corregir el error y la transferencia puede continuar. Si *hrStatus* es informativo, se informa al usuario con un cuadro de diálogo no modal y decidió no cancelar la transferencia.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl>                  | El usuario canceló la transferencia del cuadro de diálogo no modal del controlador de errores. Este valor se puede devolver en cualquier momento, independientemente de lo que sea *hrStatus* . <br/>                                                                                      |
| <dl> <dt>**Estado de WIA \_ \_ no \_ controlado**</dt> </dl> | No se realizó ninguna acción. es decir, no se presentó ningún cuadro de diálogo al usuario. Se invocará el siguiente controlador de errores. El orden de los controladores de errores es: aplicación, controlador y valor predeterminado del sistema.<br/>                                                 |



 

## <a name="remarks"></a>Observaciones

El parámetro *lPercentComplete* habilita una ventana de controlador de errores para mostrar el progreso. Por ejemplo, un controlador podría proporcionar una estimación del tiempo que tarda "calentamiento". El parámetro *lPercentComplete* pasado a **IWiaAppErrorHandler:: ReportStatus** es el mismo valor que el **lPercentComplete** que el controlador establece en la estructura [**WiaTransferParams**](-wia-wiatransferparams.md) .

Un controlador de errores puede usar las macros SUCCEEDED y FAILed para averiguar si *hrStatus* tiene un \_ error de gravedad o una gravedad \_ correcta.

Si *hrStatus* es el éxito de la gravedad \_ , se debe permitir que el usuario cancele la transferencia.

Si *hrStatus* es \_ un error de gravedad, el controlador de errores debería mostrar un cuadro de diálogo modal perteneciente a la ventana primaria de la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




