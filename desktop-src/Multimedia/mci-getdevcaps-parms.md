---
title: MCI_GETDEVCAPS_PARMS estructura (Mciapi.h)
description: La estructura MCI GETDEVCAPS PARMS contiene información sobre la funcionalidad del dispositivo para el comando \_ \_ \_ GETDEVCAPS de MCI.
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- MCI_GETDEVCAPS_PARMS estructura Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246027"
---
# <a name="mci_getdevcaps_parms-structure"></a>Estructura \_ MCI GETDEVCAPS \_ PARMS

La **estructura \_ MCI GETDEVCAPS \_ PARMS** contiene información sobre la funcionalidad del dispositivo para el comando [**\_ GETDEVCAPS de MCI.**](mci-getdevcaps.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwReturn**
</dt> <dd>

Contiene información sobre la salida.

</dd> <dt>

**dwItem**
</dt> <dd>

Funcionalidad que se está consultando. Este miembro puede ser una de las constantes enumeradas en el material de referencia para el [**comando \_ GETDEVCAPS de MCI.**](mci-getdevcaps.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



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

 

