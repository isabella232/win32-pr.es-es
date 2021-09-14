---
title: MCI_SYSINFO_PARMS estructura (Mciapi.h)
description: La estructura \_ MCI SYSINFO \_ PARMS contiene información para el \_ comando SYSINFO de MCI.
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- MCI_SYSINFO_PARMS estructura Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246009"
---
# <a name="mci_sysinfo_parms-structure"></a>Estructura \_ MCI SYSINFO \_ PARMS

La **estructura \_ MCI SYSINFO \_ PARMS** contiene información para el [**comando \_ SYSINFO de MCI.**](mci-sysinfo.md)

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



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**lpstrReturn**
</dt> <dd>

Puntero a un búfer proporcionado por el usuario para la cadena de devolución. También se usa para devolver un valor **DWORD** cuando se usa la marca \_ MCI SYSINFO \_ QUANTITY.

</dd> <dt>

**dwRetSize**
</dt> <dd>

Tamaño, en bytes, del búfer devuelto.

</dd> <dt>

**dwNumber**
</dt> <dd>

Número que indica la posición del dispositivo en la tabla de dispositivos MCI o en la lista de dispositivos abiertos si se establece la marca \_ MCI SYSINFO \_ OPEN.

</dd> <dt>

**wDeviceType**
</dt> <dd>

Tipo de dispositivo. Este miembro puede ser uno de los valores enumerados en [Tipos de dispositivo de MCI.](mci-device-types.md)

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

[**SYSINFO de MCI \_**](mci-sysinfo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

