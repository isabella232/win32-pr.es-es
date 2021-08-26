---
description: El método GetError del objeto View devuelve el error de validación y el nombre de columna para el que se produjo el error.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: Método View.GetError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ddbed26565598ad58b3605b7c70a9a5bbede3e5282ff4a7fa011df5c56bd8b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038805"
---
# <a name="viewgeterror-method"></a>Método View.GetError

El **método GetError** del [**objeto View**](view-object.md) devuelve el error de validación y el nombre de columna para el que se produjo el error. En la automatización, el valor devuelto es una cadena con el formato ColumnName, donde representa un código de error de \# \# \# \# 2 dígitos. Devuelve el primer error de la matriz de errores de la vista. Las llamadas posteriores devuelven el siguiente valor en la matriz de errores. Una vez que se devuelve un valor de "00", no existen más errores y las llamadas posteriores simplemente recorren la matriz de nuevo.

## <a name="syntax"></a>Sintaxis


```JScript
View.GetError()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView se define como \_ 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




