---
description: La interfaz IProvidePropertyBuilder, cuando se implementa, permite a los objetos especificar objetos generador de propiedades para las propiedades.
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
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649566"
---
# <a name="iprovidepropertybuilder-interface"></a>Interfaz IProvidePropertyBuilder

La interfaz **IProvidePropertyBuilder** , cuando se implementa, permite a los objetos especificar objetos generador de propiedades para las propiedades. Los generadores se invocan mediante un botón de puntos suspensivos ( \[ ... \] ) en el explorador de propiedades Microsoft Visual Studio y se invocan a través de [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) cuando se presiona el botón. Para proporcionar un generador para una propiedad determinada, devuelva un GUID para el generador de propiedades que se debe invocar para la propiedad actual desde [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md). Los generadores generalmente se implementan a través de cuadros de diálogo modales.

La versión de esta interfaz es 1,0. Las llamadas a métodos se reciben en un punto de conexión asignado dinámicamente (como se describe en la documentación binaria de MSMQ en la asignación de extremos) y usan el UUID (identificador único universal) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".

## <a name="members"></a>Miembros

La interfaz **IProvidePropertyBuilder: IUnknown** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IProvidePropertyBuilder** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IProvidePropertyBuilder: IUnknown** tiene estos métodos.



| Método                                                                       | Descripción                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md)             | Notifica a un objeto que debe mostrar su generador para la propiedad especificada.<br/> |
| [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md) | Comprueba si un generador se debe asociar a una propiedad determinada.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



 

 
