---
description: El método Close del objeto View finaliza la ejecución de la consulta y libera los recursos de la base de datos.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View. Close (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680329"
---
# <a name="viewclose-method"></a>View. Close (método)

El método **Close** del objeto [**View**](view-object.md) finaliza la ejecución de la consulta y libera los recursos de la base de datos.

## <a name="syntax"></a>Sintaxis


```JScript
View.Close()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se debe llamar a este método antes de volver a llamar al método [**Execute**](view-execute.md) en el objeto de [**vista**](view-object.md) , a menos que se hayan obtenido todas las filas del conjunto de resultados con el método [**Fetch**](view-fetch.md) . Se llama internamente cuando se destruye la vista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView se define como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




