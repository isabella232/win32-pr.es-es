---
title: Método BasicDevice.remove_ConnectionStatusChanged
description: Anula el registro de un controlador de eventos para el evento ConnectionStatusChanged. | Método BasicDevice.remove_ConnectionStatusChanged
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- método remove_ConnectionStatusChanged API de streaming multimedia
- método remove_ConnectionStatusChanged API de streaming multimedia, interfaz BasicDevice
- BasicDevice interface media streaming API, método remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280106"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a>BasicDevice. Remove \_ ConnectionStatusChanged (método)

Anula el registro de un controlador de eventos para el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*token* \[ de de\]
</dt> <dd>

Referencia a un token obtenido del método [**Add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) cuando se registró el controlador de eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

