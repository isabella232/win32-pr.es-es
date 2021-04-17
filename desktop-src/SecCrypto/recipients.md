---
description: Representa una colección de objetos de certificado.
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
ms.openlocfilehash: c68ca0217631970f35680160b71841f758b13fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689975"
---
# <a name="recipients-object"></a>Objeto Recipients

\[El objeto **Recipients** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El objeto **Recipients** representa una colección de objetos de [**certificado**](certificate.md) . Cada objeto representa un destinatario previsto del mensaje con doble cifrado. Los datos de un objeto [**EnvelopedData**](envelopeddata.md) se cifran con una clave de sesión [*simétrica*](../secgloss/s-gly.md) y esa clave de sesión simétrica se cifra a su vez para cada destinatario mediante la clave pública del certificado del destinatario previsto. Un destinatario con acceso a la [*clave privada*](../secgloss/p-gly.md) asociada a la [*clave pública*](../secgloss/p-gly.md) de un certificado puede descifrar la [*clave de sesión*](../secgloss/s-gly.md) y usar la clave de sesión descifrada para descifrar los datos reales.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **Recipients** se usa para realizar las siguientes tareas:

-   Agregue o quite un objeto de [**certificado**](certificate.md) de la colección.
-   Recupere el número de certificados de la colección.
-   Recupera un objeto de **destinatarios** específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El objeto **Recipients** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **Recipients** tiene estos métodos.



| Método                              | Descripción                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [**Agréguela**](recipients-add.md)       | Agrega un objeto de [**certificado**](certificate.md) a la colección.<br/>         |
| [**Claridad**](recipients-clear.md)   | Quita todos los objetos de [**certificado**](certificate.md) de la colección.<br/> |
| [**Retirar**](recipients-remove.md) | Quita un objeto de [**certificado**](certificate.md) de la colección.<br/>    |



 

### <a name="properties"></a>Propiedades

El objeto **Recipients** tiene estas propiedades.



| Propiedad                                           | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](recipients-newenum.md)<br/> | Solo lectura<br/> | Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contabiliza**](recipients-count.md)<br/>       |                      | El número de objetos de la colección de **destinatarios** .<br/>                                                                                                                                                              |
| [**Elemento**](recipients-item.md)<br/>         |                      | Objeto indizado en la colección. Esta es la propiedad predeterminada.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **Recipients** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
