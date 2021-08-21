---
title: BasicDevice.remove_ConnectionStatusChanged método
description: Anula el registro de un controlador de eventos para el evento ConnectionStatusChanged. | BasicDevice.remove_ConnectionStatusChanged método
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- remove_ConnectionStatusChanged media streaming API
- remove_ConnectionStatusChanged media streaming API, interfaz BasicDevice
- BasicDevice interface Media Streaming API , remove_ConnectionStatusChanged método
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89057195c23aa917c7338a8abb740817bb6af7896261cf1d31bcb37d5d5d5ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972504"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a>Método BasicDevice.remove \_ ConnectionStatusChanged

Anula el registro de un controlador de eventos para [**el evento ConnectionStatusChanged.**](connectionstatuschanged.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*token* \[ En\]
</dt> <dd>

Referencia a un token obtenido del método [**\_ add ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) cuando se registró el controlador de eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

