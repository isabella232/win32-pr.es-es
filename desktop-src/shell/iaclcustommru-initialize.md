---
description: Carga una lista de cadenas en la lista de mru usada más recientemente desde el registro.
title: IACLCustomMRU::Initialize (Método)
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
ms.openlocfilehash: 0e0cad5f144a4ce97c648463cfdf31bf1c2ee7da0fb89b5508ce9386dba0f14f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111765"
---
# <a name="iaclcustommruinitialize-method"></a>IACLCustomMRU::Initialize (Método)

Carga una lista de cadenas en la lista de mru usada más recientemente desde el registro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszMRURegKey* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a un búfer que contiene la clave del Registro que contiene las cadenas de la lista de MRU.

</dd> <dt>

*dwMax* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Número máximo de entradas que se pueden tomar de *pwszMRURegKey*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



 

 




