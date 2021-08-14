---
title: MCI_VCR_PLAY_PARMS estructura (Vcr.h)
description: La estructura MCI VCR PLAY PARMS contiene parámetros para el \_ \_ comando \_ MCI PLAY para las \_ grabadoras de vídeo.
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
ms.openlocfilehash: 6f2e725ca3dc04fa13dd89aff0a5fbd60ede66f83154740803c98679eb77aec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374369"
---
# <a name="mci_vcr_play_parms-structure"></a>Estructura MCI \_ VCR \_ PLAY \_ PARMS

La **estructura MCI \_ VCR PLAY \_ \_ PARMS** contiene parámetros para el [**comando MCI \_ PLAY**](mci-play.md) para las grabadoras de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a>Miembros

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

Valor de hora que afecta al [**comando \_ MCI PLAY**](mci-play.md) o [**MCI \_ CUE.**](mci-cue.md) Para [**MCI \_ PLAY,**](mci-play-parms.md)es el momento en que comienza la reproducción. Para **MCI \_ CUE**, es la hora en que el dispositivo cued alcanza la posición dada en **dwFrom**.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las posiciones se especifican en el formato de hora actual.

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ CUE**](mci-cue.md)
</dt> <dt>

[**MCI \_ PLAY**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

