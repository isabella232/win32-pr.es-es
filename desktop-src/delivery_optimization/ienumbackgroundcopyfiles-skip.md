---
title: IEnumBackgroundCopyFiles SKIP (método) (Deliveryoptimization. h)
description: Omite el siguiente número de elementos especificado en la secuencia de enumeración. Si quedan menos elementos en la secuencia que el número solicitado de elementos que se van a omitir, se omite el último elemento de la secuencia.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip (método)
- SKIP (método), IEnumBackgroundCopyFiles (interfaz)
- IEnumBackgroundCopyFiles (interfaz), SKIP (método)
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079016"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a>IEnumBackgroundCopyFiles:: Skip (método)

Omite el siguiente número de elementos especificado en la secuencia de enumeración. Si quedan menos elementos en la secuencia que el número solicitado de elementos que se van a omitir, se omite el último elemento de la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Celt* \[ de\]
</dt> <dd>

Número de elementos que se van a omitir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                              | Descripción                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Se omitió correctamente el número de elementos solicitados.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Se omitió un valor menor que el número de elementos solicitados.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





