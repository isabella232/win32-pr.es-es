---
title: Propiedad IRDVTaskPlugin PluginName (Tspubplugincom.h)
description: Contiene el nombre para mostrar del agente de tareas.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Propiedad PluginName Servicios de Escritorio remoto
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
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168673"
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Tspubplugincom.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





