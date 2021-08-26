---
title: MCI_BREAK_PARMS estructura (Mciapi.h)
description: La estructura MCI BREAK PARMS contiene información de ventana y código de clave \_ virtual para el comando BREAK de \_ \_ MCI.
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- MCI_BREAK_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efaff8841e0e8ef0387535aa8d42723cf9477887511b7111f02a6ee0cb2b527b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039515"
---
# <a name="mci_break_parms-structure"></a>Estructura \_ MCI BREAK \_ PARMS

La **estructura MCI \_ BREAK \_ PARMS** contiene información de ventana y código de clave virtual para el [**comando BREAK \_ de MCI.**](mci-break.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**nVirtKey**
</dt> <dd>

Código de clave virtual para la clave de interrupción.

</dd> <dt>

**hwndBreak**
</dt> <dd>

Identificador de la ventana que debe ser la ventana actual para la detección de saltos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros. Se definen las marcas siguientes:

MCI \_ BREAK \_ HWND

Valida el **miembro hwndBreak** que especifica la ventana que debe tener el foco para habilitar la detección de saltos.

CLAVE DE \_ INTERRUPCIÓN DE MCI \_

Valida el **miembro nVirtKey** que especifica el código de clave virtual que se va a usar para la clave de interrupción.

MCI \_ BREAK \_ OFF

Deshabilita cualquier clave de interrupción existente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**MCI \_ BREAK**](mci-break.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

