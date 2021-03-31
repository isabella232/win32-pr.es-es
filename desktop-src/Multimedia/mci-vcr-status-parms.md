---
title: MCI_VCR_STATUS_PARMS estructura (VCR. h)
description: La \_ estructura MCI VCR \_ status \_ parms contiene parámetros para el \_ comando MCI status para los grabadores de casete de vídeo.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- Estructura de MCI_VCR_STATUS_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995999"
---
# <a name="mci_vcr_status_parms-structure"></a>\_ \_ Estructura parms de estado del VCR de MCI \_

La estructura **MCI \_ VCR \_ status \_ parms** contiene parámetros para el comando [**MCI \_ status**](mci-status.md) para los grabadores de casete de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**dwReturn**
</dt> <dd>

Valor devuelto por el comando [**MCI \_ status**](mci-status.md) . El valor devuelto varía según la consulta del comando. Para obtener más información, consulte la descripción del comando [**MCI \_ status**](mci-status-parms.md) .

</dd> <dt>

**dwItem**
</dt> <dd>

Tipo de información solicitada.

</dd> <dt>

**dwTrack**
</dt> <dd>

Pista de audio o vídeo que almacenará información durante la siguiente grabación. Este miembro se usa para devolver información cuando el comando de [**\_ Estado de MCI**](mci-status-parms.md) consulta el estado de grabación de audio o vídeo.

</dd> <dt>

**dwNumber**
</dt> <dd>

Sintonizador lógico al que está asociado el canal actual. Este miembro se usa para devolver información cuando el comando de [**\_ Estado de MCI**](mci-status.md) consulta el número de canal actual.

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

[**Estado de MCI \_**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

