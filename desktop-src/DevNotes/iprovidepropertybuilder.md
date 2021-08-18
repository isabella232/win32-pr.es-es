---
description: La interfaz IProvidePropertyBuilder, cuando se implementa, permite a los objetos especificar objetos del generador de propiedades para las propiedades.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Interfaz IProvidePropertyBuilder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: d6d82cdafbf775c7316ed882cf3776aaf216fcb82938825d8c939f21e60cc0e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750025"
---
# <a name="iprovidepropertybuilder-interface"></a>Interfaz IProvidePropertyBuilder

La **interfaz IProvidePropertyBuilder,** cuando se implementa, permite a los objetos especificar objetos del generador de propiedades para las propiedades. Los generadores se invocan mediante un botón de puntos suspensivos ( ... ) en el explorador de propiedades Microsoft Visual Studio y se invocan a través de ExecuteBuilder cuando se \[ \] presiona el botón. [](iprovidepropertybuilder-executebuilder.md) Para proporcionar un generador para una propiedad determinada, devuelva un GUID para el generador de propiedades que se debe invocar para la propiedad actual desde [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md). Por lo general, los generadores se implementan a través de cuadros de diálogo modales.

La versión de esta interfaz es 1.0. Las llamadas a métodos se reciben en un punto de conexión asignado dinámicamente (como se describe en la documentación binaria de MSMQ sobre la asignación de puntos de conexión) y usan el UUID (identificador único universal) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".

## <a name="members"></a>Miembros

La **interfaz IProvidePropertyBuilder:IUnknown** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IProvidePropertyBuilder** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IProvidePropertyBuilder:IUnknown** tiene estos métodos.



| Método                                                                       | Descripción                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md)             | Notifica a un objeto que debe mostrar su generador para la propiedad especificada.<br/> |
| [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md) | Comprueba si un generador debe estar asociado a una propiedad determinada.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



 

 
