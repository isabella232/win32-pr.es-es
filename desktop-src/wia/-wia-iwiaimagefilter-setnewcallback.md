---
description: Establece una nueva devolución de llamada de aplicación para el filtro de procesamiento de imágenes que se va a usar para las llamadas de reenvío.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'IWiaImageFilter:: SetNewCallback (método) (WIA. h)'
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
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810772"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a>IWiaImageFilter:: SetNewCallback (método)

Establece una nueva devolución de llamada de aplicación para el filtro de procesamiento de imágenes que se va a usar para las llamadas de reenvío.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWiaTransferCallback* \[ de\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**

Especifica un puntero a la interfaz [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) de la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

No llame a este método directamente desde su aplicación.

El filtro de procesamiento de imágenes es necesario para liberar la interfaz de devolución de llamada de la aplicación previamente almacenada antes de establecer la nueva devolución de llamada.

Si *pWiaTransferCallback* es **null**, el filtro de procesamiento de imágenes simplemente debe liberar la devolución de llamada de la aplicación anterior y devolver S \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




