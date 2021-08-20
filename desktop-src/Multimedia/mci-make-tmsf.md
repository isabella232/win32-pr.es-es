---
title: MCI_MAKE_TMSF macro (Mciapi.h)
description: La macro MCI MAKE TMSF crea un valor de tiempo en formato \_ \_ packed tracks/minutes/seconds/frames (TMSF) a partir de los valores de pistas, minutos, segundos y fotogramas especificados.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec038e0eb1e46c46162c9a2139f03881689db5fe1ee5993a8e135e5d92d67984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138408"
---
# <a name="mci_make_tmsf-macro"></a>Macro \_ MCI MAKE \_ TMSF

La macro **\_ MCI MAKE \_ TMSF** crea un valor de tiempo en formato packed tracks/minutes/seconds/frames (TMSF) a partir de los valores de pistas, minutos, segundos y fotogramas especificados.

## <a name="syntax"></a>Sintaxis


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pistas* 
</dt> <dd>

Número de pistas.

</dd> <dt>

*minutes* 
</dt> <dd>

Número de minutos.

</dd> <dt>

*segundos* 
</dt> <dd>

Número de segundos.

</dd> <dt>

*marcos* 
</dt> <dd>

Número de fotogramas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la hora en formato TMSF empaquetado.

## <a name="remarks"></a>Comentarios

La hora en formato TMSF se expresa como un valor **DWORD** con el byte menos significativo que contiene pistas, el siguiente byte menos significativo que contiene minutos, el siguiente byte menos significativo que contiene segundos y el byte más significativo que contiene fotogramas.

La **macro \_ MCI MAKE \_ TMSF** se define de la siguiente manera:


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
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

 

 





