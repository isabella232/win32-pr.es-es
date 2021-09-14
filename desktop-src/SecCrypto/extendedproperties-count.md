---
description: Recupera el número de objetos ExtendedProperty de la colección.
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: Propiedad ExtendedProperties.Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d4370f7ce5fc215d18b0940d3dbc2edc221af536
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173209"
---
# <a name="extendedpropertiescount-property"></a>Propiedad ExtendedProperties.Count

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use Platform Invocation Services (PInvoke) para llamar a la función de API [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) de Win32 y obtener las propiedades. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

La **propiedad Count** recupera el número de objetos [**ExtendedProperty**](extendedproperty.md) de la colección.

## <a name="syntax"></a>Sintaxis


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de objetos [**ExtendedProperty**](extendedproperty.md) de la colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
