---
description: Representa un único atributo autenticado.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute, objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c3e07c771a34e89cfbcbba5695450e195ef55482e0a27bee008f3ea8251bf8bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879875"
---
# <a name="attribute-object"></a>Attribute, objeto

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use [**la clase CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio [**de nombres System.Security.Cryptography.**](/previous-versions/windows/)\]

El **objeto Attribute** representa un único atributo autenticado.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto Attribute** se usa para realizar las siguientes tareas:

-   Establezca o recupere el nombre CAPICOM del atributo.
-   Establezca o recupere el valor del atributo, como la hora de firma, el nombre del documento firmado o una descripción del documento firmado.

## <a name="members"></a>Miembros

El **objeto Attribute** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Attribute** tiene estas propiedades.



| Propiedad                                    | Tipo de acceso           | Descripción                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Nombre**](attribute-name.md)<br/>   | Lectura/escritura<br/> | Establece o recupera el nombre CAPICOM del atributo. Esta es la propiedad predeterminada.<br/> |
| [**Value**](attribute-value.md)<br/> | Lectura/escritura<br/> | Establece o recupera el valor del atributo.<br/>                                      |



 

## <a name="remarks"></a>Comentarios

Se **puede crear** el objeto Attribute y es seguro para el scripting. El ProgID del **objeto Attribute** es CAPICOM. Attribute.1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
