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
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473764"
---
# <a name="inapsohconstructorappendattribute-method"></a>INapSoHConstructor::AppendAttribute (Método)

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



 

## <a name="remarks"></a>Observaciones

El [**TLV sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) no debe agregarse mediante esta función. [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) agrega como primer TLV a paquetes SOH recién construidos.

Al anexar un atributo que el sistema Nap consumirá, no debe cifrarse ni modificarse de ninguna manera. Si HealthEntity requiere la comprobación de cifrado o integridad (MAC) de información privada, solo debe incluirse en el atributo [**sohAttributeTypeVendorSpecific.**](sohattributetype-enum.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





