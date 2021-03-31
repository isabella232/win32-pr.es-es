---
title: MCI_VD_PLAY_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI Vd \_ Play \_ parms contiene información sobre la posición y la velocidad del comando MCI \_ Play para dispositivos de VideoDisc.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- Estructura de MCI_VD_PLAY_PARMS de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079414"
---
# <a name="mci_vd_play_parms-structure"></a>MCI \_ Vd \_ Play \_ parms estructura

La estructura **MCI \_ Vd \_ Play \_ parms** contiene información sobre la posición y la velocidad del comando [**MCI \_ Play**](mci-play.md) para dispositivos de VideoDisc.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**dwFrom**
</dt> <dd>

Posición desde la que se va a reproducir.

</dd> <dt>

**dwTo**
</dt> <dd>

Posición en la que se va a reproducir.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Velocidad de reproducción en fotogramas por segundo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

Puede usar la estructura [**de \_ \_ parms de reproducción de MCI**](mci-play-parms.md) en lugar de **MCI \_ Vd \_ Play \_ parms** si no está usando los miembros de datos extendidos.

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

[**reproducción de MCI \_**](mci-play.md)
</dt> <dt>

[**\_parms de reproducción de MCI \_**](mci-play-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

