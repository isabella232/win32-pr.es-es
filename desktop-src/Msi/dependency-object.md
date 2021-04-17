---
description: El objeto de dependencia devuelve un módulo del que depende el módulo actual y que aún no se ha combinado en la base de datos de instalación actual.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Objeto de dependencia (Mergemod. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653677"
---
# <a name="dependency-object"></a>Objeto de dependencia

El objeto de **dependencia** devuelve un módulo del que depende el módulo actual y que aún no se ha combinado en la base de datos de instalación actual.

## <a name="members"></a>Miembros

El objeto de **dependencia** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto de **dependencia** tiene estas propiedades.



| Propiedad                                           | Descripción                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**Idioma**](dependency-language.md)<br/> | Devuelve el idioma del módulo.<br/>           |
| [**Módulo**](dependency-module.md)<br/>     | Devuelve el identificador de módulo del módulo necesario.<br/> |
| [**Versión**](dependency-version.md)<br/>   | Devuelve la versión del módulo necesario.<br/>   |



 

## <a name="c"></a>C++

interfaz **IMsmDependency: IDispatch**

## <a name="interface-id"></a>IDENTIFICADOR de interfaz



| Constante                | Value                                  |
|-------------------------|----------------------------------------|
| **\_IMSMDEPENDENCY IID** | {0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




