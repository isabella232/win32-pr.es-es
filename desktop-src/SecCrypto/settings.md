---
description: Se utiliza para configurar los componentes de CAPICOM.
title: Objeto de configuración
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
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690588"
---
# <a name="settings-object-cryptography"></a>Objeto de configuración (criptografía)

\[El objeto de **configuración** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]

El objeto de **configuración** se utiliza para configurar los componentes de CAPICOM.

## <a name="members"></a>Miembros

El objeto de **configuración** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto de **configuración** tiene estas propiedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propiedad</th>
<th style="text-align: left;">Tipo de acceso</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Establece o recupera la ubicación de búsqueda de Active Directory. La ubicación inicial no se especifica de forma predeterminada. Cuando no se especifica la ubicación, se busca en el catálogo global y, a continuación, se busca en el dominio predeterminado. La búsqueda determina si el atributo de certificado de usuario está publicado en esa ubicación.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Establece o recupera un valor booleano que indica si se pueden usar los mensajes de la interfaz de usuario para el firmante o la identidad de un remitente. <br/>
<blockquote>
[!Note]<br />
Al establecer esta propiedad, no se deshabilitan las advertencias generadas antes de que se realice un uso de clave privada desde una aplicación basada en Web.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto de **configuración** y es seguro para el scripting. El ProgID del objeto de **configuración** es CAPICOM. Configuración. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 




