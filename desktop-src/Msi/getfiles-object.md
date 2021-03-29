---
description: El objeto GetFiles recupera los archivos necesarios en un idioma determinado del módulo. Requiere que ciertas acciones se realicen a través del objeto Merge antes de que todas las partes de esta interfaz devuelvan resultados válidos.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: Objeto GetFiles (Mergemod. h)
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
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653935"
---
# <a name="getfiles-object"></a>GetFiles (objeto)

El objeto **GetFiles** recupera los archivos necesarios en un idioma determinado del módulo. Requiere que ciertas acciones se realicen a través del [objeto Merge](merge-object.md) antes de que todas las partes de esta interfaz devuelvan resultados válidos.

## <a name="members"></a>Miembros

El objeto **GetFiles** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **GetFiles** tiene estas propiedades.



| Propiedad                                               | Descripción                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ModuleFiles**](getfiles-modulefiles.md)<br/> | La propiedad [**ModuleFiles**](getfiles-modulefiles.md) devuelve todas las claves principales de la [tabla de archivos](file-table.md) para el módulo actualmente abierto.<br/> |



 

## <a name="c"></a>C++

interfaz **IMsmGetFiles: IDispatch**

## <a name="interface-id"></a>IDENTIFICADOR de interfaz



| Constante              | Value                                  |
|-----------------------|----------------------------------------|
| **\_IMSMGETFILES IID** | {7041AE26-2D78-11D2-888A-00A0C981B015} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




