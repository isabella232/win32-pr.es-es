---
description: La propiedad dependencias de solo lectura del objeto Merge devuelve una colección de objetos de dependencia que enumera un conjunto de dependencias incorrectas para la base de datos actual.
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: Propiedad Merge. dependencies (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653602"
---
# <a name="mergedependencies-property"></a>Merge. dependencies (propiedad)

La propiedad **dependencias** de solo lectura del objeto [**Merge**](merge-object.md) devuelve una colección de objetos de [**dependencia**](dependency-object.md) que enumera un conjunto de dependencias incorrectas para la base de datos actual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

No es necesario que un módulo esté abierto para recuperar la información de dependencia.

### <a name="c"></a>C++

Vea la función [**Get \_ dependencies**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
