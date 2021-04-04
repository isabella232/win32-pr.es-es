---
title: Propiedad IRDVTaskPlugin PluginName (Tspubplugincom. h)
description: Contiene el nombre para mostrar del agente de tareas.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PluginName
- Propiedad PluginName Servicios de Escritorio remoto, interfaz IRDVTaskPlugin
- Servicios de Escritorio remoto de la interfaz IRDVTaskPlugin, propiedad PluginName
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802707"
---
# <a name="irdvtaskpluginpluginname-property"></a>IRDVTaskPlugin::P propiedad luginName

Contiene el nombre para mostrar del agente de tareas. Este nombre se usa solo con fines de registro.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre para mostrar del agente de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Tspubplugincom. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





