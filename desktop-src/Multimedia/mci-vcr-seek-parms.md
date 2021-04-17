---
title: MCI_VCR_SEEK_PARMS estructura (VCR. h)
description: La \_ estructura de parms de VCR VCR \_ Seek \_ contiene los parámetros para el \_ comando MCI Seek para los grabadores de casete de vídeo.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- Estructura de MCI_VCR_SEEK_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489898"
---
# <a name="mci_vcr_seek_parms-structure"></a>\_Estructura parms de VCR VCR \_ Seek \_

La estructura de **\_ parms de VCR VCR \_ Seek \_** contiene los parámetros para el comando [**MCI \_ Seek**](mci-seek.md) para los grabadores de casete de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**dwTo**
</dt> <dd>

Posición en la que se va a buscar.

</dd> <dt>

**dwMark**
</dt> <dd>

Marca numerada que se va a buscar.

</dd> <dt>

**dwAt**
</dt> <dd>

Hora a la que comienza la búsqueda.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las posiciones se especifican en el formato de hora actual.

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**búsqueda de MCI \_**](mci-seek.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

