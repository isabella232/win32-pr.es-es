---
title: MCI_VD_PLAY_PARMS estructura (Mciapi.h)
description: La estructura MCI VD PLAY PARMS contiene información de posición y velocidad para el \_ \_ comando \_ MCI PLAY para \_ dispositivos videodisc.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- MCI_VD_PLAY_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ab04ba5cf0a2b507370a4b777c19fd60a05c30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245865"
---
# <a name="mci_vd_play_parms-structure"></a>Estructura MCI \_ VD \_ PLAY \_ PARMS

La **estructura MCI \_ VD PLAY \_ \_ PARMS** contiene información de posición y velocidad para el [**comando MCI \_ PLAY**](mci-play.md) para dispositivos videodisc.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posición desde la que se reproducirá.

</dd> <dt>

**dwTo**
</dt> <dd>

Posición en la que se reproducirá.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Velocidad de reproducción en fotogramas por segundo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

Puede usar la estructura [**MCI \_ PLAY \_ PARMS**](mci-play-parms.md) en lugar de **MCI \_ VD PLAY \_ \_ PARMS** si no usa los miembros de datos extendidos.

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

[**MCI \_ PLAY**](mci-play.md)
</dt> <dt>

[**MCI \_ PLAY \_ PARMS**](mci-play-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

