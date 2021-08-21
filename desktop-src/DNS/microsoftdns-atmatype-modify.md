---
title: Método Modify de la MicrosoftDNS_ATMAType clase
description: El método Modify actualiza un registro de recursos de dirección DE ATM a nombre (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Modificación del dns del método
- Modificar el método DNS , MicrosoftDNS_ATMAType clase
- MicrosoftDNS_ATMAType clase DNS , Método Modify
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
ms.openlocfilehash: f3c8f98288c519340e6a95959964a4c42799201c7e1701bb748f634746a94226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163763"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a>Método Modify de la clase ATMAType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos de dirección DE ATM a nombre (ATMA).

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

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*Formato* \[ en, opcional\]
</dt> <dd>

Formato de dirección ATM. Dos valores posibles para FORMAT son: 0 que indica el formato de dirección del sistema de finalización de ATM (AESA) y 1 que indica el formato E.164.

</dd> <dt>

*ATMAddress* \[ en, opcional\]
</dt> <dd>

Cadena de longitud variable de octetos que contiene la dirección ATM del nodo o propietario al que pertenece este RR. Los cuatro primeros bytes de la matriz se usan para almacenar el tamaño de la cadena de octeto. El byte más significativo se almacena en byte 0.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referencia al nuevo objeto .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cualquier parámetro no especificado se deja sin modificar en el registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase \_ ATMAType de MicrosoftDNS**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





