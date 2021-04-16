---
description: El método fetch del objeto View recupera la siguiente fila de datos de columna si hay más filas disponibles en el conjunto de resultados; en caso contrario, es NULL. Llame al método Execute antes del método Fetch.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: View. fetch (método)
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
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678981"
---
# <a name="viewfetch-method"></a>View. fetch (método)

El método **Fetch** del objeto [**View**](view-object.md) recupera la siguiente fila de datos de columna si hay más filas disponibles en el conjunto de resultados; en caso contrario, es NULL. Llame al método [**Execute**](view-execute.md) antes del método **Fetch** .

## <a name="syntax"></a>Sintaxis


```JScript
View.Fetch()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se debe usar el mismo objeto de [**registro**](record-object.md) para recuperar los datos de varias filas, o bien se debe liberar el objeto saliendo del ámbito. El registro se puede probar para el final del conjunto de resultados mediante la sintaxis "If FetchRecord is Nothing".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView se define como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




