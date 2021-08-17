---
title: Propiedad TaskSettings.NetworkSettings
description: Para el scripting, obtiene o establece el objeto de configuración de red que contiene un identificador y un nombre de perfil de red.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Propiedad NetworkSettings Programador de tareas
- Propiedad NetworkSettings Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas propiedad , NetworkSettings
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730701c71a69f05b73524d6f9d1d8ad3d89b5e93620664be33a80c5c41af1479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059663"
---
# <a name="tasksettingsnetworksettings-property"></a>Propiedad TaskSettings.NetworkSettings

Para el scripting, obtiene o establece el objeto de configuración de red que contiene un identificador y un nombre de perfil de red. Si la propiedad [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de [**TaskSettings**](tasksettings.md) es **True** y se especifica un archivo propfile de red en la **propiedad NetworkSettings,** la tarea solo se ejecutará si el perfil de red especificado está disponible.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**NetworkSettings**](networksettings.md) que contiene un identificador y un nombre de perfil de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





