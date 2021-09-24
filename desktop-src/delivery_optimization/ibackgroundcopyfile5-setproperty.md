---
title: Método IBackgroundCopyFile5 SetProperty (Deliveryoptimization.h)
description: Establece una propiedad genérica de una Optimización de distribución de archivos.
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
ms.openlocfilehash: 4730625c702ee2554b43dd96730287b0322c6f28
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520128"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a>IBackgroundCopyFile5::SetProperty (Método)

Establece una propiedad genérica de una Optimización de distribución de archivos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PropertyId* \[ En\]
</dt> <dd>

Especifica la propiedad que se va a establecer.

</dd> <dt>

*ProertyValue* \[ out\]
</dt> <dd>

Puntero a una unión que especifica el valor que se va a establecer. Se usa el miembro de unión adecuado para el identificador de propiedad.

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

[**IBackgroundCopyFile5.GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





