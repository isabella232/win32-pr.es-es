---
title: Macro MCI_MAKE_MSF (Mciapi. h)
description: La \_ macro MCI make de \_ MSF crea un valor de hora en formato empaquetado de minutos/segundos/marcos (MSF) a partir de los minutos, los segundos y los valores de fotogramas dados.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997085"
---
# <a name="mci_make_msf-macro"></a>\_Crear una \_ macro de MSF en MCI

La macro **MCI \_ Make de \_ MSF** crea un valor de hora en formato empaquetado de minutos/segundos/marcos (MSF) a partir de los minutos, los segundos y los valores de fotogramas dados.

## <a name="syntax"></a>Sintaxis


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

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

Devuelve la hora en formato de MSF empaquetado.

## <a name="remarks"></a>Observaciones

La hora en formato MSF se expresa como un valor **DWORD** con el byte menos significativo que contiene los minutos, el siguiente byte menos significativo que contiene los segundos y el siguiente byte menos significativo que contiene fotogramas. El byte más significativo no se utiliza.

La macro **MCI \_ Make de \_ MSF** se define de la siguiente manera:


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
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

 

 





