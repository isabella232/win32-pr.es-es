---
description: Representa una colección de objetos Attribute.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Objeto Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253490"
---
# <a name="attributes-object"></a>Objeto Attributes

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use [**la clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el [**espacio de nombres System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **objeto Attributes** representa una colección de objetos [**Attribute.**](attribute.md) Cada [**objeto Attribute**](attribute.md) representa un único atributo de un mensaje.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto Attributes** se usa para realizar las tareas siguientes:

-   Agregue o quite un objeto [**Attribute**](attribute.md) específico de la colección.
-   Borre la colección.
-   Recupere el número de atributos de la colección.
-   Recupere un objeto [**Attribute**](attribute.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Members

El **objeto Attributes** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Attributes** tiene estos métodos.



| Método                              | Descripción                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**Añadir**](attributes-add.md)       | Agrega un [**objeto Attribute**](attribute.md) a la colección.<br/>       |
| [**Borrar**](attributes-clear.md)   | Borra todos los [**objetos Attribute**](attribute.md) de la colección.<br/> |
| [**Remove**](attributes-remove.md) | Quita un [**objeto Attribute**](attribute.md) de la colección.<br/>  |



 

### <a name="properties"></a>Propiedades

El **objeto Attributes** tiene estas propiedades.



| Propiedad                                           | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](attributes-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Recuento**](attributes-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos [**Attribute**](attribute.md) de la colección.<br/>                                                                                                                                    |
| [**Elemento**](attributes-item.md)<br/>         | Solo lectura<br/> | Recupera el [**objeto Attribute**](attribute.md) que representa el atributo indexado. Esta es la propiedad predeterminada.<br/>                                                                                             |



 

## <a name="remarks"></a>Observaciones

No **se puede** crear el objeto Attributes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de criptografía](cryptography-objects.md)
</dt> </dl>

 

 
