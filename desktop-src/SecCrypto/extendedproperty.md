---
description: Representa una propiedad extendida de Microsoft.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: Objeto ExtendedProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671041"
---
# <a name="extendedproperty-object"></a>Objeto ExtendedProperty

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a la función de la API de Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y obtener las propiedades. Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

El objeto **ExtendedProperty** representa una propiedad extendida de Microsoft.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **ExtendedProperty** se usa para realizar las siguientes tareas:

-   Establezca o recupere el tipo de la propiedad extendida.
-   Establece o recupera el tipo de codificación utilizado para codificar la propiedad extendida.

## <a name="members"></a>Miembros

El objeto **ExtendedProperty** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **ExtendedProperty** tiene estas propiedades.



| Propiedad                                             | Tipo de acceso           | Descripción                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PropID**](extendedproperty-propid.md)<br/> | Lectura/escritura<br/> | Un valor de la enumeración de [**CAPICOM \_ PROPID**](capicom-propid.md) que establece o recupera el tipo de propiedad extendida.<br/> Esta es la propiedad predeterminada.<br/> |
| [**Value**](extendedproperty-value.md)<br/>   | Lectura/escritura<br/> | Un valor de la enumeración de [**\_ \_ tipo de codificación CAPICOM**](capicom-encoding-type.md) que establece o recupera los datos de la propiedad extendida.<br/>                              |



 

## <a name="remarks"></a>Observaciones

La colección [**ExtendedProperties**](extendedproperties.md) usa el objeto **ExtendedProperty** .

Se puede crear el objeto **ExtendedProperty** y no es seguro para el scripting. El ProgID del objeto **ExtendedProperty** es CAPICOM. ExtendedProperty. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
