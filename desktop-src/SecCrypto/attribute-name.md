---
description: Establece o recupera el nombre de CAPICOM del atributo. Esta es la propiedad predeterminada.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Propiedad Attribute.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f71bb231941765dd073d44abd11c56152ea2d975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670451"
---
# <a name="attributename-property"></a>Propiedad Attribute.Name

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/previous-versions/windows/) .\]

La propiedad **Name** establece o recupera el nombre de CAPICOM del atributo. Esta es la propiedad predeterminada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a>Valor de propiedad

Un valor de la enumeración de [**\_ atributos de CAPICOM**](capicom-attribute.md) que especifica el nombre de CAPICOM del atributo. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                                                 | Significado                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <dt>**\_tiempo de firma de atributo autenticado de CAPICOM \_ \_ \_**</dt> </dl>                         | El atributo contiene la hora a la que se creó la firma.<br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <dt>**\_nombre de documento de atributo autenticado de CAPICOM \_ \_ \_**</dt> </dl>                      | El atributo contiene el nombre del documento firmado.<br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <dt>**\_Descripción del documento de atributo autenticado de CAPICOM \_ \_ \_**</dt> </dl> | El atributo contiene una descripción del documento firmado.<br/>    |



 

## <a name="remarks"></a>Observaciones

Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el estado completo del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributo**](attribute.md)
</dt> </dl>

 

 
