---
title: Método INapSoHProcessor GetAttribute (NapProtocol.h)
description: Recupera el tipo de atributo y el valor, dada la ubicación del atributo.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- Nap del método GetAttribute
- Método Nap de GetAttribute, interfaz INapSoHProcessor
- Nap de interfaz INapSoHProcessor, método GetAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba1b86ca1eab51fdca382a758a9a65650af2249eb0d605c24274c84d1f95669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939572"
---
# <a name="inapsohprocessorgetattribute-method"></a>INapSoHProcessor::GetAttribute (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSoHProcessor::GetAttribute** recupera el tipo de atributo y el valor, dada la ubicación del atributo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*attributeLocation* \[ En\]
</dt> <dd>

Ubicación (índice) del atributo cuyo tipo y valor se van a recuperar. El valor de *attributeLocation* se devuelve de una llamada anterior a [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).

</dd> <dt>

*type* \[ out\]
</dt> <dd>

Puntero a una [**estructura SoHAttributeType**](sohattributetype-enum.md) que especifica el tipo del atributo en *el valor*.

</dd> <dt>

*value* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura SoHAttributeValue**](sohattributevalue-union.md) que contiene el valor del atributo definido por *el tipo*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





