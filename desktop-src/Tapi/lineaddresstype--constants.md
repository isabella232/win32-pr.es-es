---
description: El tipo de dirección identifica el formato de dirección, como el número de teléfono estándar o la dirección de correo electrónico. Solo las aplicaciones que negocian TAPI versión 3.0 o posterior pueden usar tipos de direcciones.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: LINEADDRESSTYPE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0a46eff2a7a0c38fa17aed4b831ef8701c565
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249992"
---
# <a name="lineaddresstype_-constants"></a>Constantes \_ LINEADDRESSTYPE

El tipo de dirección identifica el formato de dirección, como el número de teléfono estándar o la dirección de correo electrónico. Solo las aplicaciones que negocian TAPI versión 3.0 o posterior pueden usar tipos de direcciones.

<dl> <dt>

<span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE \_ PHONENUMBER**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



El tipo de dirección es un número de teléfono estándar.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE \_ SDP**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



El tipo de dirección es la conferencia del Protocolo de descripción de sesión (SDP).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EMAILNAME**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



El tipo de dirección es un nombre de correo electrónico.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ DOMAINNAME**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



El tipo de dirección es un nombre de dominio.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE \_ IPADDRESS**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



El tipo de dirección es una dirección IP.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




