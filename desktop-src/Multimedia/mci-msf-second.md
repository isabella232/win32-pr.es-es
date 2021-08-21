---
title: MCI_MSF_SECOND macro (Mciapi.h)
description: La macro MCI MSF SECOND recupera el componente seconds de un parámetro que contiene información \_ \_ empaquetada de minutos/segundos/fotogramas (MSF).
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND macro Windows Multimedia
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
ms.openlocfilehash: eb09643ae8d3ecdf59c6f3631c9dc28f43bba7ee0434ebabed3e4260c3fec01d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138364"
---
# <a name="mci_msf_second-macro"></a>Macro MCI \_ MSF \_ SECOND

La **macro MCI \_ MSF \_ SECOND** recupera el componente seconds de un parámetro que contiene información empaquetada de minutos/segundos/fotogramas (MSF).

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

Devuelve el componente de segundos de la información de MSF especificada.

## <a name="remarks"></a>Comentarios

La hora en formato MSF se expresa como un valor **DWORD** con el byte menos significativo que contiene minutos, el siguiente byte menos significativo que contiene segundos y el siguiente byte menos significativo que contiene fotogramas. El byte más significativo no se usa.

La **macro MCI \_ MSF \_ SECOND** se define de la siguiente manera:


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





