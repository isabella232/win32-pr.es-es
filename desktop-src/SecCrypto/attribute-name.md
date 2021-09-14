---
description: Establece o recupera el nombre CAPICOM del atributo. Esta es la propiedad predeterminada.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Attribute.Name propiedad
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253533"
---
# <a name="attributename-property"></a>Attribute.Name propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use [**la clase CryptographicAttributeObject en**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) el espacio de nombres [**System.Security.Cryptography.**](/previous-versions/windows/)\]

La **propiedad Name** establece o recupera el nombre CAPICOM del atributo. Esta es la propiedad predeterminada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a>Valor de propiedad

Valor de la [**enumeración CAPICOM \_ ATTRIBUTE**](capicom-attribute.md) que especifica el nombre CAPICOM del atributo. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                                                 | Significado                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <dt>**TIEMPO DE FIRMA \_ DE ATRIBUTOS AUTENTICADOS \_ DE \_ CAPICOM \_**</dt> </dl>                         | El atributo contiene la hora a la que se creó la firma.<br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <dt>**NOMBRE DEL DOCUMENTO DE ATRIBUTO AUTENTICADO CAPICOM \_ \_ \_ \_**</dt> </dl>                      | El atributo contiene el nombre del documento firmado.<br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <dt>**DESCRIPCIÓN DEL DOCUMENTO \_ DE ATRIBUTO AUTENTICADO \_ \_ CAPICOM \_**</dt> </dl> | El atributo contiene una descripción del documento firmado.<br/>    |



 

## <a name="remarks"></a>Observaciones

Cuando se restablece el valor de esta propiedad, directa o indirectamente, se restablece todo el estado del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributo**](attribute.md)
</dt> </dl>

 

 
