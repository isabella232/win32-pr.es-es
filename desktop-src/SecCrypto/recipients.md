---
description: 'Objeto Recipients: representa una colección de objetos Certificate.'
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Objeto Recipients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0f0f6474c6ed8883eb591591eff387fe387f7d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103743"
---
# <a name="recipients-object"></a>Objeto Recipients

\[El **objeto Recipients** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **objeto Recipients** representa una colección de [**objetos Certificate.**](certificate.md) Cada objeto representa un destinatario previsto del mensaje con sobres. Los datos de un objeto [**EnvelopedData**](envelopeddata.md) se cifran con una clave de sesión simétrica y, [*a*](../secgloss/s-gly.md) continuación, esa clave de sesión simétrica se cifra para cada destinatario mediante el uso de la clave pública del certificado de ese destinatario previsto. Un destinatario con acceso a la clave [](../secgloss/p-gly.md) privada asociada a [](../secgloss/s-gly.md) la clave pública de un certificado puede descifrar la clave de sesión y usar la clave de sesión descifrada para descifrar los datos reales. [](../secgloss/p-gly.md)

## <a name="when-to-use"></a>Cuándo se usa

El **objeto Recipients** se usa para realizar las siguientes tareas:

-   Agregue o quite un [**objeto Certificate**](certificate.md) de la colección.
-   Recupere el número de certificados de la colección.
-   Recuperar un objeto **Recipients** específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El **objeto Recipients** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Recipients** tiene estos métodos.



| Método                              | Descripción                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [**Añadir**](recipients-add.md)       | Agrega un [**objeto Certificate**](certificate.md) a la colección.<br/>         |
| [**Borrar**](recipients-clear.md)   | Quita todos los [**objetos Certificate**](certificate.md) de la colección.<br/> |
| [**Quitar**](recipients-remove.md) | Quita un [**objeto Certificate**](certificate.md) de la colección.<br/>    |



 

### <a name="properties"></a>Propiedades

El **objeto Recipients** tiene estas propiedades.



| Propiedad                                           | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](recipients-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](recipients-count.md)<br/>       |                      | Número de objetos de la **colección Recipients.**<br/>                                                                                                                                                              |
| [**Elemento**](recipients-item.md)<br/>         |                      | Objeto indexado de la colección. Esta es la propiedad predeterminada.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Comentarios

No **se puede crear** el objeto Recipients.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
