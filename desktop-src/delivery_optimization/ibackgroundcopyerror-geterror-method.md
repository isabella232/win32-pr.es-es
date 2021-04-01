---
title: Método IBackgroundCopyError GetError (Deliveryoptimization. h)
description: Recupera el código de error e identifica el contexto en el que se produjo el error.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Método GetError
- Método GetError, interfaz IBackgroundCopyError
- Interfaz IBackgroundCopyError, método GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996301"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a>IBackgroundCopyError:: GetError (método)

Recupera el código de error e identifica el contexto en el que se produjo el error.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ enuncia\]
</dt> <dd>

Contexto en el que se produjo el error. Para obtener una lista de valores de contexto, consulte la enumeración [**BG_ERROR_CONTEXT**](bg-error-context.md) .

</dd> <dt>

*pErrorCode* \[ enuncia\]
</dt> <dd>

Código de error del error que se ha producido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de HRESULT de com estándar en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError se define como 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError:: GetFile**](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





