---
description: Carga una lista de cadenas en la lista de elementos usados más recientemente (MRU) del registro.
title: 'IACLCustomMRU:: Initialize (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 768df625cb66c888ddccc85f72de5b8676c20b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997684"
---
# <a name="iaclcustommruinitialize-method"></a>IACLCustomMRU:: Initialize (método)

Carga una lista de cadenas en la lista de elementos usados más recientemente (MRU) del registro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszMRURegKey* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Un puntero a un búfer que contiene la clave del registro que contiene las cadenas para la lista MRU.

</dd> <dt>

*dwMax* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Número máximo de entradas que se pueden tomar de *pwszMRURegKey*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



 

 




