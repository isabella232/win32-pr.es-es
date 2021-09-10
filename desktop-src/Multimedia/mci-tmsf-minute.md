---
title: MCI_TMSF_MINUTE macro (Mciapi.h)
description: La macro MCI TMSF MINUTE recupera el componente minutes de un parámetro que contiene información empaquetada \_ \_ de pistas, minutos, segundos y fotogramas (TMSF).
ms.assetid: 9a972579-240f-4641-b65e-9088f39cdf9e
keywords:
- MCI_TMSF_MINUTE macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69a12c2622f3f97f04bdca89389c8ab9be7e948
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370225"
---
# <a name="mci_tmsf_minute-macro"></a>Macro MCI \_ TMSF \_ MINUTE

La **macro MCI \_ TMSF \_ MINUTE** recupera el componente minutes de un parámetro que contiene información empaquetada de pistas, minutos, segundos y fotogramas (TMSF).

## <a name="syntax"></a>Sintaxis


```C++
BYTE MCI_TMSF_MINUTE(
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

Devuelve el componente minutes de la información de TMSF especificada.

## <a name="remarks"></a>Observaciones

El tiempo en formato TMSF se expresa como un valor **DWORD** con el byte menos significativo que contiene pistas, el siguiente byte menos significativo que contiene minutos, el siguiente byte menos significativo que contiene segundos y el byte más significativo que contiene fotogramas.

La **macro \_ MCI TMSF \_ MINUTE** se define de la siguiente manera:


```C++
#define MCI_TMSF_MINUTE(tmsf) ((BYTE)(((WORD)(tmsf)) >> 8)) 
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

 

 





