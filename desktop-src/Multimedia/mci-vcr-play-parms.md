---
title: MCI_VCR_PLAY_PARMS estructura (Vcr.h)
description: La estructura MCI VCR PLAY PARMS contiene parámetros para el comando MCI PLAY para \_ \_ \_ \_ grabadoras de vídeo-grabadora.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- MCI_VCR_PLAY_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245925"
---
# <a name="mci_vcr_play_parms-structure"></a>Estructura MCI \_ VCR \_ PLAY \_ PARMS

La **estructura MCI \_ VCR PLAY \_ \_ PARMS** contiene parámetros para el [**comando MCI \_ PLAY**](mci-play.md) para grabadoras de vídeo-grabadora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posición desde la que se reproducirá.

</dd> <dt>

**dwTo**
</dt> <dd>

Posición en la que se reproducirá.

</dd> <dt>

**dwAt**
</dt> <dd>

Valor de tiempo que afecta al [**comando MCI \_ PLAY**](mci-play.md) [**o MCI \_ CUE.**](mci-cue.md) Para [**MCI \_ PLAY,**](mci-play-parms.md)es el momento en que comienza la reproducción. Para **MCI \_ CUE**, es el momento en que el dispositivo cued alcanza la posición dada en **dwFrom**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las posiciones se especifican en el formato de hora actual.

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ CUE**](mci-cue.md)
</dt> <dt>

[**MCI \_ PLAY**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

