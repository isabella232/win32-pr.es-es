---
title: Método SetProperty de IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Método genérico para configurar las propiedades del trabajo de optimización de entrega (DO).
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
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803295"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>IBackgroundCopyJob5:: SetProperty (método)

Método genérico para configurar las propiedades del trabajo de optimización de entrega (DO).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PropertyId* \[ de\]
</dt> <dd>

IDENTIFICADOR de la propiedad que se establece como un valor de enumeración de [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .

</dd> <dt>

*PropertyValue* \[ de\]
</dt> <dd>

Valor de la propiedad que se va a establecer. Para contener un valor cuyo tipo sea adecuado para la propiedad, este valor se especifica a través de la Unión [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) que se compone de todos los tipos de propiedad conocidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve los siguientes valores devueltos.



| Código devuelto                                                                          | Descripción        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Correcto<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 se define como E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5:: GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





