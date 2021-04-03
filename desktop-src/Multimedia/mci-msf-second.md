---
title: Macro MCI_MSF_SECOND (Mciapi. h)
description: La \_ macro MCI MSF \_ Second recupera el componente de segundos de un parámetro que contiene la información empaquetada en minutos/segundos/marcos (MSF).
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85dffd36354b335818079ea5b0c88d16752b4501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905334"
---
# <a name="mci_msf_second-macro"></a>Macro MCI de \_ MSF \_ Second

La macro **MCI \_ MSF \_ Second** recupera el componente de segundos de un parámetro que contiene la información empaquetada en minutos/segundos/marcos (MSF).

## <a name="syntax"></a>Sintaxis


```C++
BYTE MCI_MSF_SECOND(
   DWORD dwMSF
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwMSF* 
</dt> <dd>

Hora en formato MSF.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el componente de segundos de la información especificada de MSF.

## <a name="remarks"></a>Observaciones

La hora en formato MSF se expresa como un valor **DWORD** con el byte menos significativo que contiene los minutos, el siguiente byte menos significativo que contiene los segundos y el siguiente byte menos significativo que contiene fotogramas. El byte más significativo no se utiliza.

La macro **MCI \_ MSF \_ Second** se define de la siguiente manera:


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
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

 

 





