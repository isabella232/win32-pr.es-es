---
title: MCI_OVLY_LOAD_PARMS estructura (Mmsystem.h)
description: La estructura MCI OVLY LOAD PARMS contiene información para el comando MCI LOAD para dispositivos \_ \_ de \_ \_ superposición de vídeo.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- MCI_OVLY_LOAD_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc966b51224246dbceda46927f605c214ba4809a1cca451813a1075811fa5225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039105"
---
# <a name="mci_ovly_load_parms-structure"></a>Estructura \_ MCI OVLY \_ LOAD \_ PARMS

La **estructura MCI \_ OVLY \_ LOAD \_ PARMS** contiene información para el [**comando MCI \_ LOAD**](mci-load.md) para dispositivos de superposición de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**lpfilename**
</dt> <dd>

Nombre del archivo que se cargará.

</dd> <dt>

**Rc**
</dt> <dd>

Identifica el área del búfer de vídeo que se actualizará. [Las estructuras RECT](/previous-versions//ms536136(v=vs.85)) se controlan de forma diferente en MCI que en otras partes de Windows; en MCI, **rc.right** contiene el ancho del rectángulo y **rc.bottom** contiene su alto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ LOAD**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[Rect](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

