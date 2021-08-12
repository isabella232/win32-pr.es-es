---
title: Método IRDVTaskPlugin Initialize
description: Se llama para inicializar el agente de tareas.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Inicialización del método Servicios de Escritorio remoto
- Inicializar método Servicios de Escritorio remoto interfaz , IRDVTaskPlugin
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto método , Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14f4a002a0b33e403c02dba74385edd21e211fb27bcfb144c7a9ddc080a40fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606108"
---
# <a name="irdvtaskplugininitialize-method"></a>IRDVTaskPlugin::Initialize (método)

Se llama para inicializar el agente de tareas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNotifySink* \[ En\]
</dt> <dd>

Tipo: **[ **IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\***

Puntero a una [**interfaz IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) que el agente de tareas usa para comunicarse con el agente de desencadenador. Debe liberar esta interfaz cuando ya no sea necesaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





