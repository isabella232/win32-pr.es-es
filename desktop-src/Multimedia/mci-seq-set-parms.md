---
title: MCI_SEQ_SET_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI SEQ \_ set \_ parms contiene información para el comando MCI \_ set para dispositivos MIDI Sequencer.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- Estructura de MCI_SEQ_SET_PARMS de Windows multimedia
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
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996048"
---
# <a name="mci_seq_set_parms-structure"></a>MCI \_ Seq \_ set \_ parms estructura

La estructura **MCI \_ Seq \_ set \_ parms** contiene información para el comando [**MCI \_ set**](mci-set.md) para dispositivos MIDI Sequencer.

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

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

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

Ritmo.

</dd> <dt>

**dwPort**
</dt> <dd>

Puerto

</dd> <dt>

**dwSlave**
</dt> <dd>

Tipo de sincronización utilizada por el secuenciador para la operación subordinada.

</dd> <dt>

**dwMaster**
</dt> <dd>

Tipo de sincronización utilizada por el secuenciador para la operación maestra.

</dd> <dt>

**dwOffset**
</dt> <dd>

Desplazamiento de datos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ set**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

