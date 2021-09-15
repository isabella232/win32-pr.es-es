---
description: Recupera el estado de validez de la cadena o de un certificado específico de la cadena.
title: Propiedad IChain2::Status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23673289e2ff39d4180a4be8dc0be61f4a5cffc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271148"
---
# <a name="ichain2status-property"></a>Propiedad IChain2::Status

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad Status** recupera el estado de validez de la cadena o un certificado específico de la cadena.

## <a name="syntax"></a>Sintaxis


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Valor de propiedad

Valor **LONG** que representa el indicador de estado de validez de la cadena o el certificado especificado. En la siguiente tabla se muestran los valores posibles. Esta propiedad contendrá cero si la cadena o el certificado especificado son válidos. De lo contrario, esta propiedad contendrá una combinación de uno o varios de los valores siguientes.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ TRUST \_ NO ES VÁLIDO EN \_ \_ \_ TIEMPO** (&H00000001)


</dt> <dd>

Este certificado o uno de los certificados de la cadena de certificados no es válido en el tiempo.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ TRUST \_ NO ESTÁ ANIDADA EN EL \_ \_ \_ TIEMPO** (&H00000002)


</dt> <dd>

Los certificados de la cadena no se anidan correctamente.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ SE \_ REVOCA \_ LA CONFIANZA** (&H00000004)


</dt> <dd>

Se ha revocado la confianza para este certificado o uno de los certificados de la cadena de certificados.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ TRUST \_ NO ES VÁLIDA PARA \_ \_ \_ FIRMA** (&H00000008)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados no tiene una firma válida.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ TRUST \_ NO ES VÁLIDO PARA EL \_ \_ \_ \_ USO** (&H00000010)


</dt> <dd>

La cadena de certificados o certificados no es válida para su uso propuesto.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ TRUST \_ ES UNA RAÍZ \_ \_ QUE** NO ES DE CONFIANZA (&H00000020)


</dt> <dd>

La cadena de certificados o certificados se basa en una raíz que no es de confianza.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ ESTADO \_ DE \_ REVOCACIÓN DE CONFIANZA \_ DESCONOCIDO** (&H00000040)


</dt> <dd>

Se desconoce el estado de revocación del certificado o uno de los certificados de la cadena de certificados.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ TRUST \_ IS \_ CYCLIC** (&H00000080)


</dt> <dd>

Una entidad de certificación emitió uno de los certificados de la cadena [*que*](../secgloss/c-gly.md) el certificado original había certificado.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ TRUST \_ INVALID \_ EXTENSION** (&H00000100)


</dt> <dd>

Uno de los certificados tiene una extensión que no es válida.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ CONFIAR \_ EN \_ \_ RESTRICCIONES DE DIRECTIVA NO VÁLIDAS** (&H00000200)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de directiva y uno de los certificados emitidos tiene una extensión de asignación de directivas no permitido o no tiene una extensión de directivas de emisión necesaria.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ \_RESTRICCIONES \_ \_ BÁSICAS NO VÁLIDAS** DE CONFIANZA (&H00000400)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones básicas y el certificado no se puede usar para emitir otros certificados o se ha superado la longitud de la ruta de acceso de la cadena.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ RESTRICCIONES \_ DE NOMBRE NO VÁLIDO \_ \_ DE** CONFIANZA (&H00000800)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre que no es válida.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ TRUST \_ NO ADMITE LA RESTRICCIÓN \_ \_ \_ \_ NAME** (&H00001000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre que contiene campos no admitidos. No se admiten los campos mínimo y máximo. Por lo tanto, el valor mínimo siempre debe ser cero y el máximo siempre debe estar ausente. Solo se admite UPN para otro nombre. No se admiten las siguientes opciones de nombre alternativas:

-   Dirección X400
-   Nombre de la entidad EDI
-   Id. registrado

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ TRUST \_ NO HA DEFINIDO LA RESTRICCIÓN \_ \_ \_ NAME \_** (&H00002000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre y falta una restricción de nombre para una de las opciones de nombre del certificado final.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ TRUST \_ NO HA PERMITIDO LA RESTRICCIÓN \_ \_ \_ \_ NAME** (&H00004000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre y no hay una restricción de nombre permitida para una de las opciones de nombre del certificado final.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ TRUST \_ HA EXCLUIDO LA RESTRICCIÓN \_ \_ NAME \_** (&H00008000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre y una de las opciones de nombre del certificado final se excluye explícitamente.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ TRUST \_ ES \_ \_ REVOCACIÓN SIN** CONEXIÓN (&H01000000)


</dt> <dd>

El estado de revocación del certificado o uno de los certificados de la cadena de certificados es sin conexión o obsoleto.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ TRUST \_ NO \_ ISSUANCE \_ CHAIN \_ POLICY** (&H02000000)


</dt> <dd>

El certificado final no tiene ninguna directiva de emisión resultante y uno de los certificados de ca emisora tiene una extensión de restricciones de directiva que lo requiere.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ TRUST \_ ES \_ CADENA \_ PARCIAL** (&H00010000)


</dt> <dd>

La cadena de certificados no compite.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ LA \_ CTL \_ DE CONFIANZA NO ES VÁLIDA EN \_ \_ \_ TIEMPO** (&H00020000)


</dt> <dd>

Una CTL usada para crear esta cadena no era válida a la hora.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ TRUST \_ CTL \_ NO ES VÁLIDA \_ PARA \_ LA \_** FIRMA (&H00040000)


</dt> <dd>

Una CTL usada para crear esta cadena no tenía una firma válida.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ TRUST \_ CTL \_ NO ES VÁLIDA PARA \_ \_ \_ \_ USO** (&H00080000)


</dt> <dd>

Una CTL usada para crear esta cadena no es válida para este uso.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
