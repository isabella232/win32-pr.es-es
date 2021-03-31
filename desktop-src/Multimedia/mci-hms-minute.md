---
title: Macro MCI_HMS_MINUTE (Mciapi. h)
description: La \_ macro MCI HMS \_ minute recupera el componente de minutos de un parámetro que contiene información de horas/minutos/segundos empaquetados (HMS).
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151129"
---
# <a name="mci_hms_minute-macro"></a>HMS de la \_ macro de minuto de MCI \_

La macro **MCI \_ HMS \_ minute** recupera el componente de minutos de un parámetro que contiene información de horas/minutos/segundos empaquetados (HMS).

## <a name="syntax"></a>Sintaxis


```C++
BYTE MCI_HMS_MINUTE(
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

Devuelve el componente de minutos de la información de HMS especificada.

## <a name="remarks"></a>Observaciones

La hora en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene las horas, el siguiente byte menos significativo que contiene los minutos y el siguiente byte menos significativo que contiene los segundos. El byte más significativo no se utiliza.

La macro **MCI \_ HMS \_ minute** se define de la siguiente manera:


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Macros MCI](mci-macros.md)
</dt> </dl>

 

 





