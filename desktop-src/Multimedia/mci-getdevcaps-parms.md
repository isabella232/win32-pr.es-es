---
title: MCI_GETDEVCAPS_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI GETDEVCAPS \_ parms contiene información sobre la capacidad del dispositivo para el \_ comando MCI GETDEVCAPS.
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- Estructura de MCI_GETDEVCAPS_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079065"
---
# <a name="mci_getdevcaps_parms-structure"></a>\_GETDEVCAPS MCI \_ parms estructura

La estructura **MCI \_ GETDEVCAPS \_ parms** contiene información sobre la capacidad del dispositivo para el comando [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**dwReturn**
</dt> <dd>

Contiene información sobre la salida.

</dd> <dt>

**dwItem**
</dt> <dd>

Capacidad que se consulta. Este miembro puede ser una de las constantes enumeradas en el material de referencia del comando [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .

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

[**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

