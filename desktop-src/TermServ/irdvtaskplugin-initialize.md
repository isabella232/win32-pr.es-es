---
title: Método IRDVTaskPlugin Initialize
description: Se llama para inicializar el agente de tareas.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Inicializar método Servicios de Escritorio remoto
- Inicializar método Servicios de Escritorio remoto , interfaz IRDVTaskPlugin
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto , Método Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168674"
---
# <a name="irdvtaskplugininitialize-method"></a>IrDVTaskPlugin::Initialize (método)

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

Puntero a una [**interfaz IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) que el agente de tareas usa para comunicarse con el agente desencadenador. Debe liberar esta interfaz cuando ya no sea necesaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





