---
title: MCI_SYSINFO_PARMS estructura (Mciapi. h)
description: La \_ \_ estructura de parms de MCI sysinfo contiene información para el comando de MCI \_ sysinfo.
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- Estructura de MCI_SYSINFO_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676555"
---
# <a name="mci_sysinfo_parms-structure"></a>\_ \_ Estructura parms de MCI SYSINFO

La estructura de **\_ \_ parms de MCI sysinfo** contiene información para el comando de [**MCI \_ sysinfo**](mci-sysinfo.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**lpstrReturn**
</dt> <dd>

Puntero a un búfer proporcionado por el usuario para la cadena devuelta. También se usa para devolver un valor **DWORD** cuando \_ se usa la marca de cantidad de MCI SYSINFO \_ .

</dd> <dt>

**dwRetSize**
</dt> <dd>

Tamaño, en bytes, del búfer de retorno.

</dd> <dt>

**dwNumber**
</dt> <dd>

Número que indica la posición del dispositivo en la tabla de dispositivos MCI o en la lista de dispositivos abiertos \_ si \_ se establece la marca de apertura de MCI SYSINFO.

</dd> <dt>

**wDeviceType**
</dt> <dd>

Tipo de dispositivo. Este miembro puede ser uno de los valores enumerados en [tipos de dispositivo MCI](mci-device-types.md).

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

[**MCI \_ SYSINFO**](mci-sysinfo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

