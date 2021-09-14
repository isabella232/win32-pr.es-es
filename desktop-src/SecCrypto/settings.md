---
description: Se usa para configurar componentes CAPICOM.
title: Configuración objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aaeff4c8b65a68938bfab641aceb68fe4efb6334
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160727"
---
# <a name="settings-object-cryptography"></a>Configuración (criptografía)

\[El **Configuración** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.\]

El **Configuración** se usa para configurar componentes capicom.

## <a name="members"></a>Members

El **Configuración** objeto tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **Configuración** objeto tiene estas propiedades.




| Propiedad | Tipo de acceso | Descripción | 
|----------|-------------|-------------|
| <a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a><br /> | Lectura y escritura<br /> | Establece o recupera la Active Directory de búsqueda. La ubicación inicial no está especificada de forma predeterminada. Cuando la ubicación no se especifica, se busca en el catálogo global y, a continuación, se busca en el dominio predeterminado. La búsqueda determina si el atributo de certificado de usuario se publica en esa ubicación.<br /> | 
| <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a><br /> | Lectura y escritura<br /> | Establece o recupera un valor booleano que indica si la interfaz de usuario solicita la identidad de un firmante o remitente. <br /><blockquote>[!Note]<br />Al establecer esta propiedad no se deshabilitan las advertencias que se generan antes de que se haga cualquier uso de clave privada desde una aplicación basada en web.</blockquote><br /> | 




 

## <a name="remarks"></a>Observaciones

El **Configuración** se puede crear y es seguro para el scripting. El ProgID del **objeto Configuración** es CAPICOM. Configuración.1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 




