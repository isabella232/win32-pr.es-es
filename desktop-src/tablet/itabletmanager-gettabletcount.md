---
description: Recupera el número de tabletas conectadas al sistema.
ms.assetid: b2027336-611b-4d17-8943-f16770effaf8
title: 'ITabletManager:: GetTabletCount (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager.GetTabletCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fbdd485c44bc67b3ecaec5aa279d4bc20e18d167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279172"
---
# <a name="itabletmanagergettabletcount-method"></a>ITabletManager:: GetTabletCount (método)

Recupera el número de tabletas conectadas al sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTabletCount(
  [out] ULONG *pcTablets
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcTablets* \[ enuncia\]
</dt> <dd>

El número de tabletas conectadas al sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITabletManager**](itabletmanager.md)
</dt> </dl>

 

 




