---
description: El método Fetch del objeto View recupera la siguiente fila de datos de columna si hay más filas disponibles en el conjunto de resultados; de lo contrario, es Null. Llame al método Execute antes del método Fetch.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: Método View.Fetch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b05144b542fd1daa1fc59e12d8ab9ec7031c4a3a5eb6506e9d1316a29b4424ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039495"
---
# <a name="viewfetch-method"></a>Método View.Fetch

El **método Fetch** del objeto [**View**](view-object.md) recupera la siguiente fila de datos de columna si hay más filas disponibles en el conjunto de resultados; de lo contrario, es Null. Llame al [**método Execute**](view-execute.md) antes del **método Fetch.**

## <a name="syntax"></a>Sintaxis


```JScript
View.Fetch()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Debe [**usarse el**](record-object.md) mismo objeto Record para recuperar los datos de varias filas o, de lo contrario, el objeto debe liberarse al salir del ámbito. El registro se puede probar para el final del conjunto de resultados mediante la sintaxis "If FetchRecord Is Nothing".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView se define como \_ 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




