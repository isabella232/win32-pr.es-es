---
title: MCI_VCR_STATUS_PARMS estructura (Vcr.h)
description: La estructura MCI VCR STATUS PARMS contiene parámetros para el comando MCI STATUS para las \_ \_ \_ \_ grabadoras de vídeo.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- MCI_VCR_STATUS_PARMS estructura Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370111"
---
# <a name="mci_vcr_status_parms-structure"></a>Estructura MCI \_ VCR \_ STATUS \_ PARMS

La **estructura MCI \_ VCR STATUS \_ \_ PARMS** contiene parámetros para el [**comando MCI \_ STATUS**](mci-status.md) para las grabadoras de vídeo.

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

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**dwReturn**
</dt> <dd>

Valor devuelto por el [**comando MCI \_ STATUS.**](mci-status.md) El valor devuelto varía según la consulta del comando. Para obtener más información, vea la descripción del [**comando MCI \_ STATUS.**](mci-status-parms.md)

</dd> <dt>

**dwItem**
</dt> <dd>

Tipo de información solicitada.

</dd> <dt>

**dwTrack**
</dt> <dd>

Pista de audio o vídeo que almacenará información durante la siguiente grabación. Este miembro se usa para devolver información cuando el comando [**MCI \_ STATUS**](mci-status-parms.md) pregunta sobre el estado de grabación de vídeo o audio.

</dd> <dt>

**dwNumber**
</dt> <dd>

El afinador lógico al que está asociado el canal actual. Este miembro se usa para devolver información cuando el [**comando MCI \_ STATUS**](mci-status.md) pregunta sobre el número de canal actual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

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

[**ESTADO \_ DE MCI**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

