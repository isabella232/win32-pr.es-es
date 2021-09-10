---
title: MCI_OVLY_OPEN_PARMS estructura (Mmsystem.h)
description: La estructura MCI \_ OVLY OPEN PARMS contiene información para el comando MCI OPEN para dispositivos \_ de \_ \_ superposición de vídeo.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- MCI_OVLY_OPEN_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370027"
---
# <a name="mci_ovly_open_parms-structure"></a>Estructura \_ MCI OVLY \_ OPEN \_ PARMS

La **estructura MCI \_ OVLY \_ OPEN \_ PARMS** contiene información para el [**comando MCI \_ OPEN**](mci-open.md) para dispositivos de superposición de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificador devuelto a la aplicación.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nombre o identificador constante del tipo de dispositivo. (El nombre del dispositivo normalmente se obtiene del registro o SYSTEM.INI archivo). Si este miembro es una constante, puede ser uno de los valores enumerados en [Tipos de dispositivo de MCI.](mci-device-types.md)

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Nombre del elemento de dispositivo (normalmente una ruta de acceso).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias de dispositivo opcional.

</dd> <dt>

**dwStyle**
</dt> <dd>

Estilo de ventana.

</dd> <dt>

**hWndParent**
</dt> <dd>

Controlar a la ventana primaria.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

Puede usar la estructura [**MCI \_ OPEN \_ PARMS**](mci-open-parms.md) en lugar de **MCI \_ OVLY \_ OPEN \_ PARMS** si no usa los miembros de datos extendidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ OPEN**](mci-open.md)
</dt> <dt>

[**MCI \_ OPEN \_ PARMS**](mci-open-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

