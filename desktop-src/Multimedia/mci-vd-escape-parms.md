---
title: MCI_VD_ESCAPE_PARMS estructura (Mciapi.h)
description: La estructura MCI VD ESCAPE PARMS contiene el comando enviado a un dispositivo para el comando ESCAPE de \_ \_ \_ MCI \_ para dispositivos videodisc.
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- MCI_VD_ESCAPE_PARMS estructura Windows Multimedia
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
ms.openlocfilehash: 2f9a0fef0e60168d4539756c741527d751fd726ab3d2472cdbaf3b080784e70c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783850"
---
# <a name="mci_vd_escape_parms-structure"></a>Estructura MCI \_ VD \_ ESCAPE \_ PARMS

La **estructura MCI \_ VD ESCAPE \_ \_ PARMS** contiene el comando enviado a un dispositivo para el comando ESCAPE de [**MCI \_**](mci-escape.md) para dispositivos videodisc.

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

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**lpstrCommand**
</dt> <dd>

Comando que se envía al dispositivo.

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

[**ESCAPE \_ de MCI**](mci-escape.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

