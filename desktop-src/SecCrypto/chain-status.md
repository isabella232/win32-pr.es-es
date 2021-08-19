---
description: Recupera el estado de validez de la cadena o un certificado específico de la cadena.
title: IChain2::Status, propiedad
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
ms.openlocfilehash: 5307d03d340a0a960a5d78226d26e7b5553d27af72f255131651690e5b723355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769555"
---
# <a name="ichain2status-property"></a>IChain2::Status, propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad Status** recupera el estado de validez de la cadena o un certificado específico de la cadena.

## <a name="syntax"></a>Syntax


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Valor de propiedad

Valor **LONG** que representa el indicador de estado de validez de la cadena o el certificado especificado. En la siguiente tabla se muestran los valores posibles. Esta propiedad contendrá cero si la cadena o el certificado especificado son válidos. De lo contrario, esta propiedad contendrá una combinación de uno o varios de los valores siguientes.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ TRUST \_ IS \_ NOT \_ TIME \_ VALID** (&H00000001)


</dt> <dd>

Este certificado o uno de los certificados de la cadena de certificados no es válido en el tiempo.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ LA \_ CONFIANZA NO ESTÁ ANIDADA EN \_ \_ \_ EL** TIEMPO (&H00000002)


</dt> <dd>

Los certificados de la cadena no se anidan correctamente en el tiempo.

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

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ LA \_ CONFIANZA NO ES VÁLIDA PARA \_ \_ \_ \_ EL** USO (&H00000010)


</dt> <dd>

El certificado o la cadena de certificados no es válido para su uso propuesto.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ LA \_ CONFIANZA NO ES UNA \_ \_ RAÍZ** DE CONFIANZA (&H00000020)


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

Uno de los certificados de la cadena lo emitió una entidad [*de certificación*](../secgloss/c-gly.md) que el certificado original había certificado.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ EXTENSIÓN \_ NO \_ VÁLIDA DE** CONFIANZA (&H00000100)


</dt> <dd>

Uno de los certificados tiene una extensión que no es válida.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ CONFIAR \_ EN \_ \_ RESTRICCIONES DE DIRECTIVA NO VÁLIDAS** (&H00000200)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de directiva y uno de los certificados emitidos tiene una extensión de asignación de directivas no permitido o no tiene una extensión de directivas de emisión necesaria.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ CONFIAR \_ EN \_ \_ RESTRICCIONES BÁSICAS NO VÁLIDAS** (&H00000400)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones básicas y el certificado no se puede usar para emitir otros certificados o se ha superado la longitud de la ruta de acceso de cadena.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ CONFIAR \_ EN \_ \_ RESTRICCIONES DE NOMBRE NO VÁLIDAS** (&H00000800)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre que no es válida.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ TRUST \_ NO \_ ADMITE \_ \_ \_ RESTRICCIONES DE NOMBRE** (&H00001000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre que contiene campos no admitidos. No se admiten los campos mínimo y máximo. Por lo tanto, el valor mínimo siempre debe ser cero y el máximo siempre debe estar ausente. Solo se admite UPN para otro nombre. No se admiten las siguientes opciones de nombre alternativo:

-   Dirección X400
-   Nombre de la entidad EDI
-   Id. registrado

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ TRUST \_ NO HA DEFINIDO LA RESTRICCIÓN DE \_ \_ \_ \_ NOMBRE** (&H00002000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre y falta una restricción de nombre para una de las opciones de nombre del certificado final.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ TRUST \_ NO HA PERMITIDO LA RESTRICCIÓN \_ \_ \_ \_ DE** NOMBRE (&H00004000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre y no hay una restricción de nombre permitida para una de las opciones de nombre del certificado final.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ TRUST \_ HA EXCLUIDO LA RESTRICCIÓN \_ \_ \_ NAME** (&H00008000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre y una de las opciones de nombre del certificado final se excluye explícitamente.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ LA \_ CONFIANZA \_ ES \_ REVOCACIÓN SIN** CONEXIÓN (&H01000000)


</dt> <dd>

El estado de revocación del certificado o uno de los certificados de la cadena de certificados es sin conexión o obsoleto.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ DIRECTIVA \_ DE CADENA DE \_ \_ \_ EMISIÓN** DE CONFIANZA SIN (&H02000000)


</dt> <dd>

El certificado final no tiene ninguna directiva de emisión resultante y uno de los certificados de ca emisoras tiene una extensión de restricciones de directiva que lo requiere.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ TRUST \_ ES \_ CADENA \_ PARCIAL** (&H00010000)


</dt> <dd>

La cadena de certificados no compite.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ TRUST \_ CTL \_ NO ES VÁLIDA EN \_ \_ \_ TIEMPO** (&H00020000)


</dt> <dd>

Una CTL usada para crear esta cadena no era válida en el tiempo.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ TRUST \_ CTL \_ NO ES VÁLIDA \_ PARA \_ \_ LA** FIRMA (&H00040000)


</dt> <dd>

Una CTL usada para crear esta cadena no tenía una firma válida.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ TRUST \_ CTL \_ NO ES VÁLIDA PARA EL \_ \_ \_ \_ USO** (&H00080000)


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



 

 
