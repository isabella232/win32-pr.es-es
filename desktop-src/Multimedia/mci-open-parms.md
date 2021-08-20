---
title: MCI_OPEN_PARMS estructura (Mciapi.h)
description: La estructura MCI \_ OPEN \_ PARMS contiene información para el comando MCI \_ OPEN.
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- MCI_OPEN_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80d01f41db904cea583f83aa446e718d1067e99e4d8bac3a3c6791ef5696f83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138310"
---
# <a name="mci_open_parms-structure"></a>Estructura \_ MCI OPEN \_ PARMS

La **estructura MCI \_ OPEN \_ PARMS** contiene información para el [**comando MCI \_ OPEN.**](mci-open.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
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

Elemento Device (a menudo una ruta de acceso).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias de dispositivo opcional.

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

[**MCI \_ OPEN**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

