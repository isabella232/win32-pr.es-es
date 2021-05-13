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
ms.openlocfilehash: 715c6991021070dd132942de0bb18c8b77684860
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841236"
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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



 

 




