---
description: 'Método IEnumPStoreItems::Clone: crea otro enumerador que contiene el mismo estado de enumeración que el actual.'
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: Método IEnumPStoreItems::Clone (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 29b618881305296a560dc9102f7571c08236d1bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089333"
---
# <a name="ienumpstoreitemsclone-method"></a>IEnumPStoreItems::Clone (Método)

\[El almacenamiento protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Crea otro enumerador que contiene el mismo estado de enumeración que el actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*laum* \[ out\]
</dt> <dd>

Puntero a un [**puntero IEnumPStoreItems.**](ienumpstoreitems.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> </dl>

 

 
