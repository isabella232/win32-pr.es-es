---
title: Método AppendAttribute de INapSoHConstructor (NapProtocol.h)
description: Agrega un TLV al final del búfer soH.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Método AppendAttribute NAP
- Método AppendAttribute NAP, interfaz INapSoHConstructor
- INapSoHConstructor interface NAP , AppendAttribute (método)
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7d7ca4636d0eaeea35054dc5330b17f1360dffec5231922ad0acc357231c3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939592"
---
# <a name="inapsohconstructorappendattribute-method"></a>INapSoHConstructor::AppendAttribute (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSoHConstructor::AppendAttribute** agrega un TLV al final del búfer de SoH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* \[ En\]
</dt> <dd>

Enumeración [**SoHAttributeType**](sohattributetype-enum.md) que indica el tipo de atributo del nuevo TLV.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

Puntero a una [**estructura SoHAttributeValue**](sohattributevalue-union.md) que contiene el valor del nuevo TLV.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

El [**TLV sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) no debe agregarse mediante esta función. [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) agrega como el primer TLV a los paquetes SOH recién construidos.

Al anexar un atributo que el sistema Nap consumirá, no debe cifrarse ni modificarse de ninguna manera. Si HealthEntity requiere la comprobación de cifrado o integridad (MAC) de información privada, solo debe incluirse en el atributo [**sohAttributeTypeVendorSpecific.**](sohattributetype-enum.md)

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

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





