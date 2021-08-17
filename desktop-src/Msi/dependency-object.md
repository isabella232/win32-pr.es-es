---
description: El objeto Dependency devuelve un módulo del que depende el módulo actual y que aún no se ha combinado con la base de datos de instalación actual.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Objeto dependency (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: ac5786dcf3d4818fdfb3f0458cbfa85c923e5200ae69b5cb93d38330c322abf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378895"
---
# <a name="dependency-object"></a>Objeto de dependencia

El **objeto Dependency** devuelve un módulo del que depende el módulo actual y que aún no se ha combinado con la base de datos de instalación actual.

## <a name="members"></a>Miembros

El **objeto Dependency** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Dependency** tiene estas propiedades.



| Propiedad                                           | Descripción                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**Idioma**](dependency-language.md)<br/> | Devuelve el idioma del módulo.<br/>           |
| [**Módulo**](dependency-module.md)<br/>     | Devuelve el identificador del módulo necesario.<br/> |
| [**Versión**](dependency-version.md)<br/>   | Devuelve la versión del módulo necesario.<br/>   |



 

## <a name="c"></a>C++

interface **IMsmDependency: IDispatch**

## <a name="interface-id"></a>Identificador de interfaz



| Constante                | Valor                                  |
|-------------------------|----------------------------------------|
| **IID \_ IMsmDependency** | {0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




