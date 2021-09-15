---
title: MCI_HMS_SECOND macro (Mciapi.h)
description: La macro MCI HMS SECOND recupera el componente seconds de un parámetro que contiene información empaquetada \_ \_ de horas/minutos/segundos (HMS).
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476836"
---
# <a name="mci_hms_second-macro"></a>Macro \_ MCI HMS \_ SECOND

La **macro MCI \_ HMS \_ SECOND** recupera el componente seconds de un parámetro que contiene información empaquetada de horas/minutos/segundos (HMS).

## <a name="syntax"></a>Sintaxis


```C++
BYTE MCI_HMS_SECOND(
   DWORD dwHMS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwHMS* 
</dt> <dd>

Hora en formato HMS.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el componente de segundos de la información de HMS especificada.

## <a name="remarks"></a>Observaciones

La hora en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene horas, el siguiente byte menos significativo que contiene minutos y el siguiente byte menos significativo que contiene segundos. El byte más significativo no se usa.

La **macro \_ MCI HMS \_ SECOND** se define de la siguiente manera:


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI Macros](mci-macros.md)
</dt> </dl>

 

 





