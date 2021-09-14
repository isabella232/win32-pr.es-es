---
description: La propiedad Item recupera un objeto ExtendedProperty de la colección. Esta es la propiedad predeterminada.
ms.assetid: add819e1-6330-483a-8a76-3b7fb8d3f110
title: Propiedad ExtendedProperties.Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 200e36f232c97c1b5a86c8a8a975783469d64a71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173198"
---
# <a name="extendedpropertiesitem-property"></a>Propiedad ExtendedProperties.Item

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use Servicios de invocación de plataforma (PInvoke) para llamar a la función [**certGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) de la API de Win32 y obtener las propiedades. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

La **propiedad Item** recupera un objeto [**ExtendedProperty**](extendedproperty.md) de la colección. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
ExtendedProperties.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**ExtendedProperty**](extendedproperty.md) que representa la propiedad extendida indizada de la colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
