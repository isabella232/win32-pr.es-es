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
ms.openlocfilehash: 1cd5ce697057a04d611dcf7f2f0cd0757874a27f869b5b6aa450d9c6bcc85209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378894"
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



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

