---
description: Representa una colección de objetos ExtendedProperty.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: Objeto ExtendedProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0225582217df56f486a44f12e3ca6ea0003130fdb209fb67e9f9e4ee258764d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007243"
---
# <a name="extendedproperties-object"></a>Objeto ExtendedProperties

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use Servicios de invocación de plataforma (PInvoke) para llamar a la función [**certGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) de la API de Win32 y obtener las propiedades. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

El **objeto ExtendedProperties** representa una colección de [**objetos ExtendedProperty.**](extendedproperty.md) Cada objeto representa una sola propiedad extendida.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto ExtendedProperties** se usa para realizar las siguientes tareas:

-   Agregue o quite un [**objeto ExtendedProperty**](extendedproperty.md) de la colección.
-   Recupere el número de propiedades extendidas de la colección.
-   Recupera un objeto [**ExtendedProperty**](extendedproperty.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El **objeto ExtendedProperties** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#extendedproperties-object)

### <a name="methods"></a>Métodos

El **objeto ExtendedProperties** tiene estos métodos.



| Método                                      | Descripción                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Añadir**](extendedproperties-add.md)       | Agrega un [**objeto ExtendedProperty**](extendedproperty.md) a la colección.<br/>      |
| [**Quitar**](extendedproperties-remove.md) | Quita un [**objeto ExtendedProperty**](extendedproperty.md) de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto ExtendedProperties** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extendedproperties-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](extendedproperties-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos [**ExtendedProperty**](extendedproperty.md) de la colección.<br/>                                                                                                                      |
| [**Elemento**](extendedproperties-item.md)<br/>         | Solo lectura<br/> | Recupera un objeto [**ExtendedProperty**](extendedproperty.md) que representa la propiedad extendida indizada de la colección. Esta es la propiedad predeterminada.<br/>                                                      |



 

## <a name="remarks"></a>Comentarios

No se puede crear el objeto **ExtendedProperties.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
