---
title: MCI_BREAK_PARMS estructura (Mciapi. h)
description: La \_ estructura de \_ parms de interrupción de MCI contiene código de clave virtual e información de ventana para el comando de interrupción de MCI \_ .
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- Estructura de MCI_BREAK_PARMS de Windows multimedia
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
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534017"
---
# <a name="mci_break_parms-structure"></a>\_Estructura parms de interrupción de MCI \_

La estructura de **\_ \_ parms de interrupción de MCI** contiene código de clave virtual e información de ventana para el comando de [**\_ interrupción de MCI**](mci-break.md) .

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

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**nVirtKey**
</dt> <dd>

Código de clave virtual para la clave de interrupción.

</dd> <dt>

**hwndBreak**
</dt> <dd>

Identificador de la ventana que debe ser la ventana actual para la detección de interrupciones.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros. Se definen las marcas siguientes:

\_hWnd de interrupción de MCI \_

Valida el miembro **hwndBreak** que especifica la ventana que debe tener el foco para habilitar la detección de interrupciones.

\_tecla de interrupción de MCI \_

Valida el miembro de **nVirtKey** que especifica el código de la clave virtual que se va a usar para la clave de interrupción.

interrupción de MCI \_ \_

Deshabilita cualquier clave de interrupción existente.

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

[**interrupción de MCI \_**](mci-break.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

