---
description: El objeto GetFiles recupera los archivos necesarios en un lenguaje determinado del módulo. Requiere que se realicen determinadas acciones a través del objeto Merge antes de que todas las partes de esta interfaz devuelvan resultados válidos.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: Objeto GetFiles (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c8e5848b04b5b87a09d43f1705c48c34adc13eb99017b14260f89357226750c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044245"
---
# <a name="getfiles-object"></a>Objeto GetFiles

El **objeto GetFiles** recupera los archivos necesarios en un lenguaje determinado del módulo. Requiere que se realicen determinadas acciones a través del [objeto Merge antes](merge-object.md) de que todas las partes de esta interfaz devuelvan resultados válidos.

## <a name="members"></a>Miembros

El **objeto GetFiles** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto GetFiles** tiene estas propiedades.



| Propiedad                                               | Descripción                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ModuleFiles**](getfiles-modulefiles.md)<br/> | [**La propiedad ModuleFiles**](getfiles-modulefiles.md) devuelve todas las claves principales de la [tabla File](file-table.md) para el módulo abierto actualmente.<br/> |



 

## <a name="c"></a>C++

interface **IMsmGetFiles: IDispatch**

## <a name="interface-id"></a>Identificador de interfaz



| Constante              | Value                                  |
|-----------------------|----------------------------------------|
| **IID \_ IMsmGetFiles** | {7041AE26-2D78-11D2-888A-00A0C981B015} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




