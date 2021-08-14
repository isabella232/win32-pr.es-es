---
description: En Windows installer 1.0 y 1.1, la propiedad Path siempre es la cadena vacía. Las versiones futuras pueden usar este valor para devolver la ruta de acceso al archivo o directorio que no se pudo crear.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Propiedad Error.Path (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7787fcd5bad5550b933b2a866308c1d5b77dd24f60fce23ebc3b227829528307
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378156"
---
# <a name="errorpath-property"></a>Error.Path, propiedad

En Windows installer 1.0 y 1.1, la propiedad Path siempre es la cadena vacía. Las versiones futuras pueden usar este valor para devolver la ruta de acceso al archivo o directorio que no se pudo crear.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.Path
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Este valor solo es válido para errores de tipo msmErrorFileCreate o msmErrorDirCreate. Puede determinar el tipo de error llamando a [**la propiedad Type**](error-type.md) del objeto [**Error.**](error-object.md)

### <a name="c"></a>C++

Consulte [**la función get \_ Path.**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

