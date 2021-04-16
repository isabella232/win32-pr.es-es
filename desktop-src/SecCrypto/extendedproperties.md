---
description: Representa una colección de objetos ExtendedProperty.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: ExtendedProperties (objeto)
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
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649907"
---
# <a name="extendedproperties-object"></a>ExtendedProperties (objeto)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a la función de la API de Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y obtener las propiedades. Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

El objeto **ExtendedProperties** representa una colección de objetos [**ExtendedProperty**](extendedproperty.md) . Cada objeto representa una única propiedad extendida.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **ExtendedProperties** se usa para realizar las siguientes tareas:

-   Agregue o quite un objeto [**ExtendedProperty**](extendedproperty.md) de la colección.
-   Recupere el número de propiedades extendidas de la colección.
-   Recupera un objeto [**ExtendedProperty**](extendedproperty.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El objeto **ExtendedProperties** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#extendedproperties-object)

### <a name="methods"></a>Métodos

El objeto **ExtendedProperties** tiene estos métodos.



| Método                                      | Descripción                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Agréguela**](extendedproperties-add.md)       | Agrega un objeto [**ExtendedProperty**](extendedproperty.md) a la colección.<br/>      |
| [**Retirar**](extendedproperties-remove.md) | Quita un objeto [**ExtendedProperty**](extendedproperty.md) de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **ExtendedProperties** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extendedproperties-newenum.md)<br/> | Solo lectura<br/> | Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contabiliza**](extendedproperties-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos [**ExtendedProperty**](extendedproperty.md) de la colección.<br/>                                                                                                                      |
| [**Elemento**](extendedproperties-item.md)<br/>         | Solo lectura<br/> | Recupera un objeto [**ExtendedProperty**](extendedproperty.md) que representa la propiedad extendida indizada de la colección. Esta es la propiedad predeterminada.<br/>                                                      |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **ExtendedProperties** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
