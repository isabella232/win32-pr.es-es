---
title: MCI_VD_STEP_PARMS estructura (Mciapi.h)
description: La estructura MCI \_ VD \_ STEP \_ PARMS contiene información para el comando MCI \_ STEP para dispositivos videodisc.
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- MCI_VD_STEP_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f494c821a1df68b98548c95a10af47b817e00b8bc0ffbd52ee7836bb4d97441f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783860"
---
# <a name="mci_vd_step_parms-structure"></a>Estructura MCI \_ VD \_ STEP \_ PARMS

La **estructura MCI \_ VD STEP \_ \_ PARMS** contiene información para el [**comando MCI \_ STEP**](mci-step.md) para dispositivos videodisc.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana usado para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwFrames**
</dt> <dd>

Número de fotogramas para el paso.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**PASO \_ de MCI**](mci-step.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

