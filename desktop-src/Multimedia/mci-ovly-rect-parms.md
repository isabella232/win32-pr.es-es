---
title: MCI_OVLY_RECT_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI OVLY \_ Rect \_ parms contiene información de posición de los \_ comandos MCI Put y MCI \_ Where para dispositivos de superposición de vídeo.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- Estructura de MCI_OVLY_RECT_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488986"
---
# <a name="mci_ovly_rect_parms-structure"></a>MCI \_ OVLY \_ Rect \_ parms estructura

La estructura **MCI \_ OVLY \_ Rect \_ parms** contiene información de posición de los comandos [**MCI \_ Put**](mci-put.md) y [**MCI \_ Where**](mci-where.md) para dispositivos de superposición de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**CR**
</dt> <dd>

Rectángulo que contiene información de posición. Las estructuras [Rect](/previous-versions//ms536136(v=vs.85)) se administran de forma diferente en MCI que en otras partes de Windows. en MCI, **RC. Right** contiene el ancho del rectángulo y **RC. Bottom** contiene el alto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**colocación de MCI \_**](mci-put.md)
</dt> <dt>

[**MCI \_ donde**](mci-where.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[RECT](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

