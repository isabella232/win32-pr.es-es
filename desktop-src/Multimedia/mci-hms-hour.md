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
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370190"
---
# <a name="mci_hms_hour-macro"></a>Macro \_ MCI HMS \_ HOUR

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

## <a name="remarks"></a>Observaciones

La hora en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene horas, el siguiente byte menos significativo que contiene minutos y el siguiente byte menos significativo que contiene segundos. El byte más significativo no se usa.

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

[MCI](mci.md)
</dt> <dt>

[MCI Macros](mci-macros.md)
</dt> </dl>

 

 





