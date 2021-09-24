---
title: Método IBackgroundCopyJob5 SetProperty (Deliveryoptimization.h)
description: Método genérico para establecer Optimización de distribución de trabajo.
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
ms.openlocfilehash: 3b006ab3c4e53db1a9e76d35c8812ec32f09dffa
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520505"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>IBackgroundCopyJob5::SetProperty (método)

Método genérico para establecer Optimización de distribución de trabajo.

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

Identificador de la propiedad que se establece como un [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) de enumeración.

</dd> <dt>

*PropertyValue* \[ En\]
</dt> <dd>

Valor de la propiedad que se va a establecer. Para contener un valor cuyo tipo es adecuado para la propiedad , este valor se especifica [**a**](bits-job-property-value-.md) través de la unión BITS_JOB_PROPERTY_VALUE que se compone de todos los tipos de propiedad conocidos.

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

[**IBackgroundCopyJob5::GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





