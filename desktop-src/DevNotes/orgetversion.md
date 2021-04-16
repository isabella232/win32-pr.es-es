---
description: Esta función recupera la versión de la biblioteca del registro sin conexión.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: Función ORGetVersion (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649849"
---
# <a name="orgetversion-function"></a>ORGetVersion función)

Esta función recupera la versión de la biblioteca del registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwMajorVersion* \[ enuncia\]
</dt> <dd>

Un puntero a una variable para recibir la versión principal de la biblioteca del registro sin conexión. Para la versión inicial de la biblioteca, el valor es 1.

</dd> <dt>

*pdwMinorVersion* \[ enuncia\]
</dt> <dd>

Un puntero a una variable para recibir la versión secundaria de la biblioteca del registro sin conexión. Para la versión inicial de la biblioteca, el valor es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



 

 




