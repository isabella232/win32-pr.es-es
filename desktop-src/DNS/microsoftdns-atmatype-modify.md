---
title: Método Modify de la clase MicrosoftDNS_ATMAType
description: El método Modify actualiza un registro de recursos de dirección ATM a nombre (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_ATMAType clase
- MicrosoftDNS_ATMAType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079384"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a>Método Modify de la \_ clase MicrosoftDNS ATMAType

El método **Modify** actualiza un registro de recursos de dirección ATM a nombre (Atma).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ de en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*Formato* \[ en, opcional\]
</dt> <dd>

Formato de dirección ATM. Dos valores posibles para FORMAT son: 0, que indica el formato de dirección del sistema de finalización (AESA) de ATM y 1 que indica el formato E. 164.

</dd> <dt>

*ATMAddress* \[ en, opcional\]
</dt> <dd>

Cadena de longitud variable de octetos que contiene la dirección ATM del nodo/propietario al que pertenece este RR. Los primeros cuatro bytes de la matriz se utilizan para almacenar el tamaño de la cadena de octeto. El byte más significativo se almacena en byte 0.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Referencia al nuevo objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los parámetros no especificados se dejan sin cambios en el registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS ATMAType**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





