---
description: Proporciona el progreso y otras notificaciones durante una transferencia.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'IWiaTransferCallback:: TransferCallback (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696517"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a>IWiaTransferCallback:: TransferCallback (método)

Proporciona el progreso y otras notificaciones durante una transferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*pWiaTransferParams* \[ de\]
</dt> <dd>

Tipo: **[**WiaTransferParams**](-wia-wiatransferparams.md) \** _

Especifica un puntero a una estructura [_ *WiaTransferParams* *](-wia-wiatransferparams.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Cuando un filtro de procesamiento de imágenes implementa este método, el minicontrolador de adquisición de imágenes de Windows (WIA) 2,0 lo llama durante la adquisición de la imagen para devolver mensajes de progreso a la aplicación.

**IWiaTransferCallback:: TransferCallback** de un filtro debe delegarse en el método **IWiaTransferCallback:: TransferCallback** de la devolución de llamada de la aplicación. Normalmente, el flujo de filtro filtra los datos que se le pasan y escribe los datos filtrados directamente en la secuencia proporcionada por la aplicación. Cuando el filtro de procesamiento de imágenes almacena datos entre llamadas a su método [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , también debe modificar los valores *lPercentComplete* y *ulBytesWrittenToCurrentStream* en la estructura [**WiaTransferParams**](-wia-wiatransferparams.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
