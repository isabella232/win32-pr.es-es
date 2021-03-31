---
title: MCI_STATUS_PARMS estructura (Mciapi. h)
description: La \_ estructura de \_ parms de estado de MCI contiene información para el \_ comando MCI status.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- Estructura de MCI_STATUS_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996047"
---
# <a name="mci_status_parms-structure"></a>\_Estructura parms de estado de MCI \_

La estructura de **\_ \_ parms de estado de MCI** contiene información para el comando [**MCI \_ status**](mci-status.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**dwReturn**
</dt> <dd>

Contiene información sobre la devolución.

</dd> <dt>

**dwItem**
</dt> <dd>

Capacidad que se consulta.

</dd> <dt>

**dwTrack**
</dt> <dd>

Longitud o número de pistas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La \_ marca del \_ elemento de estado de MCI debe establecerse en el parámetro *fdwCommand* de la función [**MciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar el miembro **dwItem** , que debe contener una de las constantes que indican qué información de estado se solicita.

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

[**Estado de MCI \_**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

