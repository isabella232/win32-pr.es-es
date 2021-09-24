---
title: Método GetProperty de IBackgroundCopyJob5 (Deliveryoptimization.h)
description: Método genérico para obtener Optimización de distribución de trabajo.
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
ms.openlocfilehash: 6c09d5886acb7d1bada165180e3d26bdf6505a6b
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520277"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a>IBackgroundCopyJob5::GetProperty (método)

Método genérico para obtener Optimización de distribución de trabajo.

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



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 se define como E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5::SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





