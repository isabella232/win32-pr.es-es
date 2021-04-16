---
title: Macro MCI_MSF_MINUTE (Mciapi. h)
description: La \_ macro MCI \_ -minute de MSF recupera el componente de minutos de un parámetro que contiene información empaquetada en minutos/segundos/marcos (MSF).
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65f978c13fc1b3fbf86266c35786b21612c4e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651418"
---
# <a name="mci_msf_minute-macro"></a>Macro MCI- \_ minute de MSF \_

La macro **MCI- \_ \_ minute de MSF** recupera el componente de minutos de un parámetro que contiene información empaquetada en minutos/segundos/marcos (MSF).

## <a name="syntax"></a>Sintaxis


```C++
BYTE MCI_MSF_MINUTE(
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

Devuelve el componente de minutos de la información de MSF especificada.

## <a name="remarks"></a>Observaciones

La hora en formato MSF se expresa como un valor **DWORD** con el byte menos significativo que contiene los minutos, el siguiente byte menos significativo que contiene los segundos y el siguiente byte menos significativo que contiene fotogramas. El byte más significativo no se utiliza.

La macro **MCI de \_ MSF \_ minute** se define de la siguiente manera:


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
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

 

 





