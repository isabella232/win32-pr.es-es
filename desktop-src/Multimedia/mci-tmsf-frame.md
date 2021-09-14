---
title: MCI_TMSF_FRAME macro (Mciapi.h)
description: La macro MCI TMSF FRAME recupera el componente frames de un parámetro que contiene información empaquetada \_ \_ de pistas, minutos, segundos y fotogramas (TMSF).
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- MCI_TMSF_FRAME macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245973"
---
# <a name="mci_tmsf_frame-macro"></a>Macro \_ MCI TMSF \_ FRAME

La **macro \_ MCI TMSF \_ FRAME** recupera el componente frames de un parámetro que contiene información empaquetada de pistas, minutos, segundos y fotogramas (TMSF).

## <a name="syntax"></a>Sintaxis


```C++
BYTE MCI_TMSF_FRAME(
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

Devuelve el componente de fotogramas de la información de TMSF especificada.

## <a name="remarks"></a>Observaciones

El tiempo en formato TMSF se expresa como un valor **DWORD** con el byte menos significativo que contiene pistas, el siguiente byte menos significativo que contiene minutos, el siguiente byte menos significativo que contiene segundos y el byte más significativo que contiene fotogramas.

La **macro \_ MCI TMSF \_ FRAME** se define de la siguiente manera:


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
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

 

 





