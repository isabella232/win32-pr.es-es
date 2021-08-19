---
title: MCI_VCR_SETAUDIO_PARMS estructura (Vcr.h)
description: La estructura MCI VCR SETAUDIO PARMS contiene parámetros para el comando SETAUDIO de MCI para \_ \_ las \_ \_ grabadoras de vídeo.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- MCI_VCR_SETAUDIO_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa07d4cf8b88eb246019bf18dd1c1328413718a70b17ebb16e27606958473f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802963"
---
# <a name="mci_vcr_setaudio_parms-structure"></a>Estructura MCI \_ VCR \_ SETAUDIO \_ PARMS

La **estructura MCI \_ VCR \_ SETAUDIO \_ PARMS** contiene parámetros para el [**comando \_ SETAUDIO**](mci-setaudio.md) de MCI para las grabadoras de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwTrack**
</dt> <dd>

Pista de audio.

</dd> <dt>

**dwTo**
</dt> <dd>

Tipo de entrada o entrada supervisada.

</dd> <dt>

**dwNumber**
</dt> <dd>

Entrada de audio (del tipo especificado en el **miembro dwTo)** que se usará.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ SETAUDIO**](mci-setaudio.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

