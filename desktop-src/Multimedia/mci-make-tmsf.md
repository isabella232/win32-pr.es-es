---
title: Macro MCI_MAKE_TMSF (Mciapi. h)
description: La macro de TMSF de MCI \_ \_ crea un valor de hora en el formato empaquetado de pistas/minutos/segundos/marcos (TMSF) a partir de los valores de las pistas, los minutos, los segundos y los marcos especificados.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF de macros de Windows multimedia
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
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676984"
---
# <a name="mci_make_tmsf-macro"></a>\_TMSF de creación de \_ macros

La macro de **\_ \_ TMSF de MCI** crea un valor de hora en el formato empaquetado de pistas/minutos/segundos/marcos (TMSF) a partir de los valores de las pistas, los minutos, los segundos y los marcos especificados.

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

*realiza* 
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

## <a name="remarks"></a>Observaciones

La hora en formato TMSF se expresa como un valor **DWORD** con el byte menos significativo que contiene pistas, el siguiente byte menos significativo que contiene los minutos, el siguiente byte menos significativo que contiene los segundos y el byte más significativo que contiene fotogramas.

La macro **MCI \_ Make \_ TMSF** se define de la siguiente manera:


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
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

 

 





