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
ms.openlocfilehash: bc61747d891d3c91afd5e4cb7f9a16eef44e13eb3de275bbf9575d8a4f584d40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039235"
---
# <a name="mci_hms_second-macro"></a>Macro MCI \_ HMS \_ SECOND

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

## <a name="remarks"></a>Comentarios

El tiempo en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene horas, el siguiente byte menos significativo que contiene minutos y el siguiente byte menos significativo que contiene segundos. El byte más significativo no se usa.

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

[Mci](mci.md)
</dt> <dt>

[MCI Macros](mci-macros.md)
</dt> </dl>

 

 





