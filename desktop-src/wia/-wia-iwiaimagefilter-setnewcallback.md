---
description: Establece una nueva devolución de llamada de aplicación para el filtro de procesamiento de imágenes que se usará para el reenvío de llamadas.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: Método IWiaImageFilter::SetNewCallback (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: abb279faba1c5174fc39ebdfe30a4a8cde8cabf86e8b86599f8d3ab9cc3247cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450495"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a>IWiaImageFilter::SetNewCallback (método)

Establece una nueva devolución de llamada de aplicación para el filtro de procesamiento de imágenes que se usará para el reenvío de llamadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWiaTransferCallback* \[ En\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**

Especifica un puntero a la interfaz [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) de la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

No llame a este método directamente desde la aplicación.

El filtro de procesamiento de imágenes es necesario para liberar la interfaz de devolución de llamada de aplicación almacenada previamente antes de establecer la nueva devolución de llamada.

Si *pWiaTransferCallback* es **NULL,** el filtro de procesamiento de imágenes simplemente debe liberar la devolución de llamada de aplicación anterior y devolver S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




