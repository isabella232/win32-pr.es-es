---
description: Agrega una entrada a la lista de mru usada más recientemente.
title: IACLCustomMRU::AddMRUString (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: e5acd71a56ef0dd569315ee924313b10e27e6a4ba7ca75d1dbfa0d1e50932cdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223599"
---
# <a name="iaclcustommruaddmrustring-method"></a>IACLCustomMRU::AddMRUString (método)

Agrega una entrada a la lista de mru usada más recientemente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszEntry* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a un búfer que contiene la nueva entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



 

 




