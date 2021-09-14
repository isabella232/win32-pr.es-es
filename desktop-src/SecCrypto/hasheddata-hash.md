---
description: Crea un hash de la cadena especificada.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: Método HashedData.Hash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265388"
---
# <a name="hasheddatahash-method"></a>Método HashedData.Hash

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase HashAlgorithm en**](/previous-versions/windows/) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Hash** crea un hash de la cadena especificada.

## <a name="syntax"></a>Sintaxis


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* 
</dt> <dd>

Cadena que contiene el valor que se debe hash.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para crear el hash de una gran cantidad de datos, llame al **método Hash** para cada fragmento de datos. El hash de cada fragmento de datos se concatena con la [**propiedad Value**](hasheddata-value.md) hasta que se lee la propiedad. El contenido de la **propiedad Value** se restablece cuando se lee la propiedad .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
