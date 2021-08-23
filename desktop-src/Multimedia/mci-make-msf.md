---
title: MCI_MAKE_MSF macro (Mciapi.h)
description: La macro MCI MAKE MSF crea un valor de tiempo en formato de \_ minutos,segundos/fotogramas empaquetados (MSF) a partir de los valores de minutos, segundos y \_ fotogramas especificados.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF macro Windows Multimedia
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
ms.openlocfilehash: e16f5cfa2b99f7bdbd7eb3029b3f0186904d8b8e94f455614464fadc98cdd20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690138"
---
# <a name="mci_make_msf-macro"></a>Macro MCI \_ MAKE \_ MSF

La **macro \_ MCI MAKE \_ MSF** crea un valor de tiempo en formato de minutos,segundos/fotogramas empaquetados (MSF) a partir de los valores de minutos, segundos y fotogramas especificados.

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

Devuelve la hora en formato MSF empaquetado.

## <a name="remarks"></a>Comentarios

La hora en formato MSF se expresa como un valor **DWORD** con el byte menos significativo que contiene minutos, el siguiente byte menos significativo que contiene segundos y el siguiente byte menos significativo que contiene fotogramas. El byte más significativo no se usa.

La **macro \_ MCI MAKE \_ MSF** se define de la siguiente manera:


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
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

 

 





