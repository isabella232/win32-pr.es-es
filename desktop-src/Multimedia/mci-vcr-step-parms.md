---
title: MCI_VCR_STEP_PARMS estructura (Vcr.h)
description: La estructura MCI VCR STEP PARMS contiene parámetros para el \_ \_ comando \_ MCI STEP para las \_ grabadoras de vídeo.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- MCI_VCR_STEP_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a616b31500a2c814edb3dd443586131ed0ffae7d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370171"
---
# <a name="mci_vcr_step_parms-structure"></a>Estructura MCI \_ VCR \_ STEP \_ PARMS

La **estructura MCI \_ VCR STEP \_ \_ PARMS** contiene parámetros para el [**comando MCI \_ STEP**](mci-step.md) para las grabadoras de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwFrames**
</dt> <dd>

Número de fotogramas para saltar (la longitud de un solo paso) a medida que el comando [**MCI \_ STEP**](mci-step.md) avanza o retrocede por el contenido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

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

[**PASO \_ de MCI**](mci-step.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

