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
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842006"
---
# <a name="iaclcustommruaddmrustring-method"></a>IACLCustomMRU::AddMRUString (método)

Agrega una entrada a la lista de MRU usada más recientemente.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



 

 




