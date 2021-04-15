---
title: IRDVTaskPlugin Terminate (método)
description: Se llama cuando se está cerrando el agente de tareas.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Método Terminate Servicios de Escritorio remoto
- Método Terminate Servicios de Escritorio remoto, interfaz IRDVTaskPlugin
- Servicios de Escritorio remoto de la interfaz IRDVTaskPlugin, método Terminate
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422420"
---
# <a name="irdvtaskpluginterminate-method"></a>IRDVTaskPlugin:: Terminate (método)

Se llama cuando se está cerrando el agente de tareas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HR* \[ de\]
</dt> <dd>

Indica si el apagado se debe a un apagado normal o a un error. Si el apagado es normal, contiene **S \_ correctos**. De lo contrario, contiene un código de error **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

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

 

 





