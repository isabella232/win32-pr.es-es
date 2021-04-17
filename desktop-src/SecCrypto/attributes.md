---
description: Representa una colección de objetos de atributo.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attributes (objeto)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670682"
---
# <a name="attributes-object"></a>Attributes (objeto)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El objeto **attributes** representa una colección de objetos de [**atributo**](attribute.md) . Cada objeto de [**atributo**](attribute.md) representa un atributo único de un mensaje.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **attributes** se usa para realizar las siguientes tareas:

-   Agregue o quite un objeto de [**atributo**](attribute.md) específico de la colección.
-   Borre la colección.
-   Recupere el número de atributos de la colección.
-   Recupera un objeto de [**atributo**](attribute.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El objeto **attributes** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **attributes** tiene estos métodos.



| Método                              | Descripción                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**Agréguela**](attributes-add.md)       | Agrega un objeto de [**atributo**](attribute.md) a la colección.<br/>       |
| [**Claridad**](attributes-clear.md)   | Borra todos los objetos de [**atributo**](attribute.md) de la colección.<br/> |
| [**Retirar**](attributes-remove.md) | Quita un objeto de [**atributo**](attribute.md) de la colección.<br/>  |



 

### <a name="properties"></a>Propiedades

El objeto **attributes** tiene estas propiedades.



| Propiedad                                           | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](attributes-newenum.md)<br/> | Solo lectura<br/> | Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contabiliza**](attributes-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos de [**atributo**](attribute.md) de la colección.<br/>                                                                                                                                    |
| [**Elemento**](attributes-item.md)<br/>         | Solo lectura<br/> | Recupera el objeto de [**atributo**](attribute.md) que representa el atributo indizado. Esta es la propiedad predeterminada.<br/>                                                                                             |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **attributes** .

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

 

 
