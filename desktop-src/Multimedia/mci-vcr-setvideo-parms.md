---
title: MCI_VCR_SETVIDEO_PARMS estructura (VCR. h)
description: La \_ estructura MCI VCR \_ SETVIDEO \_ parms contiene parámetros para el \_ comando MCI SETVIDEO para los grabadores de casete de vídeo.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- Estructura de MCI_VCR_SETVIDEO_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905538"
---
# <a name="mci_vcr_setvideo_parms-structure"></a>\_SETVIDEO MCI \_ VCR \_ parms estructura

La estructura **MCI \_ VCR \_ SETVIDEO \_ parms** contiene parámetros para el comando [**MCI \_ SETVIDEO**](mci-setvideo.md) para los grabadores de casete de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**dwTrack**
</dt> <dd>

Pista afectada.

</dd> <dt>

**dwTo**
</dt> <dd>

Tipo de entrada o entrada supervisada.

</dd> <dt>

**dwNumber**
</dt> <dd>

Entrada de vídeo (del tipo especificado en el miembro **dwTo** ) que se va a usar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

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

[**MCI \_ SETVIDEO**](mci-setvideo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

