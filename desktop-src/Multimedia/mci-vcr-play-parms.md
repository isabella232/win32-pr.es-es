---
title: MCI_VCR_PLAY_PARMS estructura (VCR. h)
description: La \_ estructura MCI VCR \_ Play \_ parms contiene parámetros para el comando de reproducción de MCI para los \_ grabadores de casete de vídeo.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- Estructura de MCI_VCR_PLAY_PARMS de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996500"
---
# <a name="mci_vcr_play_parms-structure"></a>\_Parms MCI VCR \_ Play \_ Structure

La estructura **MCI \_ VCR \_ Play \_ parms** contiene parámetros para el comando de [**\_ reproducción de MCI**](mci-play.md) para los grabadores de casete de vídeo.

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

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**dwFrom**
</dt> <dd>

Posición desde la que se va a reproducir.

</dd> <dt>

**dwTo**
</dt> <dd>

Posición en la que se va a reproducir.

</dd> <dt>

**dwAt**
</dt> <dd>

Valor de tiempo que afecta al comando [**MCI \_ Play**](mci-play.md) o [**MCI \_ CUE**](mci-cue.md) . En el caso de [**MCI \_ Play**](mci-play-parms.md), es el momento en que comienza la reproducción. En el caso de **MCI \_**, es el momento en que el dispositivo señalado alcanza la posición proporcionada en **dwFrom**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las posiciones se especifican en el formato de hora actual.

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**\_pista MCI**](mci-cue.md)
</dt> <dt>

[**reproducción de MCI \_**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

