---
description: Recupera los datos con hash después de llamar correctamente al método Hash.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: Propiedad HashedData.Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265383"
---
# <a name="hasheddatavalue-property"></a>Propiedad HashedData.Value

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase HashAlgorithm en**](/previous-versions/windows/) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Value** recupera los datos con hash después de llamar correctamente al método [**Hash.**](hasheddata-hash.md) El valor hash se devuelve en formato hexadecimal. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
HashedData.Value As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene los datos con hash en formato hexadecimal.

## <a name="remarks"></a>Observaciones

Para crear el hash de una gran cantidad de datos, llame al [**método Hash**](hasheddata-hash.md) para cada fragmento de datos. El hash de cada fragmento de datos se concatena con la **propiedad Value** hasta que se lee la propiedad. El contenido de la **propiedad Value** se restablece cuando se lee la propiedad .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
