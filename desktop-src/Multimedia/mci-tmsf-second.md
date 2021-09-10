---
title: MCI_TMSF_SECOND macro (Mciapi.h)
description: La macro MCI TMSF SECOND recupera el componente seconds de un parámetro que contiene información empaquetada \_ \_ de pistas, minutos, segundos y fotogramas (TMSF).
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722949487400f80ed72f9e120d5dbf8678ab81a3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370226"
---
# <a name="mci_tmsf_second-macro"></a>Macro MCI \_ TMSF \_ SECOND

La **macro \_ MCI TMSF \_ SECOND** recupera el componente seconds de un parámetro que contiene información empaquetada de pistas, minutos, segundos y fotogramas (TMSF).

## <a name="syntax"></a>Sintaxis


```C++
BYTE MCI_TMSF_SECOND(
   DWORD dwTMSF
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwTMSF* 
</dt> <dd>

Hora en formato TMSF.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el componente de segundos de la información de TMSF especificada.

## <a name="remarks"></a>Observaciones

La hora en formato TMSF se expresa como un valor **DWORD** con el byte menos significativo que contiene pistas, el siguiente byte menos significativo que contiene minutos, el siguiente byte menos significativo que contiene segundos y el byte más significativo que contiene fotogramas.

La **macro \_ MCI TMSF \_ SECOND** se define de la siguiente manera:


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
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

 

 





