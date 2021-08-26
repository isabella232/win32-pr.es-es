---
title: MCI_HMS_HOUR macro (Mciapi.h)
description: La macro MCI HMS HOUR recupera el componente hours de un parámetro que contiene información empaquetada \_ \_ de horas/minutos/segundos (HMS).
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b8000e642d18f8499be5f8622a1cf7540fefbd041b7d34f23e1fd5e231815a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039275"
---
# <a name="mci_hms_hour-macro"></a>Macro MCI \_ HMS \_ HOUR

La **macro \_ MCI HMS \_ HOUR** recupera el componente hours de un parámetro que contiene información empaquetada de horas/minutos/segundos (HMS).

## <a name="syntax"></a>Sintaxis


```C++
BYTE MCI_HMS_HOUR(
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

Devuelve el componente hours de la información de HMS especificada.

## <a name="remarks"></a>Comentarios

El tiempo en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene horas, el siguiente byte menos significativo que contiene minutos y el siguiente byte menos significativo que contiene segundos. El byte más significativo no se usa.

La **macro \_ MCI HMS \_ HOUR** se define de la siguiente manera:


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
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

 

 





