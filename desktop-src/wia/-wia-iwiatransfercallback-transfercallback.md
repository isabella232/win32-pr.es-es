---
description: Proporciona el progreso y otras notificaciones durante una transferencia.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: Método IWiaTransferCallback::TransferCallback (Wia.h)
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
ms.openlocfilehash: 02c24f4cb1795e233fbbbb3dc30ad1bbb3624e104d59ac72f8e310bbbd323820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440323"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a>IWiaTransferCallback::TransferCallback (Método)

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

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*pWiaTransferParams* \[ En\]
</dt> <dd>

Tipo: **[ **WiaTransferParams**](-wia-wiatransferparams.md)\***

Especifica un puntero a una [**estructura WiaTransferParams.**](-wia-wiatransferparams.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Cuando este método se implementa mediante un filtro de procesamiento de imágenes, el minidriver de adquisición de imágenes de Windows (WIA) 2.0 lo llama durante la adquisición de imágenes para enviar mensajes de progreso a la aplicación.

El método **IWiaTransferCallback::TransferCallback** de un filtro debe delegar en el método **IWiaTransferCallback::TransferCallback** de la devolución de llamada de la aplicación. Normalmente, el flujo de filtro filtra los datos que se le pasan y escribe los datos filtrados directamente en la secuencia proporcionada por la aplicación. Cuando el filtro de procesamiento de imágenes almacena datos entre llamadas a su método [IStream::Write,](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) también debe modificar los valores *lPercentComplete* y *ulBytesWrittenToCurrentStream* en la estructura [**WiaTransferParams.**](-wia-wiatransferparams.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
