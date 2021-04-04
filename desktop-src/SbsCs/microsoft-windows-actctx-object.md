---
description: El objeto Microsoft. Windows. ActCtx hace referencia a los manifiestos y proporciona una manera de que los motores de scripting tengan acceso a los ensamblados en paralelo. El objeto Microsoft. Windows. ActCtx se puede usar para crear una instancia de un ensamblado en paralelo con componentes COM.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Objeto Microsoft. Windows. ActCtx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908830"
---
# <a name="microsoftwindowsactctx-object"></a>Objeto Microsoft. Windows. ActCtx

El objeto **Microsoft. Windows. ActCtx** hace referencia a los manifiestos y proporciona una manera de que los motores de scripting tengan acceso a los ensamblados en paralelo. El objeto **Microsoft. Windows. ActCtx** se puede usar para crear una instancia de un ensamblado en paralelo con componentes com.

El objeto **Microsoft. Windows. ActCtx** se incluye como un ensamblado en Windows Server 2003. También puede instalarse mediante aplicaciones que usan el Windows Installer para la configuración e incluirla como módulo de combinación en su paquete de instalación.

## <a name="members"></a>Miembros

El objeto **Microsoft. Windows. ActCtx** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **Microsoft. Windows. ActCtx** tiene estos métodos.



| Método                               | Descripción                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [**DataSpace**](createobject.md) | Crea un objeto en el contexto del manifiesto actual.<br/>            |
| [**GetObject**](getobject.md)       | Obtiene una instancia de un objeto **Microsoft. Windows. ActCtx** existente.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **Microsoft. Windows. ActCtx** tiene estas propiedades.



| Propiedad                                | Tipo de acceso          | Descripción                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [**Manifiesto**](manifest.md)<br/> | Solo lectura<br/> | Obtiene el contexto de activación activo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



 

 




