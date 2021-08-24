---
title: MCI_VCR_LIST_PARMS estructura (Vcr.h)
description: La estructura MCI VCR LIST PARMS contiene parámetros para el \_ \_ comando \_ MCI LIST para las \_ grabadoras de vídeo.
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- MCI_VCR_LIST_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8eeb74aeee254ab050d394dbf250c037d00d10d51fe872052dd5d36164b2c3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137986"
---
# <a name="mci_vcr_list_parms-structure"></a>Estructura MCI \_ VCR \_ LIST \_ PARMS

La **estructura MCI \_ VCR LIST \_ \_ PARMS** contiene parámetros para el [**comando MCI \_ LIST**](mci-list.md) para las grabadoras de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwReturn**
</dt> <dd>

Búfer para la información devuelta.

</dd> <dt>

**dwNumber**
</dt> <dd>

Número de entradas de audio o vídeo de VCR.

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

[**LISTA \_ de MCI**](mci-list.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

