---
title: MCI_VCR_RECORD_PARMS estructura (Vcr.h)
description: La estructura MCI VCR RECORD PARMS contiene parámetros para el \_ \_ comando \_ MCI RECORD para las \_ grabadoras de vídeo.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- MCI_VCR_RECORD_PARMS estructura Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369980"
---
# <a name="mci_vcr_record_parms-structure"></a>Estructura MCI \_ VCR \_ RECORD \_ PARMS

La **estructura MCI \_ VCR RECORD \_ \_ PARMS** contiene parámetros para el [**comando MCI \_ RECORD**](mci-record.md) para las grabadoras de vídeo.

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

Valor de hora que afecta al [**comando MCI \_ RECORD**](mci-record.md) o [**MCI \_ CUE.**](mci-cue.md) En **el caso de MCI \_ RECORD,** es el momento en que comienza la grabación. Para **MCI \_ CUE**, es la hora en que el dispositivo cued alcanza la posición dada en **dwFrom**.

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

[**REGISTRO \_ de MCI**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

