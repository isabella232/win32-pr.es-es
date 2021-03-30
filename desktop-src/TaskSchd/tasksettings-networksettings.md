---
title: Propiedad TaskSettings. NetworkSettings
description: Para scripting, obtiene o establece el objeto de configuración de red que contiene un identificador y un nombre de Perfil de red.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Programador de tareas de la propiedad NetworkSettings
- Programador de tareas de la propiedad NetworkSettings, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad NetworkSettings
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
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801471"
---
# <a name="tasksettingsnetworksettings-property"></a>Propiedad TaskSettings. NetworkSettings

Para scripting, obtiene o establece el objeto de configuración de red que contiene un identificador y un nombre de Perfil de red. Si la propiedad [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de [**TaskSettings**](tasksettings.md) es **true** y se especifica una Propfile de red en la propiedad **NetworkSettings** , la tarea se ejecutará solo si el perfil de red especificado está disponible.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>Valor de propiedad

Un objeto [**NetworkSettings**](networksettings.md) que contiene un identificador y un nombre de Perfil de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





