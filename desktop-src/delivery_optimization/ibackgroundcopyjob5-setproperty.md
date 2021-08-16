---
title: Método IBackgroundCopyJob5 SetProperty (Deliveryoptimization.h)
description: Método genérico para establecer Optimización de distribución de trabajo (DO).
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty (método)
- Método SetProperty, interfaz IBackgroundCopyJob5
- Interfaz IBackgroundCopyJob5, método SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f9b7dab17780572a59e12dde9905c3d8db23895e6564aac47cb6eb2d984bfaf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542688"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>IBackgroundCopyJob5::SetProperty (Método)

Método genérico para establecer Optimización de distribución de trabajo (DO).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PropertyId* \[ En\]
</dt> <dd>

Identificador de la propiedad que se va a establecer especificada como un [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) de enumeración.

</dd> <dt>

*PropertyValue* \[ En\]
</dt> <dd>

Valor de la propiedad que se establece. Para contener un valor cuyo tipo es adecuado para la propiedad , este valor se especifica [**a**](bits-job-property-value-.md) través de la unión BITS_JOB_PROPERTY_VALUE que se compone de todos los tipos de propiedad conocidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve los siguientes valores devueltos.



| Código devuelto                                                                          | Descripción        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Correcto<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 se define como E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5::GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





