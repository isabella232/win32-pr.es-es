---
description: El objeto Dependency devuelve un módulo del que depende el módulo actual y que aún no se ha combinado en la base de datos de instalación actual.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Objeto de dependencia (Mergemod.h)
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
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158599"
---
# <a name="dependency-object"></a>Objeto de dependencia

El **objeto Dependency** devuelve un módulo del que depende el módulo actual y que aún no se ha combinado en la base de datos de instalación actual.

## <a name="members"></a>Members

El **objeto Dependency** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Dependency** tiene estas propiedades.



| Propiedad.                                           | Descripción                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**Idioma**](dependency-language.md)<br/> | Devuelve el idioma del módulo.<br/>           |
| [**Módulo**](dependency-module.md)<br/>     | Devuelve el identificador del módulo necesario.<br/> |
| [**Versión**](dependency-version.md)<br/>   | Devuelve la versión del módulo necesario.<br/>   |



 

## <a name="c"></a>C++

interfaz **IMsmDependency: IDispatch**

## <a name="interface-id"></a>Identificador de interfaz



| Constante                | Value                                  |
|-------------------------|----------------------------------------|
| **IID \_ IMsmDependency** | {0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




