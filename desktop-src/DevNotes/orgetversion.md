---
description: Esta función recupera la versión de la biblioteca del Registro sin conexión.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: Función ORGetVersion (Offreg.h)
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
ms.openlocfilehash: f72f4d9995a9cf01e887770bec2d51c6bf566772a1afd027d3419daf374b07e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653384"
---
# <a name="orgetversion-function"></a>Función ORGetVersion

Esta función recupera la versión de la biblioteca del Registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwMajorVersion* \[ out\]
</dt> <dd>

Puntero a una variable para recibir la versión principal de la biblioteca del Registro sin conexión. Para la versión inicial de la biblioteca, el valor es 1.

</dd> <dt>

*pdwMinorVersion* \[ out\]
</dt> <dd>

Puntero a una variable para recibir la versión secundaria de la biblioteca del Registro sin conexión. Para la versión inicial de la biblioteca, el valor es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



 

 




