---
title: MCI_MAKE_HMS macro (Mciapi.h)
description: La macro MCI MAKE HMS crea un valor de tiempo en formato \_ packed hours/minutes/seconds (HMS) a partir de los valores de \_ horas, minutos y segundos especificados.
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370207"
---
# <a name="mci_make_hms-macro"></a>Macro \_ MCI MAKE \_ HMS

La **macro \_ MCI MAKE \_ HMS** crea un valor de tiempo en formato packed hours/minutes/seconds (HMS) a partir de los valores de horas, minutos y segundos especificados.

## <a name="syntax"></a>Sintaxis


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hours* 
</dt> <dd>

Número de horas.

</dd> <dt>

*minutes* 
</dt> <dd>

Número de minutos.

</dd> <dt>

*segundos* 
</dt> <dd>

Número de segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la hora en formato HMS empaquetado.

## <a name="remarks"></a>Observaciones

El tiempo en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene horas, el siguiente byte menos significativo que contiene minutos y el siguiente byte menos significativo que contiene segundos. El byte más significativo no se usa.

La **macro \_ MCI MAKE \_ HMS** se define de la siguiente manera:


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
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

 

 





