---
title: Método SetProperty de IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Establece una propiedad genérica de la transferencia de archivos de optimización de entrega (DO).
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- SetProperty (método)
- Método SetProperty, interfaz IBackgroundCopyFile5
- Interfaz IBackgroundCopyFile5, método SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996299"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a>IBackgroundCopyFile5:: SetProperty (método)

Establece una propiedad genérica de la transferencia de archivos de optimización de entrega (DO).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PropertyId* \[ de\]
</dt> <dd>

Especifica la propiedad que se va a establecer.

</dd> <dt>

*ProertyValue* \[ enuncia\]
</dt> <dd>

Puntero a una Unión que especifica el valor que se va a establecer. Se utiliza el miembro de Unión adecuado para el ID. de propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 se define como 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





