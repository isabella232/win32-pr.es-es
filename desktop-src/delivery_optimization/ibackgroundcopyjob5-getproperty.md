---
title: Método GetProperty de IBackgroundCopyJob5 (Deliveryoptimization.h)
description: Método genérico para obtener Optimización de distribución de trabajo (DO).
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- Método GetProperty
- Método GetProperty, interfaz IBackgroundCopyJob5
- Interfaz IBackgroundCopyJob5, método GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2141afba2d2f58a08c62d609b9029c07ae07923e35f43e985f61a13a02aa68d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542804"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a>IBackgroundCopyJob5::GetProperty (método)

Método genérico para obtener Optimización de distribución de trabajo (DO).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PropertyId* \[ En\]
</dt> <dd>

Identificador de la propiedad que se obtiene especificada como un [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) de enumeración.

</dd> <dt>

*pPropertyValue* \[ out\]
</dt> <dd>

Valor de propiedad devuelto como una BITS_JOB_PROPERTY_VALUE unión.

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

[**IBackgroundCopyJob5::SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





