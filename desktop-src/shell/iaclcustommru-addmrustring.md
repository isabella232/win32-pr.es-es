---
description: Agrega una entrada a la lista de elementos usados más recientemente (MRU).
title: 'IACLCustomMRU:: AddMRUString (método)'
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
ms.openlocfilehash: d2f444041f466b367f3d4532f65029bcc69c3683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997685"
---
# <a name="iaclcustommruaddmrustring-method"></a>IACLCustomMRU:: AddMRUString (método)

Agrega una entrada a la lista de elementos usados más recientemente (MRU).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszEntry* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a un búfer que contiene la nueva entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



 

 




