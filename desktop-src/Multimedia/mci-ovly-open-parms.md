---
title: Estructura de MCI_OVLY_OPEN_PARMS (mmsystem. h)
description: La \_ estructura MCI OVLY \_ Open \_ parms contiene información del comando MCI \_ Open para dispositivos de superposición de vídeo.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- Estructura de MCI_OVLY_OPEN_PARMS de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488987"
---
# <a name="mci_ovly_open_parms-structure"></a>MCI \_ OVLY \_ Open \_ parms estructura

La estructura **MCI \_ OVLY \_ Open \_ parms** contiene información del comando [**MCI \_ Open**](mci-open.md) para dispositivos de superposición de vídeo.

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

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificador devuelto a la aplicación.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nombre o identificador constante del tipo de dispositivo. (El nombre del dispositivo normalmente se obtiene del registro o del archivo de SYSTEM.INI). Si este miembro es una constante, puede ser uno de los valores enumerados en [tipos de dispositivo MCI](mci-device-types.md).

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

Identificador de la ventana primaria.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

Puede usar la estructura [**MCI \_ Open \_ parms**](mci-open-parms.md) en lugar de **MCI \_ OVLY \_ Open \_ parms** si no está usando los miembros de datos extendidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ abierto**](mci-open.md)
</dt> <dt>

[**MCI \_ abierto \_ parms**](mci-open-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

