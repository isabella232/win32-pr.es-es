---
title: MCI_HMS_MINUTE macro (Mciapi.h)
description: La macro MCI HMS MINUTE recupera el componente minutes de un parámetro que contiene información empaquetada \_ \_ de horas/minutos/segundos (HMS).
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE macro Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370196"
---
# <a name="mci_hms_minute-macro"></a>Macro MCI \_ HMS \_ MINUTE

La **macro MCI \_ HMS \_ MINUTE** recupera el componente minutes de un parámetro que contiene información empaquetada de horas/minutos/segundos (HMS).

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

Devuelve el componente minutes de la información de HMS especificada.

## <a name="remarks"></a>Observaciones

El tiempo en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene horas, el siguiente byte menos significativo que contiene minutos y el siguiente byte menos significativo que contiene segundos. El byte más significativo no se usa.

La **macro \_ MCI HMS \_ MINUTE** se define de la siguiente manera:


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
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

 

 





