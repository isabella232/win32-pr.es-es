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
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476731"
---
# <a name="settings-object-cryptography"></a>Configuración objeto (criptografía)

\[El **Configuración** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.\]

El **Configuración** se usa para configurar los componentes capicom.

## <a name="members"></a>Miembros

El **Configuración** objeto tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **Configuración** objeto tiene estas propiedades.




| Propiedad | Tipo de acceso | Descripción | 
|----------|-------------|-------------|
| <a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a><br /> | Lectura/escritura<br /> | Establece o recupera la Active Directory de búsqueda. La ubicación inicial no está especificada de forma predeterminada. Cuando la ubicación no se especifica, se busca en el catálogo global y, a continuación, se busca en el dominio predeterminado. La búsqueda determina si el atributo de certificado de usuario se publica en esa ubicación.<br /> | 
| <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a><br /> | Lectura/escritura<br /> | Establece o recupera un valor booleano que indica si la interfaz de usuario solicita la identidad de un firmante o remitente. <br /><blockquote>[!Note]<br />Al establecer esta propiedad no se deshabilitan las advertencias que se generan antes de que se haga cualquier uso de clave privada desde una aplicación basada en web.</blockquote><br /> | 




 

## <a name="remarks"></a>Comentarios

El **Configuración** se puede crear y es seguro para el scripting. El ProgID del **objeto Configuración** es CAPICOM. Configuración.1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 




