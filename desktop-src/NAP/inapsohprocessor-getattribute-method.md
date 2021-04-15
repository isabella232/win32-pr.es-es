---
title: Método GetAttribute INapSoHProcessor (NapProtocol. h)
description: Recupera el tipo y el valor del atributo, según la ubicación del atributo.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- GetAttribute (método) NAP
- Método GetAttribute NAP, interfaz INapSoHProcessor
- Interfaz INapSoHProcessor NAP, método GetAttribute
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
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676581"
---
# <a name="inapsohprocessorgetattribute-method"></a>INapSoHProcessor:: GetAttribute (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSoHProcessor:: getAttribute** recupera el tipo de atributo y el valor, según la ubicación del atributo.

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

*attributeLocation* \[ de\]
</dt> <dd>

La ubicación (índice) del atributo cuyo tipo y valor se van a recuperar. El valor de *attributeLocation* se devuelve de una llamada anterior a [**INapSoHProcessor:: FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).

</dd> <dt>

*tipo* \[ de enuncia\]
</dt> <dd>

Puntero a una estructura [**SoHAttributeType**](sohattributetype-enum.md) que especifica el tipo del atributo en el *valor*.

</dd> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**SoHAttributeValue**](sohattributevalue-union.md) que contiene el valor del atributo tal y como lo define el *tipo*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





