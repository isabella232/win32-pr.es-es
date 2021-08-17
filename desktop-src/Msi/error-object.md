---
description: El objeto Error devuelve la información de un único error de combinación.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Objeto de error (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 237cf88b2830bf210e84d016b52b7fd0b0183c0c0072ac8f654663e2cd3c12dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947036"
---
# <a name="error-object"></a>Objeto de error

El **objeto Error** devuelve la información de un único error de combinación.

## <a name="members"></a>Miembros

El **objeto Error** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Error** tiene estas propiedades.



| Propiedad                                                | Descripción                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**DatabaseKeys**](error-databasekeys.md)<br/>   | Devuelve las claves principales de la fila de la tabla de base de datos que produjo el error.<br/> |
| [**DatabaseTable**](error-databasetable.md)<br/> | Devuelve el nombre de tabla de la tabla de la base de datos que produce el error.<br/>           |
| [**Lenguaje**](error-language.md)<br/>           | Devuelve el idioma del error.<br/>                                                |
| [**ModuleKeys**](error-modulekeys.md)<br/>       | Devuelve las claves principales de la fila de la tabla de módulos que produjo el error.<br/>   |
| [**ModuleTable**](error-moduletable.md)<br/>     | Devuelve el nombre de tabla de la tabla del módulo que produce el error.<br/>             |
| [**Ruta de acceso**](error-path.md)<br/>                   | Devuelve la ruta de acceso al archivo o directorio que produce el error. Actualmente no se usa.<br/>    |
| [**Tipo**](error-type.md)<br/>                   | Devuelve el tipo de error.<br/>                                                        |



 

## <a name="c"></a>C++

interface **IMsmError: IDispatch**

## <a name="interface-id"></a>Identificador de interfaz



| Constante           | Value                                  |
|--------------------|----------------------------------------|
| **IID \_ IMsmError** | {0ADDA828-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




