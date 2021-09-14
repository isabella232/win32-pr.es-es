---
description: El objeto ConfigurableItem representa una sola fila de la tabla ModuleConfiguration.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Objeto ConfigurableItem (Mergemod.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158792"
---
# <a name="configurableitem-object"></a>Objeto ConfigurableItem

El **objeto ConfigurableItem representa** una sola fila de la tabla [ModuleConfiguration](moduleconfiguration-table.md). Se trata de un único "atributo" configurable del módulo. La interfaz consta de propiedades de solo lectura, una para cada columna de la tabla ModuleConfiguration. La definición de interfaz es la siguiente.

## <a name="members"></a>Members

El **objeto ConfigurableItem** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto ConfigurableItem** tiene estas propiedades.



| Propiedad.                                                         | Descripción                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atributos**](configurableitem-attributes.md)<br/>     | Devuelve el valor del campo Atributos del registro de este objeto en la tabla ModuleConfiguration.<br/>                            |
| [**Contexto**](configurableitem-context.md)<br/>           | Devuelve el valor del campo Context del registro de este objeto en la tabla ModuleConfiguration.<br/>                               |
| [**Defaultvalue**](configurableitem-defaultvalue.md)<br/> | Devuelve el valor del campo DefaultValue del registro de este objeto en la tabla ModuleConfiguration.<br/>                          |
| [**Descripción**](configurableitem-description.md)<br/>   | Devuelve el valor del campo Descripción del registro de este objeto en la tabla ModuleConfiguration.<br/>                           |
| [**Displayname**](configurableitem-displayname.md)<br/>   | Devuelve el valor del campo DisplayName del registro de este objeto en la tabla ModuleConfiguration.<br/>                           |
| [**Formato**](configurableitem-format.md)<br/>             | Devuelve el valor del campo Formato del registro de este objeto en la tabla ModuleConfiguration.<br/>                                |
| [**HelpKeyword**](configurableitem-helpkeyword.md)<br/>   | Devuelve el valor del campo HelpKeyword del registro de este objeto en la tabla ModuleConfiguration.<br/>                           |
| [**HelpLocation**](configurableitem-helplocation.md)<br/> | Devuelve el valor del campo HelpLocation del registro de este objeto en la tabla ModuleConfiguration.<br/>                          |
| [**Nombre**](configurableitem-name.md)<br/>                 | Devuelve el valor del campo Nombre del registro de este objeto en la [tabla ModuleConfiguration](moduleconfiguration-table.md).<br/> |
| [**Tipo**](configurableitem-type.md)<br/>                 | Devuelve el valor del campo Tipo del registro de este objeto en la tabla ModuleConfiguration.<br/>                                  |



 

## <a name="c"></a>C++

interface **IMsmConfigurableItem: IDispatch**

## <a name="interface-id"></a>Identificador de interfaz



| Constante                      | Value                                  |
|-------------------------------|----------------------------------------|
| **IID \_ IMsmConfigurableItem** | {4D6E6284-D21D-401E-84F6-909E00B50F71} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




