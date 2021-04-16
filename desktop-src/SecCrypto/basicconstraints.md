---
description: Representa la extensión de restricciones básicas de un certificado.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Objeto BasicConstraints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671411"
---
# <a name="basicconstraints-object"></a>Objeto BasicConstraints

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

El objeto **BasicConstraints** representa la extensión de restricciones básicas de un certificado.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **BasicConstraints** se usa para realizar las siguientes tareas:

-   Determine si la extensión de restricciones básicas está presente.
-   Determine si la extensión de restricciones básicas está marcada como crítica.
-   Determine si el certificado está restringido a las entidades de certificación.
-   Determine si la restricción de longitud de ruta de acceso está presente y recupere el valor de la restricción de longitud de ruta de acceso.

## <a name="members"></a>Miembros

El objeto **BasicConstraints** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **BasicConstraints** tiene estas propiedades.



| Propiedad                                                                                     | Tipo de acceso          | Descripción                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCertificateAuthority**](basicconstraints-iscertificateauthority.md)<br/>         | Solo lectura<br/> | Recupera un valor booleano que indica si el certificado es para una [*entidad de certificación*](../secgloss/c-gly.md) (CA).<br/> |
| [**IsCritical**](basicconstraints-iscritical.md)<br/>                                 | Solo lectura<br/> | Recupera un valor booleano que indica si la extensión de restricción básica está marcada como crítica.<br/>                                                                                                     |
| [**IsPathLenConstraintPresent**](basicconstraints-ispathlenconstraintpresent.md)<br/> | Solo lectura<br/> | Recupera un valor booleano que indica si la restricción de longitud de ruta de acceso del certificado está presente.<br/>                                                                                                   |
| [**IsPresent**](basicconstraints-ispresent.md)<br/>                                   | Solo lectura<br/> | Recupera un valor booleano que indica si la extensión de restricciones básicas está presente. Esta es la propiedad predeterminada.<br/>                                                                              |
| [**PathLenConstraint**](basicconstraints-pathlenconstraint.md)<br/>                   | Solo lectura<br/> | Recupera el valor de la restricción de longitud de ruta de acceso.<br/>                                                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **BasicConstraints** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de criptografía](cryptography-objects.md)
</dt> </dl>

 

 
