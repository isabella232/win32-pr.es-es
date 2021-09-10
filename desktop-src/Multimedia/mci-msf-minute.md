---
title: MCI_MSF_MINUTE macro (Mciapi.h)
description: La macro MCI MSF MINUTE recupera el componente minutes de un parámetro que contiene información empaquetada \_ \_ de minutos/segundos/fotogramas (MSF).
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE macro Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370214"
---
# <a name="mci_msf_minute-macro"></a>Macro MCI \_ MSF \_ MINUTE

La **macro MCI \_ MSF \_ MINUTE** recupera el componente minutes de un parámetro que contiene información empaquetada de minutos/segundos/fotogramas (MSF).

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

Devuelve el componente minutes de la información de MSF especificada.

## <a name="remarks"></a>Observaciones

El tiempo en formato MSF se expresa como un valor **DWORD** con el byte menos significativo que contiene minutos, el siguiente byte menos significativo que contiene segundos y el siguiente byte menos significativo que contiene fotogramas. El byte más significativo no se usa.

La **macro MCI \_ MSF \_ MINUTE** se define de la siguiente manera:


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
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

 

 





