---
description: Representa una propiedad extendida por Microsoft.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: ExtendedProperty, objeto
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171038"
---
# <a name="extendedproperty-object"></a>ExtendedProperty, objeto

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use Servicios de invocación de plataforma (PInvoke) para llamar a la función [**certGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) de la API de Win32 y obtener las propiedades. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

El **objeto ExtendedProperty** representa una propiedad extendida por Microsoft.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto ExtendedProperty** se usa para realizar las siguientes tareas:

-   Establezca o recupere el tipo de la propiedad extendida.
-   Establezca o recupere el tipo de codificación utilizado para codificar la propiedad extendida.

## <a name="members"></a>Members

El **objeto ExtendedProperty** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto ExtendedProperty** tiene estas propiedades.



| Propiedad                                             | Tipo de acceso           | Descripción                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PropID**](extendedproperty-propid.md)<br/> | Lectura y escritura<br/> | Valor de la [**enumeración CAPICOM \_ PROPID**](capicom-propid.md) que establece o recupera el tipo de propiedad extendida.<br/> Esta es la propiedad predeterminada.<br/> |
| [**Value**](extendedproperty-value.md)<br/>   | Lectura y escritura<br/> | Valor de la enumeración [**\_ CAPICOM ENCODING \_ TYPE**](capicom-encoding-type.md) que establece o recupera los datos de propiedad extendida.<br/>                              |



 

## <a name="remarks"></a>Observaciones

La colección [**ExtendedProperties**](extendedproperties.md) usa el objeto **ExtendedProperty.**

El **objeto ExtendedProperty** se puede crear y no es seguro para el scripting. El ProgID del **objeto ExtendedProperty** es CAPICOM. ExtendedProperty.1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
