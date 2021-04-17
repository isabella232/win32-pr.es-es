---
description: Recupera el estado de validez de la cadena o de un certificado específico de la cadena.
title: 'IChain2:: status (propiedad)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690530"
---
# <a name="ichain2status-property"></a>IChain2:: status (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **status** recupera el estado de validez de la cadena o de un certificado específico de la cadena.

## <a name="syntax"></a>Sintaxis


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Valor de propiedad

Un valor de **tipo Long** que representa el indicador de estado de validez de la cadena o del certificado especificado. En la siguiente tabla se muestran los valores posibles. Esta propiedad contendrá cero si la cadena o el certificado especificado son válidos. De lo contrario, esta propiedad contendrá una combinación de uno o varios de los valores siguientes.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ La \_ confianza \_ no es una \_ hora \_ válida** (&H00000001)


</dt> <dd>

Este certificado o uno de los certificados de la cadena de certificados no es válido en tiempo.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ La \_ confianza \_ no \_ está \_ anidada en tiempo** (&H00000002)


</dt> <dd>

Los certificados de la cadena no están correctamente anidados.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ \_Se \_ revoca la confianza** (&H00000004)


</dt> <dd>

Se ha revocado la confianza de este certificado o de uno de los certificados de la cadena de certificados.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ La \_ confianza \_ no \_ es \_ válida** para la firma (&H00000008)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados no tiene una firma válida.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ La \_ confianza \_ no es \_ válida \_ para el \_ uso** (&H00000010)


</dt> <dd>

El certificado o la cadena de certificados no es válido para su uso propuesto.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ La confianza \_ es una \_ \_ raíz que no es de confianza** (&H00000020)


</dt> <dd>

El certificado o la cadena de certificados se basa en una raíz que no es de confianza.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ \_Estado de REvocación de confianza \_ \_ desconocido** (&H00000040)


</dt> <dd>

Se desconoce el estado de revocación del certificado o uno de los certificados de la cadena de certificados.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ La confianza \_ es \_ cíclica** (&H00000080)


</dt> <dd>

Uno de los certificados de la cadena fue emitido por una [*entidad de certificación*](../secgloss/c-gly.md) que el certificado original había certificado.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ CONFIAR en una \_ \_ extensión no válida** (&H00000100)


</dt> <dd>

Uno de los certificados tiene una extensión no válida.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ CONFIAR en las \_ \_ \_ restricciones de Directiva no válidas** (&H00000200)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de directiva y uno de los certificados emitidos tiene una extensión de asignación de directivas no permitida o no tiene una extensión de directivas de emisión requerida.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ CONFIAR \_ en \_ \_ Restricciones básicas no válidas** (&H00000400)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones básicas y el certificado no se puede usar para emitir otros certificados, o bien se ha superado la longitud de la ruta de acceso de la cadena.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ CONFIAR \_ en \_ \_ restricciones de nombre no válidas** (&H00000800)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre que no es válida.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ La \_ confianza \_ no \_ admite \_ la \_ restricción de nombre** (&H00001000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre que contiene campos no compatibles. No se admiten los campos mínimo y máximo. Por lo tanto, el mínimo debe ser siempre cero y el máximo siempre debe estar ausente. Solo se admite UPN para otro nombre. No se admiten las siguientes opciones de nombre alternativo:

-   Dirección X400
-   Nombre de entidad de EDI
-   ID. registrado

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ La \_ confianza \_ no ha \_ definido una \_ \_ restricción de nombre** (&H00002000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre y falta una restricción de nombre para una de las opciones de nombre del certificado final.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ La \_ confianza \_ no ha \_ permitido la \_ \_ restricción de nombre** (&H00004000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre y no hay una restricción de nombre permitida para una de las opciones de nombre del certificado final.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ La confianza \_ tiene una \_ \_ \_ restricción de nombre excluida** (&H00008000)


</dt> <dd>

El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre, y una de las opciones de nombre del certificado final se excluye explícitamente.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ La \_ confianza \_ es \_ revocación sin conexión** (&H01000000)


</dt> <dd>

El estado de revocación del certificado o uno de los certificados de la cadena de certificados está sin conexión o obsoleto.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ NO confiar en la \_ \_ Directiva de \_ cadena \_ de emisión** (&H02000000)


</dt> <dd>

El certificado final no tiene ninguna directiva de emisión resultante y uno de los certificados de la CA emisora tiene una extensión de restricciones de directivas que lo requiere.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ La confianza \_ es una \_ \_ cadena parcial** (&H00010000)


</dt> <dd>

La cadena de certificados no compite.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ CONFIAR en \_ CTL \_ no es una \_ \_ hora \_ válida** (&H00020000)


</dt> <dd>

Una CTL utilizada para crear esta cadena no era válida.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ La \_ CTL de confianza \_ \_ no es \_ \_ válida** para la firma (&H00040000)


</dt> <dd>

Una CTL utilizada para crear esta cadena no tenía una signatura válida.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ La \_ CTL \_ \_ de confianza no es \_ válida para el \_ \_ uso** (&H00080000)


</dt> <dd>

Una CTL utilizada para crear esta cadena no es válida para este uso.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
