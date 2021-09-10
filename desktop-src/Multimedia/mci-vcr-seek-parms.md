---
title: MCI_VCR_SEEK_PARMS estructura (Vcr.h)
description: La estructura MCI \_ VCR SEEK PARMS contiene parámetros para el comando MCI SEEK para \_ las \_ \_ grabadoras de vídeo.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- MCI_VCR_SEEK_PARMS de Windows multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370046"
---
# <a name="mci_vcr_seek_parms-structure"></a>Estructura \_ MCI VCR \_ SEEK \_ PARMS

La **estructura MCI \_ VCR SEEK \_ \_ PARMS** contiene parámetros para el [**comando MCI \_ SEEK**](mci-seek.md) para las grabadoras de vídeo.

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

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwTo**
</dt> <dd>

Posición a la que buscar.

</dd> <dt>

**dwMark**
</dt> <dd>

Marca numerada que se buscará.

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
| Encabezado<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ SEEK**](mci-seek.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

