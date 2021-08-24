---
title: MCI_SEQ_SET_PARMS estructura (Mciapi.h)
description: La estructura MCI \_ SEQ \_ SET \_ PARMS contiene información para el comando MCI \_ SET para dispositivos de secuenciador MIDI.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- MCI_SEQ_SET_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffb96cfd2f652bf989673bad68c95c6765034d2105fa554efee057faf099a9c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374973"
---
# <a name="mci_seq_set_parms-structure"></a>Estructura MCI \_ SEQ \_ SET \_ PARMS

La **estructura MCI \_ SEQ SET \_ \_ PARMS** contiene información para el [**comando MCI \_ SET**](mci-set.md) para dispositivos de secuenciador MIDI.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana usado para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato de hora del secuenciador.

</dd> <dt>

**dwAudio**
</dt> <dd>

Canal de salida de audio.

</dd> <dt>

**dwTempo**
</dt> <dd>

Tempo.

</dd> <dt>

**dwPort**
</dt> <dd>

Puerto

</dd> <dt>

**dw DwE**
</dt> <dd>

Tipo de sincronización utilizado por el secuenciador para la operación subordinada.

</dd> <dt>

**dwMaster**
</dt> <dd>

Tipo de sincronización utilizado por el secuenciador para la operación maestra.

</dd> <dt>

**dwOffset**
</dt> <dd>

Desplazamiento de datos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

