---
title: Propiedad IRDVTaskPlugin PluginName (Tspubplugincom.h)
description: Contiene el nombre para mostrar del agente de tareas.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Extensión de la propiedad PluginName Servicios de Escritorio remoto
- Propiedad PluginName Servicios de Escritorio remoto interfaz , IRDVTaskPlugin
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto , propiedad PluginName
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
ms.openlocfilehash: 078934c8f19085bf233df78501798a8416ceadf7ba6a0b663cb14b8a8c46b223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129336"
---
# <a name="irdvtaskpluginpluginname-property"></a>IRDVTaskPlugin::P luginName

Contiene el nombre para mostrar del agente de tareas. Este nombre solo se usa con fines de registro.

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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                           |
| Header<br/>                   | <dl> <dt>Tspubplugincom.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





