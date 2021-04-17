---
title: Método INapSoHConstructor AppendAttribute (NapProtocol. h)
description: Agrega un TLV al final del búfer de SoH.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Método AppendAttribute NAP
- Método AppendAttribute NAP, interfaz INapSoHConstructor
- Interfaz INapSoHConstructor NAP, método AppendAttribute
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534095"
---
# <a name="inapsohconstructorappendattribute-method"></a>INapSoHConstructor:: AppendAttribute (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSoHConstructor:: AppendAttribute** agrega un TLV al final del búfer de SOH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo* \[ de de\]
</dt> <dd>

Una enumeración [**SoHAttributeType**](sohattributetype-enum.md) que indica el tipo de atributo del nuevo TLV.

</dd> <dt>

*valor* \[ de de\]
</dt> <dd>

Puntero a una estructura [**SoHAttributeValue**](sohattributevalue-union.md) que contiene el valor para el nuevo TLV.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

El TLV [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) no debe agregarse mediante esta función. Se agrega como primer TLV de [**INapSoHConstructor:: Initialize**](inapsohconstructor-initialize-method.md) a paquetes SOH recién construidos.

Al anexar un atributo que utilizará el sistema NAP, no debe cifrarse ni modificarse de ninguna manera. Si el HealthEntity requiere la comprobación de la integridad y el cifrado (MACs) de la información privada, solo debe incluirse en el atributo [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) .

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

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





