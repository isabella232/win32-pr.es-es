---
description: El método Close del objeto View finaliza la ejecución de consultas y libera los recursos de base de datos.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: Método View.Close
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
ms.openlocfilehash: edbf2dd30902fa437fdd67d21efb86bb2edeabbd499f0f022501f166ad1b92a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498855"
---
# <a name="viewclose-method"></a>Método View.Close

El **método Close** del objeto [**View**](view-object.md) finaliza la ejecución de consultas y libera los recursos de base de datos.

## <a name="syntax"></a>Sintaxis


```JScript
View.Close()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se debe llamar a este método antes de que se vuelva a llamar al método [**Execute**](view-execute.md) en el objeto [**View**](view-object.md) a menos que se hayan obtenido todas las filas del conjunto de resultados con el [**método Fetch.**](view-fetch.md) Se llama internamente cuando se destruye la vista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView se define como \_ 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




