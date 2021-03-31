---
title: MCI_VCR_SETTUNER_PARMS estructura (VCR. h)
description: La \_ estructura MCI VCR \_ SETTUNER \_ parms contiene parámetros para el \_ comando MCI SETTUNER para los grabadores de casete de vídeo.
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- Estructura de MCI_VCR_SETTUNER_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891ddf3b4b3dcb9532a2431901b0b2b9d84b0e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802503"
---
# <a name="mci_vcr_settuner_parms-structure"></a>\_SETTUNER MCI \_ VCR \_ parms estructura

La estructura **MCI \_ VCR \_ SETTUNER \_ parms** contiene parámetros para el comando [**MCI \_ SETTUNER**](mci-settuner.md) para los grabadores de casete de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**dwChannel**
</dt> <dd>

Nuevo número de canal.

</dd> <dt>

**dwNumber**
</dt> <dd>

Sintonizador lógico al que afecta el comando [**\_ SETTUNER de MCI**](mci-settuner.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

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

[**MCI \_ SETTUNER**](mci-settuner.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

