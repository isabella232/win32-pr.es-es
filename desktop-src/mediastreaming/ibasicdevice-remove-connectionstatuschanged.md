---
title: Método remove_ConnectionStatusChanged IBasicDevice
description: Anula el registro de un controlador de eventos para el evento ConnectionStatusChanged. | Método remove_ConnectionStatusChanged IBasicDevice
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- método remove_ConnectionStatusChanged API de streaming multimedia
- método remove_ConnectionStatusChanged API de streaming multimedia, interfaz IBasicDevice
- IBasicDevice interface media streaming API, método remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105707681"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>IBasicDevice:: Remove \_ ConnectionStatusChanged (método)

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

Referencia a un token obtenido del método [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) cuando se registró el controlador de eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





