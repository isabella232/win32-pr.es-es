---
title: Método IBackgroundCopyFile5 GetProperty (Deliveryoptimization.h)
description: Obtiene una propiedad genérica de una Optimización de distribución de archivos.
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- Método GetProperty
- Método GetProperty, interfaz IBackgroundCopyFile5
- Interfaz IBackgroundCopyFile5, método GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d22e9af42cbb5b6534e27646ed1e038cca5e1169
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128519865"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a>IBackgroundCopyFile5::GetProperty (método)

Obtiene una propiedad genérica de una Optimización de distribución de archivos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PropertyId* \[ En\]
</dt> <dd>

Especifica la propiedad de archivo cuyo valor se va a recuperar.

</dd> <dt>

*PropertyValue* \[ out\]
</dt> <dd>

Valor de propiedad, devuelto como puntero a una BITS_FILE_PROPERTY_VALUE unión. Use el campo union adecuado para el valor de id. de propiedad pasado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 se define como 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5.SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





