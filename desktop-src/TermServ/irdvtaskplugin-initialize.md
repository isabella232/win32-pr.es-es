---
title: IRDVTaskPlugin Initialize (método)
description: Se llama para inicializar el agente de tareas.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Método Initialize Servicios de Escritorio remoto
- Método Initialize Servicios de Escritorio remoto, interfaz IRDVTaskPlugin
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto, método Initialize
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422062"
---
# <a name="irdvtaskplugininitialize-method"></a>IRDVTaskPlugin:: Initialize (método)

Se llama para inicializar el agente de tareas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNotifySink* \[ de\]
</dt> <dd>

Tipo: **[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) \** _

Un puntero a una interfaz [_ *IRDVTaskPluginNotifySink* *](irdvtaskpluginnotifysink.md) que el agente de tareas usa para comunicarse con el agente de desencadenador. Debe liberar esta interfaz cuando ya no se necesite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





