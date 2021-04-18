---
title: MCI_VD_ESCAPE_PARMS estructura (Mciapi. h)
description: La estructura parms de los caracteres de escape de MCI \_ Vd \_ \_ contiene el comando que se envía a un dispositivo para el \_ comando MCI escape para dispositivos de VideoDisc.
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- Estructura de MCI_VD_ESCAPE_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80712cd693e2c7ebe290be6b9827c1e051dd86a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676717"
---
# <a name="mci_vd_escape_parms-structure"></a>\_ \_ Estructura parms de secuencias de escape de MCI Vd \_

La **estructura \_ \_ \_ parms** de los caracteres de escape de MCI Vd contiene el comando que se envía a un dispositivo para el comando [**MCI \_ escape**](mci-escape.md) para dispositivos de VideoDisc.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**lpstrCommand**
</dt> <dd>

Comando que se va a enviar a un dispositivo.

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

[**ESCAPE de MCI \_**](mci-escape.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

