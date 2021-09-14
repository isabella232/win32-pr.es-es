---
description: La propiedad Module de solo lectura del objeto dependency devuelve el ModuleID del módulo que requiere la cadena actual en forma de BSTR. ModuleID es la misma forma que se usa en la tabla ModuleSignature.
ms.assetid: 22aae1b6-59b6-4842-9523-d1e064511380
title: Propiedad Dependency.Module (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency.Module
- IMsmDependency.get_Module
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4bcf2241cd278640b333bb9f08dc24e645990b4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158600"
---
# <a name="dependencymodule-property"></a>Propiedad Dependency.Module

La propiedad **Module** de solo lectura del objeto [**Dependency**](dependency-object.md) devuelve el ModuleID del módulo requerido por la cadena actual en forma de **BSTR.** ModuleID es la misma forma que se usa en [la tabla ModuleSignature](modulesignature-table.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Dependency.Module
```



## <a name="property-value"></a>Valor de propiedad

## <a name="c"></a>C++

Consulte el [**método IMsmDependency \_ get \_ Module.**](/windows/win32/api/mergemod/nf-mergemod-imsmdependency-get_module)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

