---
title: MCI_VCR_RECORD_PARMS estructura (VCR. h)
description: La \_ estructura parms del registro VCR de MCI \_ \_ contiene los parámetros para el \_ comando MCI record para los grabadores de casete de vídeo.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- Estructura de MCI_VCR_RECORD_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676702"
---
# <a name="mci_vcr_record_parms-structure"></a>\_ \_ Estructura parms del registro VCR de MCI \_

La **estructura \_ \_ \_ parms del registro VCR de MCI** contiene los parámetros para el comando [**MCI \_ Record**](mci-record.md) para los grabadores de casete de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
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

Valor de tiempo que afecta al comando [**MCI \_ Record**](mci-record.md) o [**MCI \_ CUE**](mci-cue.md) . En el caso del **\_ registro MCI**, es el momento en el que comienza la grabación. En el caso de **MCI \_**, es el momento en que el dispositivo señalado alcanza la posición proporcionada en **dwFrom**.

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

[**registro de MCI \_**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

