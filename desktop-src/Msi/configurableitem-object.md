---
description: El objeto ConfigurableItem representa una sola fila de la tabla ModuleConfiguration.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Objeto ConfigurableItem (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653924"
---
# <a name="configurableitem-object"></a>Objeto ConfigurableItem

El **objeto ConfigurableItem** representa una sola fila de la [tabla ModuleConfiguration](moduleconfiguration-table.md). Se trata de un único "atributo" configurable desde el módulo. La interfaz consta de propiedades de solo lectura, una para cada columna de la tabla ModuleConfiguration. La definición de la interfaz es la siguiente.

## <a name="members"></a>Miembros

El objeto **ConfigurableItem** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **ConfigurableItem** tiene estas propiedades.



| Propiedad                                                         | Descripción                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atributos**](configurableitem-attributes.md)<br/>     | Devuelve el valor del campo Attributes del registro de este objeto en la tabla ModuleConfiguration.<br/>                            |
| [**Context**](configurableitem-context.md)<br/>           | Devuelve el valor en el campo de contexto del registro de este objeto en la tabla ModuleConfiguration.<br/>                               |
| [**DefaultValue**](configurableitem-defaultvalue.md)<br/> | Devuelve el valor del campo DefaultValue del registro de este objeto en la tabla ModuleConfiguration.<br/>                          |
| [**Descripción**](configurableitem-description.md)<br/>   | Devuelve el valor en el campo de Descripción del registro de este objeto en la tabla ModuleConfiguration.<br/>                           |
| [**DisplayName**](configurableitem-displayname.md)<br/>   | Devuelve el valor en el campo DisplayName del registro de este objeto en la tabla ModuleConfiguration.<br/>                           |
| [**Aplique**](configurableitem-format.md)<br/>             | Devuelve el valor en el campo de formato del registro de este objeto en la tabla ModuleConfiguration.<br/>                                |
| [**HelpKeyword**](configurableitem-helpkeyword.md)<br/>   | Devuelve el valor del campo HelpKeyword del registro de este objeto en la tabla ModuleConfiguration.<br/>                           |
| [**HelpLocation**](configurableitem-helplocation.md)<br/> | Devuelve el valor en el campo HelpLocation del registro de este objeto en la tabla ModuleConfiguration.<br/>                          |
| [**Name**](configurableitem-name.md)<br/>                 | Devuelve el valor del campo Nombre del registro de este objeto en la [tabla ModuleConfiguration](moduleconfiguration-table.md).<br/> |
| [**Tipo**](configurableitem-type.md)<br/>                 | Devuelve el valor en el campo de tipo del registro de este objeto en la tabla ModuleConfiguration.<br/>                                  |



 

## <a name="c"></a>C++

interfaz **IMsmConfigurableItem: IDispatch**

## <a name="interface-id"></a>IDENTIFICADOR de interfaz



| Constante                      | Value                                  |
|-------------------------------|----------------------------------------|
| **\_IMSMCONFIGURABLEITEM IID** | {4D6E6284-D21D-401E-84F6-909E00B50F71} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




