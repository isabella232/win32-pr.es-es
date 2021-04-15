---
title: MCI_WAVE_OPEN_PARMS estructura (Mciapi. h)
description: La estructura de parms de MCI \_ \_ Open Wave \_ contiene información para el \_ comando MCI Open para dispositivos de audio de forma de onda.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- Estructura de MCI_WAVE_OPEN_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676861"
---
# <a name="mci_wave_open_parms-structure"></a>\_ \_ Estructura parms de MCI Open Wave \_

La estructura de **parms de MCI \_ \_ Open \_ Wave** contiene información para el comando [**MCI \_ Open**](mci-open.md) para dispositivos de audio de forma de onda.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificador devuelto a la aplicación.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nombre o identificador constante del tipo de dispositivo. (El nombre del dispositivo normalmente se obtiene del registro o del archivo de SYSTEM.INI). Este miembro puede ser uno de los valores enumerados en [tipos de dispositivo MCI](mci-device-types.md).

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Nombre del elemento de dispositivo (normalmente una ruta de acceso).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias de dispositivo opcional.

</dd> <dt>

**dwBufferSeconds**
</dt> <dd>

Longitud del búfer, en segundos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

Puede usar la estructura [**MCI \_ Open \_ parms**](mci-open-parms.md) en lugar de **MCI \_ Wave \_ Open \_ parms** si no está usando los miembros de datos extendidos.

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

[**MCI \_ abierto**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCI \_ abierto \_ parms**](mci-open-parms.md)
</dt> </dl>

 

