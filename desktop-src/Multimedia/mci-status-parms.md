---
title: MCI_STATUS_PARMS estructura (Mciapi.h)
description: La estructura MCI \_ STATUS \_ PARMS contiene información para el comando MCI \_ STATUS.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- MCI_STATUS_PARMS estructura Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370124"
---
# <a name="mci_status_parms-structure"></a>Estructura MCI \_ STATUS \_ PARMS

La **estructura MCI \_ STATUS \_ PARMS** contiene información para el [**comando MCI \_ STATUS.**](mci-status.md)

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

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwReturn**
</dt> <dd>

Contiene información sobre la devolución.

</dd> <dt>

**dwItem**
</dt> <dd>

Funcionalidad que se está consultando.

</dd> <dt>

**dwTrack**
</dt> <dd>

Longitud o número de pistas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La marca MCI STATUS ITEM debe establecerse en el parámetro fdwCommand de la función \_ \_ [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))  para validar el **miembro dwItem,** que debe contener una de las constantes que indican qué información de estado se solicita.

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

[**ESTADO \_ DE MCI**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

